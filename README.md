# primevue-input-bug

Minimal repro for a bug in PrimeVue: https://lenni009.github.io/primevue-input-bug

This bug is very weird. Commenting out a div that only holds some text fixes the bug. Keeping the div in the code without comment brings the bug back.

Since comments are removed during the build step, this does not fix the bug in production.

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```
