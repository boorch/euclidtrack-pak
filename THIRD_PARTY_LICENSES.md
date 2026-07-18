# Third-Party Licenses and Acknowledgments

EUCLIDTRACK is built upon the work of many talented developers and open-source projects. This document acknowledges their contributions.

---

## Mutable Instruments Plaits

EUCLIDTRACK's ENGINE view is powered by DSP algorithms derived from **Plaits**, a macro oscillator Eurorack module originally designed and developed by **Émilie Gillet** of [Mutable Instruments](https://mutable-instruments.net/).

Plaits is a versatile synthesis voice featuring 24 different synthesis engines, released in 2018. The original firmware and hardware design files were generously published under permissive open-source licenses, enabling the community to learn from, build upon, and create derivatives of this groundbreaking work.

- **Original Repository:** https://github.com/pichenettes/eurorack
- **Module Documentation:** https://mutable-instruments.net/modules/plaits/

## mi-plaits-dsp-rs

The Plaits engines reach EUCLIDTRACK through **mi-plaits-dsp-rs**, a native Rust port of the Plaits DSP code, created by **Oliver Rockstedt**.

- **Repository:** https://github.com/sourcebox/mi-plaits-dsp-rs
- **Author:** Oliver Rockstedt <info@sourcebox.de>
- **Based on:** Plaits firmware release 1.2

### MIT License (Plaits / mi-plaits-dsp-rs)

