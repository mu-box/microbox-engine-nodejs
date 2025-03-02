# Node.js

This is a Node.js engine for running node apps with [Microbox](http://microbox.cloud).

## Usage
To use the Node.js engine, specify `nodejs` as your `engine` in your boxfile.yml

```yaml
run.config:
  engine: nodejs
```

## Build Process
When [running your app](https://docs.nanboox.io/cli/run/), this engine compiles code by doing the following:

- `yarn install`

## Configuration Options
This engine exposes configuration options through the [Boxfile](https://docs.microbox.cloud/boxfile/), a yaml config file used to provision and configure your app's infrastructure when using Microbox.

#### Overview of Boxfile Configuration Options
```yaml
run.config:
  engine: nodejs
  engine.config:
    runtime: nodejs-4.4
    dep_manager: yarn
    python_version: python-2.7
```

---

#### runtime
Specifies which Node.js runtime and version to use. The following runtimes are available:

- nodejs-0.8
- nodejs-0.10
- nodejs-0.12
- nodejs-4.8
- nodejs-5.12
- nodejs-6.11
- nodejs-7.10
- nodejs-8.6
- nodejs-8.9

```yaml
run.config:
  engine: nodejs
  engine.config:
    runtime: nodejs-8.6
```

---

#### dep_manager
Specifies whether the engine should use npm or yarn to fetch node modules. Defaults to `yarn`.

```yaml
run.config:
  engine.config:
    dep_manager: yarn
```

#### python_version
Specifies the version of Python to install with the following available values:

- python-2.7
- python-3.4
- python-3.5
- python-3.6 (Default)

```yaml
run.config:
  engine.config:
    python_version: python-2.7
```



---

## Help & Support
This is a generic (non-framework-specific) Node.js engine provided by [Microbox](http://microbox.cloud). If you need help with this engine, you can reach out to us in the [Microbox Discord](https://discord.gg/MCDdHfy). If you are running into an issue with the engine, feel free to [create a new issue on this project](https://github.com/mu-box/microbox-engine-nodejs/issues/new).
