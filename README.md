[![Build status](https://badge.buildkite.com/c76805e51e194fb0cdf4bf537306e3b6270cb1ebc4db48f21c.svg?branch=master)](https://buildkite.com/monadic/radicle-link)

# Radicle Link 🌱

This is the working repo for the second iteration of the [Radicle](https://radicle.xyz/)
code collaboration protocol and stack.

**🚨 WORK IN PROGRESS 🚨**

_In fact, there is nothing substantial to see here yet_

Join our [#radicle](https://webchat.freenode.net/?channels=radicle) IRC channel
for development updates.

## Build

Besides a Rust build environment (best obtained using [rustup](https://rustup.rs)),
you may need to install the following packages on a Debian system:

* `file`
* `gcc`
* `git`
* `libc6-dev`
* `liblzma-dev`
* `libssl-dev`
* `make` (GNU make)
* `pkg-config`
* `zlib1g-dev`

For an up-to-date specification of the build and development toolchain, see the
[Dockerfile used for CI](./.buildkite/docker/rust/Dockerfile).

To compile, run `cargo build`.

### Windows

This [project uses libpnet](https://github.com/libpnet/libpnet#windows), which requires setting up
winpcap dev tools to link to packet.

If it fails to build with a `LINK : fatal error LNK1181 ...Packet.lib...`, then remember to set the env
var to point to the appropriate folder which cointains Packet.lib from winpact dev tools.

```powershell
$env:LIB="C:\Users\myuser\Downloads\WpdPack_4_1_2\WpdPack\Lib\x64"
cargo build
```

## License

Unless otherwise noted, all source code in this repository is licensed under the
[GPLv3](https://www.gnu.org/licenses/gpl-3.0.txt).
