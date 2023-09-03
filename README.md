# tauri-sveltekit-kit
This package is not intended for public usage, but there's nothing here to stop you.

## Description

It provides a starter layout for using Tauri and SvelteKit, with several other distinctive settings:
- Tailwind is pre-configured. `font-geek` is available as the font **Gemunu Libre**. `font-sans` is altered to **Signika Negative**. `font-display` is available as the font **Phudu**.
- Two additional Tauri libraries are marked as dependencies. Only one is pre-configured to be used in the setup (the current functionality in one is broken in Windows 11 Update 22H2): [window-vibrancy](https://crates.io/crates/window-vibrancy) (disabled), and [window-shadows](https://crates.io/crates/window-shadows) (enabled). The Tauri configuration is pre-configured to disable the native window decoration, but re-add it with more customizability.
- As such, the native app bar is replaced with a **macOS-style** window control layout.
- A full list of packages: `@supabase/supabase-js@2.32.0`,`@sveltejs/adapter-auto@2.1.0`,`@sveltejs/adapter-static@2.0.3`,`@sveltejs/kit@1.22.4`,`@tauri-apps/api@1.4.0`,`@tauri-apps/cli@1.4.0`,`js-tiktoken@1.0.7`,`openai@3.3.0`,`postcss@8.4.27`,`prettier-plugin-svelte@2.10.1`,`prettier@2.8.8`,`supabase@1.83.7`,`svelte-check@3.4.6`,`svelte@4.1.2`,`tailwindcss@3.3.3`,`three@0.156.0`,`tslib@2.6.1`,`typescript@5.1.6`,`vite@4.4.9`.

![picture of app](https://github.com/McBroColi/tauri-sveltekit-kit/assets/4147952/05dd2303-87f0-46f3-aff9-75a8de395969)

## Other Notes
- TypeScript is enabled.
- There's already some pre-existing customization which you probably will not like within the folder system of the project. But maybe you will!
