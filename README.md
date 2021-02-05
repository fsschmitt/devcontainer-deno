# Devcontainer for Deno

The goal of this repo is to serve as a base dev container for a Deno application

> *The Visual Studio Code Remote - Containers extension lets you use a [Docker container](https://docker.com/) as a full-featured development environment. It allows you to open any folder or repository inside a container and take advantage of Visual Studio Code's full feature set. A `devcontainer.json` file in your project tells VS Code how to access (or create) a development container with a well-defined tool and runtime stack. This container can be used to run an application or to sandbox tools, libraries, or runtimes needed for working with a codebase.*

## Requirements
- Docker Engine installed in our machine, more information here: https://docs.docker.com/get-docker/

## How To

1. Clone this repo into your local machine
```
git clone git@github.com:fsschmitt/devcontainer-deno.git
```

2. Open Visual Studio Code on the repo base folder

3. Run the following command or the `Reopen in Container` popup:

```
>Remote-Containers: Reopen in Container
```

![VSCode dev containers](https://gist.githubusercontent.com/fsschmitt/bcc84df15bd1ec4dca8b6ec171f89d41/raw/vscode-container.png)

4. Then a new window of VSCode will open and the container will be built and initialized. After this you'll be able to run any deno command within the container. (This will only take time on the first run or whenever the container needs to be rebuilt)

## Use it

![deno terminal](https://gist.githubusercontent.com/fsschmitt/bcc84df15bd1ec4dca8b6ec171f89d41/raw/vscode-deno-bash.png)

### Check version
```bash
vscode ➜ /workspaces/devcontainer-deno (main ✗) $ deno --version
deno 1.6.3 (release, x86_64-unknown-linux-gnu)
v8 8.8.294
typescript 4.1.3
```

### Run deno hello world
```bash
vscode ➜ /workspaces/devcontainer-deno (main ✗) $ deno run hello-world.ts 
Check file:///workspaces/devcontainer-deno/hello-world.ts
Hello John
Hello Sarah
Hello Kai
```

## Extend functionalities in your dev container

### VSCode Configuration

Within the file `.devcontainer/devcontainer.json` you are able to extend:
- Settings
```
// Set *default* container specific settings.json values on container create.
"settings": {
    "terminal.integrated.shell.linux": "/bin/bash",
    "deno.enable": true,
    "deno.unstable": true,
    "deno.lint": true
},
```
Check more settings configurations in the [documentation](https://code.visualstudio.com/docs/getstarted/settings).

- Extensions
```
// Add the IDs of extensions you want installed when the container is created.
"extensions": [
    "ms-azuretools.vscode-docker",
    "denoland.vscode-deno",
    "ms-vscode.vscode-typescript-tslint-plugin",
    "esbenp.prettier-vscode"
],
```

Find more extensions in the [VSCode Marketplace](https://marketplace.visualstudio.com/VSCode)


## Questions
More information or questions, feel free to open an issue or reach out:

[Twitter](https://twitter.com/schmittfelipe) | [Github](https://github.com/fsschmitt) | [Website](https://felipeschmitt.com)
