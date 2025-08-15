# toolchains_gcc_packages
Bazel toolchains for GNU GCC

## Overview
This repository builds GCC toolchains for use with Bazel build system using crosstool-ng.

## Supported Architectures
- x86_64 (AMD64)
- aarch64 (ARM64)

## Building

### Using Docker (recommended)
```bash
# Build for x86_64 (default)
./docker_build_and_run.sh

# Build for ARM64
./docker_build_and_run.sh arm64

# Build for specific architecture and GCC version
./docker_build_and_run.sh arm64 12
```

### Manual Build
```bash
# Set required environment variables
export GCC=12  # GCC major version
export ARCH=x86_64  # or arm64/aarch64

# Run the build
./build.sh
```

## Output
The build will create a tarball in the `output/` directory:
- For x86_64: `x86_64-unknown-linux-gnu_gcc12.tar.gz`
- For ARM64: `aarch64-unknown-linux-gnu_gcc12.tar.gz`
