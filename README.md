# Wait-For

A rust utility to wait that a program exits with 0.

You need to wait for something to start up and don't know when it finishes?
You want to chain some other commands after it? You want to run a bunch of commands and drink a coffee?
Than this is a tool for you.

I initially wrote it to start docker and run some processes after it, but you can do way more with it,
like waiting for a specific URL to become available after booting up a server in the background or anything else.

- `wait-for docker ps && npm run <script> && npm run <other-script>`
- `wait-for 'curl --fail <non-existing-url>' && ./script.sh`

# Usage

```
wait-for 0.1.0
Max Strübing <mxstrbng@gmail.com>
Waits until the exit code of a program is zero

USAGE:
    wait-for [FLAGS] [OPTIONS] <COMMAND>...

FLAGS:
        --debug       Outputs debug information
    -h, --help        Prints help information
    -n, --no-retry    Don't try to rerun the command in case it fails with non-zero exit code
    -V, --version     Prints version information
        --verbose     Outputs verbose information

OPTIONS:
    -i, --interval <interval>    in which interval the command should be retried in milliseconds [default: 1000]

ARGS:
    <COMMAND>...    Which command should be waited for
```

# Installation

# Crates.io

`cargo install wait-for`

# Raw

Clone the repo and run `cargo build --release` and you should find the binary as `./target/release/wait-for`.

# Contribution

- Fork this project
- Create a branch
- Provide a pull request

The CI will lint your commit message with [commitlint](https://commitlint.js.org/#/).
