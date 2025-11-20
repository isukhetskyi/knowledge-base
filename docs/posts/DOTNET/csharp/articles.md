[Enhance your .NET Testing #7: 5 best practices to write better tests](https://goatreview.com/5-best-practices-write-better-tests/) - by [Pierre Belin](https://goatreview.com/author/pierre-belin/)

***

Reliable software testing is essential for quality, but poorly written tests—especially those causing false positives—can be more harmful than no tests at all. The article outlines five key rules for creating effective, maintainable tests.

1.  **No Conditions or Loops:** Tests must remain pure. Avoid `if` statements or `for` loops, as they add logic and complexity. Instead of testing multiple scenarios in a loop, separate each case into its own distinct test.

2.  **Use the AAA Pattern:** Structure every test using **Arrange** (set up all necessary data), **Act** (call a *single* function to be tested), and **Assert** (validate the outcome). If you feel the need to use this pattern more than once, the test should be split.

3.  **Clear Naming Conventions:** Test names serve as crucial, living documentation. Use descriptive patterns inspired by Behavior-Driven Development (BDD), such as `Should[ResultExpected]_When[CaseTested]` or `Given[InitialCondition]_When[CaseTested]_Then[ResultExpected]`.

4.  **Improve Assertion Readability:** Employ libraries like **FluentAssertions** to make validation logic more natural and human-readable (e.g., `actual.Should().Be(expected)` is clearer than `Assert.AreEqual(expected, actual)`).

5.  **Use Mocks Sparingly:** Mocks are necessary for isolating unit tests from external dependencies (like databases or APIs). However, mocking complex *internal* classes is a "red flag" indicating that the internal class itself is poorly designed and should be refactored.

***

### [Mastering the C# Dispose Pattern]()(https://blog.ivankahl.com/csharp-dispose-pattern/) - by [Ivan Kahl](https://ivankahl.com/)

***

In C#, the `IDisposable` interface is crucial for deterministically cleaning up **unmanaged resources**—like database connections, file handles, or network sockets—which the .NET Garbage Collector (GC) cannot manage.

The article details two primary implementations:

1.  **The Basic Dispose Pattern:** This is the most common scenario, used when a class *owns* other objects that already implement `IDisposable` (e.g., an `NpgsqlConnection`). The class's `Dispose()` method simply calls `Dispose()` on its owned members. It must also be made **idempotent** (safe to call multiple times) by using a private `_disposed` boolean flag. Consumers should use the `using` statement to ensure `Dispose()` is called automatically.

2.  **The Full Dispose Pattern:** This pattern is necessary when a class *directly* manages raw unmanaged resources (e.g., an `IntPtr`). It is more complex and involves:
    * A public `Dispose()` method that calls `GC.SuppressFinalize(this)`.
    * A **finalizer** (destructor `~ClassName()`) to act as a fallback.
    * A `protected virtual Dispose(bool disposing)` method to centralize cleanup logic.

This `disposing` boolean differentiates between a deterministic call (freeing *both* managed and unmanaged resources) and a finalizer call (freeing *only* unmanaged resources).

The article also covers best practices, such as how to handle inheritance by overriding `Dispose(bool)`, and recommends using **`SafeHandle`** to wrap raw pointers, which simplifies the full pattern back to the basic one. Finally, it introduces **`IAsyncDisposable`** for resources requiring asynchronous cleanup, which is consumed using `await using`.