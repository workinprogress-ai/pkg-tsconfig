# @workinprogress-ai/tsconfig

Shared TypeScript configurations for WIP projects

## Installation

```bash
pnpm add -D @workinprogress-ai/tsconfig typescript
```

## Usage

Create a `tsconfig.json` in your project and extend the desired configuration.

## Configurations

| Configuration        | Purpose                      | Best For                        |
| -------------------- | ---------------------------- | ------------------------------- |
| `base.json`          | Base strict configuration    | Starting point for all projects |
| `library.json`       | General TypeScript libraries | Utils, SDKs, tools              |
| `react-library.json` | React component libraries    | React components, hooks         |
| `vite.json`          | Vite applications            | React apps with Vite            |
| `node.json`          | Node.js applications         | Backend services, CLIs          |

## Usage Examples

### Base Configuration

```json
// tsconfig.json
{
    "extends": "@workinprogress-ai/tsconfig/base.json",
    "compilerOptions": {
        "outDir": "./dist"
    },
    "include": ["src"]
}
```

### General Library

```json
// tsconfig.json
{
    "extends": "@workinprogress-ai/tsconfig/library.json",
    "compilerOptions": {
        "outDir": "./dist",
        "rootDir": "./src"
    },
    "include": ["src"]
}
```

### React Library

```json
// tsconfig.json
{
    "extends": "@workinprogress-ai/tsconfig/react-library.json",
    "include": ["src"],
    "compilerOptions": {
        "outDir": "./dist"
    }
}
```

### Vite App

For applications built with Vite.

```json
// tsconfig.json
{
    "extends": "@workinprogress-ai/tsconfig/vite.json",
    "include": ["src", "**/*.ts", "**/*.tsx"]
}
```

### Node.js App

```json
// tsconfig.json
{
    "extends": "@workinprogress-ai/tsconfig/node.json",
    "compilerOptions": {
        "outDir": "./build"
    },
    "include": ["src"]
}
```
