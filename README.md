# IDE

IDE is a desktop code editor project built on the open-source [Code - OSS](https://github.com/microsoft/vscode) codebase. The upstream project provides the editor, workbench, extension host, terminal, source control, and language tooling; this repository is the foundation for making them our own.

This repository currently uses the upstream Code - OSS product identity and behavior. Product branding and project-specific features can be developed on top of this base.

## Source and license

- Upstream: [microsoft/vscode](https://github.com/microsoft/vscode)
- Imported snapshot: [`ebfd846096ecc3e7752b8af6a3197952281769a0`](https://github.com/microsoft/vscode/tree/ebfd846096ecc3e7752b8af6a3197952281769a0) (September 30, 2026)
- License: MIT; see [LICENSE.txt](LICENSE.txt)

The source snapshot is imported as one baseline commit after this repository's original commit. Upstream source history is available in the Microsoft repository.

## Build and run

Follow the current [Code - OSS build guide](https://github.com/microsoft/vscode/wiki/How-to-Contribute#build-and-run). The repository pins its Node.js version in [`.nvmrc`](.nvmrc). A native compiler toolchain and Python are also required for native dependencies.

On macOS or Linux:

```sh
nvm use                 # or: fnm use
npm install
npm run watch           # wait for "Finished compilation"
./scripts/code.sh
```

On Windows, run `npm install`, then `npm run watch`, and launch with `scripts\code.bat`.

Git LFS is needed to materialize the upstream Copilot simulation cache fixtures. They are not required for the editor's normal development build. To fetch those test assets, install Git LFS and configure the Microsoft repository as an `upstream` remote before running `git lfs fetch upstream main`.

## Development

The Code - OSS repository has detailed [contribution and debugging instructions](https://github.com/microsoft/vscode/wiki/How-to-Contribute), including platform prerequisites, tests, and packaging tasks. When syncing upstream, review incoming changes before merging them into this project.
