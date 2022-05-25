# RustDesk Server Program



[**Download**](https://github.com/rustdesk/rustdesk-server/releases)

[**Manual**](https://rustdesk.com/docs/en/self-host/)  

Self-host your own RustDesk server, it is free and open source.

```
cargo build --release

ubuntu 20.04 LTS

# curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
# source $HOME/.cargo/env
# apt install gcc-arm-linux-gnueabihf
# rustup target add armv7-unknown-linux-gnueabihf
# vim ~/.cargo/config

input:
[target.armv7-unknown-linux-gnueabihf]
linker = "arm-linux-gnueabihf-gcc"

# cargo build --release --target=armv7-unknown-linux-gnueabihf
```

Two executables will be generated in target/release.
  - hbbs - RustDesk ID/Rendezvous server
  - hbbr - RustDesk relay server

If you wanna develop your own server, [rustdesk-server-demo](https://github.com/rustdesk/rustdesk-server-demo) might be a better and simpler start for you than this repo.
