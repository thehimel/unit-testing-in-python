#

## Overview of TDD

![img.png](tdd.png)

- Before moving to our exercises, I want to take a step back to explain how test-driven development relates to unit
testing. As we move through this section we will primarily use the lens of test-driven development to implement
functionality in the source code and write accompanying tests. To guide how we use test-driven development, it's
important to first think about what behaviors we want our system to execute, even before we implement it in code.
- **Test-driven development is a software development process that can be used while writing unit tests.** Using this
method of writing software at the start, influences how the developer writes modular tests that will illustrate what
features their system will carry out.
  - First, the developer writes a test that will surely fail without code to implement its behavior. This is also known
  as being in a red failure state.
  - Then the developer must make sure it eventually passes by writing the minimum implementation code needed to get this
  test passing.
  - Once that's been done, this test, along with the rest of the tests should be run to make sure the entire project is
  in a passing state. If the new implementation code has caused other tests to fail, then the developer needs to
  refactor as necessary.
  - After all needed factoring is complete the tests are now in a green, or passing state. This shortens the development
  cycle, influencing the developer to focus on functionality in small pieces on the forefront. It's their job to
  iteratively stitch these pieces together to get a final system. Additionally, when behaviors are clearly defined
  during the development process, the developer can think about ways they might extend the project to include new
  features in the future. As such, new code written down the line can be structured to potentially build-off of or
  reuse existing behaviors. This helps the developer avoid being overwhelmed by the desire to implement all the core
  functionality at once. Instead, they can focus on gradually adding features as they go.
- Using test-driven development with behaviors in mind also facilitates code reuse in the broader community. Think about
it like this, if you downloaded another developer's project that promised to solve a huge problem you had, you'd expect
to make use of the functionality they promised. However, if you ran their code and encountered errors, you most likely
avoid using their projects and search for another solution. To avoid a situation like this ourselves, it's important to
communicate behaviors explicitly as you develop, verifying that those behaviors are indeed occurring. We will use the
test-driven development method of writing tests strategically within this course with behaviors in mind. As we do this,
we will cover basic debugging tips and tricks that will help us navigate the refactoring process as we attempt to get
our test passing again, or in the green.