```
MIT License

Copyright (c) 2021 Oliver Rockstedt <info@sourcebox.de>

Based on original code by:
Copyright (c) 2016 Emilie Gillet <emilie.o.gillet@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Special thanks to **Émilie Gillet** for creating Mutable Instruments and open-sourcing the module designs, and to **Oliver Rockstedt** for the meticulous Rust port that made integrating these algorithms into this project possible.

---

## vaixterm

On the TrimUI Brick, EUCLIDTRACK's interface runs inside a modified build of **vaixterm**, a lightweight SDL terminal emulator by **Stanley00**, published under the MIT License.

- **Upstream Repository:** https://github.com/Stanley00/vaixterm
- **License:** MIT, Copyright (c) 2025 Stanley00

EUCLIDTRACK's build extends vaixterm with a gamepad-to-keyboard input layer and boot-time glyph prewarming; the terminal core is Stanley00's work.

---

## gamepad_config

The pak includes **gamepad_config**, a small standalone diagnostic tool for probing and mapping gamepads on unsupported TrimUI variants (`probe_gamepad.sh`). It is derived from **sdl-jstest** (Copyright (C) 2014 Ingo Ruhnke) via the gamepad_config fork bundled with the 1M8ARK distribution, and is licensed under the **GNU General Public License v2 or later**.

It is a separate program aggregated in the pak; it shares no code with EUCLIDTRACK itself. In compliance with the GPL, its complete source (`gamepad_config.c`) and license text (`gamepad_config.LICENSE`) ship inside the pak alongside its binary.

- **sdl-jstest:** https://github.com/Grumbel/sdl-jstest
- **Full GPL v2 text:** https://www.gnu.org/licenses/old-licenses/gpl-2.0.html

---

## Rust Crate Dependencies

EUCLIDTRACK is written in Rust and builds on 168 open-source crates, all published under permissive licenses (MIT, Apache-2.0, BSD, ISC, Zlib, Unlicense, or combinations thereof). Each crate's specific license can be found in its published metadata on [crates.io](https://crates.io).

Key direct dependencies include: `ratatui` (terminal UI), `crossterm` (terminal backend), `cpal` (audio I/O), `gilrs` (desktop gamepad support), `crossbeam-channel`, `serde`, `toml`, `anyhow`, `ansi-to-tui`, `mimalloc`, and `libc`.

The full dependency list:

`aho-corasick`, `allocator-api2`, `alsa`, `alsa-sys`, `ansi-to-tui`, `anyhow`, `autocfg`, `bindgen`, `bitflags`, `bumpalo`, `bytes`, `cassowary`, `castaway`, `cc`, `cesu8`, `cexpr`, `cfg-if`, `cfg_aliases`, `clang-sys`, `combine`, `compact_str`, `core-foundation-sys`, `coreaudio-rs`, `coreaudio-sys`, `cpal`, `crossbeam-channel`, `crossbeam-utils`, `crossterm`, `crossterm_winapi`, `darling`, `darling_core`, `darling_macro`, `dasp_sample`, `either`, `equivalent`, `errno`, `find-msvc-tools`, `fnv`, `foldhash`, `futures-core`, `futures-task`, `futures-util`, `getrandom`, `gilrs`, `gilrs-core`, `glob`, `hashbrown`, `heck`, `ident_case`, `indexmap`, `indoc`, `inotify`, `inotify-sys`, `instability`, `itertools`, `itoa`, `jni`, `jni-sys`, `jni-sys-macros`, `jobserver`, `js-sys`, `libc`, `libloading`, `libm`, `libmimalloc-sys`, `libudev-sys`, `linux-raw-sys`, `lock_api`, `log`, `lru`, `mach2`, `memchr`, `mimalloc`, `minimal-lexical`, `mio`, `ndk`, `ndk-context`, `ndk-sys`, `nix`, `nom`, `num-derive`, `num-traits`, `num_enum`, `num_enum_derive`, `objc2-core-foundation`, `objc2-io-kit`, `oboe`, `oboe-sys`, `once_cell`, `parking_lot`, `parking_lot_core`, `paste`, `pin-project-lite`, `pkg-config`, `proc-macro-crate`, `proc-macro2`, `quote`, `r-efi`, `ratatui`, `redox_syscall`, `regex`, `regex-automata`, `regex-syntax`, `rustc-hash`, `rustix`, `rustversion`, `ryu`, `same-file`, `scopeguard`, `serde`, `serde_core`, `serde_derive`, `serde_spanned`, `shlex`, `signal-hook`, `signal-hook-mio`, `signal-hook-registry`, `simdutf8`, `slab`, `smallvec`, `spin`, `static_assertions`, `strsim`, `strum`, `strum_macros`, `syn`, `thiserror`, `thiserror-impl`, `toml`, `toml_datetime`, `toml_edit`, `toml_parser`, `toml_write`, `unicode-ident`, `unicode-segmentation`, `unicode-truncate`, `unicode-width`, `uuid`, `vec_map`, `walkdir`, `wasi`, `wasip2`, `wasm-bindgen`, `wasm-bindgen-futures`, `wasm-bindgen-macro`, `wasm-bindgen-macro-support`, `wasm-bindgen-shared`, `web-sys`, `winapi`, `winapi-i686-pc-windows-gnu`, `winapi-util`, `winapi-x86_64-pc-windows-gnu`, `windows`, `windows-core`, `windows-link`, `windows-result`, `windows-sys`, `windows-targets`, `windows_aarch64_gnullvm`, `windows_aarch64_msvc`, `windows_i686_gnu`, `windows_i686_gnullvm`, `windows_i686_msvc`, `windows_x86_64_gnu`, `windows_x86_64_gnullvm`, `windows_x86_64_msvc`, `winnow`, `wit-bindgen`

---

## MesloLGS Nerd Font Mono

The pak ships **MesloLGS Nerd Font Mono** for the terminal display.

- **Meslo LG** (the base typeface) is licensed under the **Apache License 2.0**.
- The **Nerd Fonts** patching project, which adds the icon glyphs, is licensed under the **MIT License**: https://github.com/ryanoasis/nerd-fonts
- The embedded icon glyphs used throughout EUCLIDTRACK's interface come from **Material Design Icons** by Pictogrammers, licensed under the **Apache License 2.0**: https://pictogrammers.com/library/mdi/

---

## SDL2

vaixterm links against **SDL2** (zlib license). SDL2 is not redistributed in the pak; the build uses the TrimUI Brick firmware's own SDL2 library, which is the bridge to the device's GPU stack.

- **SDL:** https://www.libsdl.org/
