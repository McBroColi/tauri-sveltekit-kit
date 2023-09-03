# tauri-sveltekit-kit
This package is not intended for public usage, but there's nothing here to stop you.

## Description

It provides a starter layout for using Tauri and SvelteKit, with several other distinctive settings:
- Tailwind is pre-configured. `font-geek` is available as the font **Gemunu Libre**. `font-sans` is altered to **Signika Negative**. `font-display` is available as the font **Phudu**.
- Two additional Tauri libraries are marked as dependencies. Only one is pre-configured to be used in the setup (the current functionality in one is broken in Windows 11 Update 22H2): [window-vibrancy](https://crates.io/crates/window-vibrancy) (disabled), and [window-shadows](https://crates.io/crates/window-shadows) (enabled). The Tauri configuration is pre-configured to disable the native window decoration, but re-add it with more customizability.
- As such, the native app bar is replaced with a **macOS-style** window control layout.

![picture of app](https://github.com/McBroColi/tauri-sveltekit-kit/assets/4147952/05dd2303-87f0-46f3-aff9-75a8de395969)

## Other Notes
- TypeScript is enabled.
- There's already some pre-existing customization which you probably will not like within the folder system of the project. But maybe you will!
