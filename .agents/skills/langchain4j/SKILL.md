```markdown
# langchain4j Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `langchain4j` Java codebase. You'll learn about file naming, import/export styles, commit message patterns, and how to write and organize tests. While no automated workflows were detected, this guide provides suggested commands and step-by-step instructions for common development tasks.

## Coding Conventions

### File Naming
- **Style:** PascalCase  
  Example:  
  ```java
  public class MyAwesomeClass { ... }
  ```

### Import Style
- **Relative Imports:**  
  Use relative paths when importing classes from the same project.
  ```java
  import com.myproject.module.MyClass;
  ```

### Export Style
- **Named Exports:**  
  Export classes or interfaces using named exports.
  ```java
  public class LangChainEngine { ... }
  public interface Chainable { ... }
  ```

### Commit Messages
- **Type:** Mixed (no strict convention, but some use `fix` prefix)
- **Prefix Example:**  
  ```
  fix: correct typo in ChainProcessor
  ```
- **Average Length:** ~57 characters

## Workflows

### Adding a New Feature
**Trigger:** When implementing new functionality  
**Command:** `/add-feature`

1. Create a new Java file using PascalCase for the class name.
2. Implement your feature, using relative imports for dependencies.
3. Export your class or interface with a named export.
4. Write corresponding tests in a file matching `*.test.*`.
5. Commit your changes with a descriptive message.

### Fixing a Bug
**Trigger:** When resolving a bug or issue  
**Command:** `/fix-bug`

1. Locate the problematic code.
2. Apply the fix, following the code style conventions.
3. Update or add tests to cover the bug fix.
4. Commit with a message prefixed by `fix:`, e.g.,  
   ```
   fix: handle null pointer in LangChainEngine
   ```

### Writing and Running Tests
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Write test files using the `*.test.*` naming pattern.
2. Use the project's (unknown) test framework to implement tests.
3. Run tests using the appropriate build or test command for the project.

## Testing Patterns

- **Test File Naming:**  
  Test files follow the pattern `*.test.*` (e.g., `LangChainEngine.test.java`).
- **Framework:**  
  The specific testing framework is unknown, but standard Java testing frameworks like JUnit are likely.
- **Example Test File:**
  ```java
  // LangChainEngine.test.java
  import org.junit.Test;
  import static org.junit.Assert.*;

  public class LangChainEngineTest {
      @Test
      public void testProcessChain() {
          // test logic here
      }
  }
  ```

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /add-feature | Start a new feature implementation      |
| /fix-bug     | Apply and commit a bug fix              |
| /run-tests   | Run all tests in the codebase           |
```
