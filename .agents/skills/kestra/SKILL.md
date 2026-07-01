```markdown
# kestra Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `kestra` TypeScript codebase. You'll learn about file naming, import/export styles, commit conventions, and how to structure and run tests. This guide is designed to help contributors quickly align with the project's established practices for consistent, maintainable code.

## Coding Conventions

### File Naming
- **Convention:** camelCase
- **Example:**  
  ```plaintext
  myUtilityFile.ts
  processData.ts
  ```

### Import Style
- **Convention:** Relative imports
- **Example:**
  ```typescript
  import { processData } from './processData';
  import { helper } from '../utils/helper';
  ```

### Export Style
- **Convention:** Named exports
- **Example:**
  ```typescript
  // In processData.ts
  export function processData(input: string): string {
    // ...
  }
  ```

### Commit Messages
- **Convention:** Conventional commits with type prefixes (e.g., `build`)
- **Example:**
  ```
  build: update dependencies to latest versions
  ```

## Workflows

### Building the Project
**Trigger:** When you need to build the project for development or production  
**Command:** `/build`

1. Ensure all dependencies are installed.
2. Run the build script (typically `npm run build` or `yarn build`).
3. Verify that the output is generated without errors.

### Writing Code
**Trigger:** When adding new features or fixing bugs  
**Command:** `/write-code`

1. Create new files using camelCase naming.
2. Use relative imports for all internal modules.
3. Export functions and constants using named exports.
4. Write clear, conventional commit messages with appropriate prefixes.

### Testing Code
**Trigger:** When you need to verify code correctness  
**Command:** `/test`

1. Create test files matching the `*.test.*` pattern (e.g., `myFunction.test.ts`).
2. Write tests using the project's chosen (unknown) framework.
3. Run tests using the project's test script (e.g., `npm test` or `yarn test`).

## Testing Patterns

- **Test File Naming:**  
  Use the `*.test.*` pattern for test files.
  ```plaintext
  processData.test.ts
  utils.test.ts
  ```
- **Framework:**  
  Not explicitly detected; refer to project documentation or `package.json` for details.
- **Test Example:**
  ```typescript
  import { processData } from './processData';

  describe('processData', () => {
    it('should process input correctly', () => {
      expect(processData('input')).toBe('expectedOutput');
    });
  });
  ```

## Commands
| Command      | Purpose                                      |
|--------------|----------------------------------------------|
| /build       | Build the project                            |
| /write-code  | Start writing code following conventions      |
| /test        | Run the test suite                           |
```
