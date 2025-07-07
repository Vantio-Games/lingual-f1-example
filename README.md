# F1 API

An unofficial SDK for the [Formula 1 API](https://f1api.dev/).

## Language Packages

This repository automatically generates language-specific packages for multiple programming languages using [Lingual](https://github.com/lingual-lang/lingual). The packages are built from the `f1.example` source file and deployed to separate branches.

### Available Language Packages

- **C#**: `csharp` branch
- **TypeScript**: `typescript` branch  
- **JavaScript**: `javascript` branch
- **Python**: `python` branch
- **GDScript**: `gdscript` branch

### CI/CD Workflow

The repository uses GitHub Actions to automatically:

1. **Build**: When changes are pushed to the `main` branch, the workflow runs `npx lingual-lang build f1.example`
2. **Generate**: Creates language-specific packages in the `out/` directory
3. **Deploy**: Pushes each language's package to its respective branch

### Development

To modify the API definitions, edit the `f1.example` file and push to the `main` branch. The CI/CD pipeline will automatically rebuild and deploy all language packages.

### Local Development

To build packages locally:

```bash
# Install lingual-lang globally
npm install -g lingual-lang

# Build packages
npx lingual-lang build f1.example
```

The generated packages will be available in the `out/` directory.
