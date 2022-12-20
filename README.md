# syntact

Render `stdin` input with [`syntect`](https://github.com/trishume/syntect) as formatted HTML to `stdout`.

## Building

Instructions for building a Rust XCFramework from https://betterprogramming.pub/from-rust-to-swift-df9bde59b7cd [automated](Makefile).

```sh
rustup default stable
rustup update
rustup target add aarch64-apple-ios
rustup target add aarch64-apple-darwin
rustup target add x86_64-apple-darwin

make clean
make

codesign -d --verbose=2 target/aarch64-apple-ios/release/libsyntact.a # verify signatures
```

## Sources
- https://www.gnu.org/software/make/manual/html_node/Automatic-Variables.html
- https://stackoverflow.com/questions/60782402/calling-rust-from-swift, doesn't work
- https://snacky.blog/en/string-ffi-rust.html does
- https://gregoryszorc.com/docs/apple-codesign/main/ should ease code signing
- https://medium.com/visly/rust-on-ios-39f799b3c1dd
- https://nadim.computer/posts/2022-02-11-maccatalyst.html
