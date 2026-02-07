# libsignal-bin

Pre-compiled [libsignal](https://github.com/signalapp/libsignal) FFI static libraries for use with [signal-go](https://github.com/gwillem/signal-go).

## Available platforms

| Platform | File |
|----------|------|
| macOS ARM64 | `libsignal_ffi-darwin-arm64.a` |
| Linux x86_64 (musl) | `libsignal_ffi-linux-amd64.a` |

Each release also includes the platform-independent C header `libsignal-ffi.h`.

## Usage

Download from [Releases](https://github.com/gwillem/libsignal-bin/releases):

```bash
VERSION=v0.87.0
curl -fSL https://github.com/gwillem/libsignal-bin/releases/download/${VERSION}/libsignal_ffi-darwin-arm64.a -o libsignal_ffi.a
curl -fSL https://github.com/gwillem/libsignal-bin/releases/download/${VERSION}/libsignal-ffi.h -o libsignal-ffi.h
```

Or use `make deps-download` in signal-go.

## Building

```bash
gh workflow run build.yml -f libsignal_version=v0.87.0
```
