[![Cargo build](https://github.com/pepa65/eqr/actions/workflows/rust.yml/badge.svg)](https://github.com/pepa65/eqr/actions/workflows/rust.yml)

# eqr 1.1.0
**Encode text into svg/png/jpg/terminal-format QR codes**

## Install standalone single-binary
```
wget https://github.com/pepa65/eqr/releases/download/v1.0.1/qr
sudo mv qr /usr/local/bin
sudo chown root:root /usr/local/bin/qr
sudo chmod +x /usr/local/bin/qr
```

## Install with cargo
If not installed yet, install a **Rust toolchain**, see https://www.rust-lang.org/tools/install

### Direct from crates.io
`cargo install eqr`

### Direct from repo
`cargo install --git https://github.com/pepa65/eqr`

### Static build (avoiding GLIBC incompatibilities)
```
git clone https://github.com/pepa65/eqr
cd eqr
rustup target add x86_64-unknown-linux-musl
cargo rel  # Alias in .cargo/config.toml
```

The binary will be at `target/x86_64-unknown-linux-musl/release/qr`

## Usage
```
eqr 1.1.0
Marco Radocchia <marco.radocchia@outlook.com>, github.com/pepa65
Encode text into svg/png/jpg/terminal-format QR codes

USAGE:
    qr [OPTIONS] [STRING]

ARGS:
    <STRING>    String to encode

OPTIONS:
    -b, --bg <BG>
            Background RGB color (hex code) [default: fff]

    -B, --border <BORDER>
            Border size (expressed in unit blocks) [default: 1]

    -f, --fg <FG>
            Foreground RGB color (hex code) [default: 000]

    -h, --help
            Print help information

    -L, --error-correction-level <ERROR_CORRECTION_LEVEL>
            QR error correction level [default: medium] [possible values: low, medium, quartile,
            high]

    -o, --output <OUTPUT>
            Output file (supported file extensions: jpg, png, svg); omit to print QR code to console

    -s, --scale <SCALE>
            Scale factor (1..255) [default: 16]

    -V, --version
            Print version information
```

## Changelog
Complete [CHANGELOG](CHANGELOG.md).

## License
[GPLv3](LICENSE)
