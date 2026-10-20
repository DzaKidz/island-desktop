# Island for Windows

Desktop application built with Tauri, Rust, and JavaScript.

## Requirements

- Node.js and npm
- Rust
- Visual Studio Build Tools with "Desktop development with C++"
- Microsoft Edge WebView2 Runtime

## Development

```sh
npm ci
npm run dev
```

The first build compiles the Rust dependencies and can take a few minutes.
The interface lives in `src/index.html`.
Quit the application from Task Manager if it has no taskbar icon.

## Build an installer

```sh
npm run build
```

The NSIS installer is generated in `src-tauri/target/release/bundle/nsis/`.

## Repository contents

Keep source code, configuration, icons, `package-lock.json`, and
`src-tauri/Cargo.lock` in Git. Dependencies, compiled output, and generated
Tauri schemas are excluded by `.gitignore` and recreated when installing
dependencies or building the application.

Share built installers separately from the source repository.
