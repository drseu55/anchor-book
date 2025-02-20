# Installation

## Rust

Go [here](https://www.rust-lang.org/tools/install) to install Rust.

## Solana

Go [here](https://docs.solana.com/cli/install-solana-cli-tools) to install Solana and then run `solana-keygen new` to create a keypair at the default location. Anchor uses this keypair to run your program tests.

## Yarn

Go [here](https://yarnpkg.com/getting-started/install) to install Yarn.

## Anchor

### Installing using Anchor version manager (avm) (recommended)

Anchor version manager is a tool for using multiple versions of the anchor-cli. It will require the same dependencies as building from source. It is recommended you uninstall the NPM package if you have it installed.

Install `avm` using Cargo. Note this will replace your `anchor` binary if you had one installed.

```
cargo install --git https://github.com/project-serum/anchor avm --locked --force
```

Install the latest version of the CLI using `avm`. You can also use the command to upgrade to the latest release in the future.

```
avm use latest
```

Verify the installation.

```
anchor --version
```

### Install using pre-build binary on x86_64 Linux

Anchor binaries are available via an NPM package [`@project-serum/anchor-cli`](https://www.npmjs.com/package/@project-serum/anchor-cli). Only `x86_64` Linux is supported currently, you must build from source for other OS'.

### Build from source for other operating systems without avm

We can also use Cargo to install the CLI directly. Make sure that the `--tag` argument uses the version you want (the version here is just an example).

```
cargo install --git https://github.com/project-serum/anchor --tag v0.22.0 anchor-cli --locked
```

On Linux systems you may need to install additional dependencies if cargo install fails. On Ubuntu,

```
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install -y pkg-config build-essential libudev-dev
```

Now verify the CLI is installed properly.

```
anchor --version
```
