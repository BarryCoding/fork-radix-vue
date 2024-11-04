---
title: My Study Plan
description: A Plan to study Radix Vue.
---

# My Study Plan

<Description>
A Plan to study Radix Vue.
</Description>

## Understand Package

- root package
  - [ ] workspaces
    - plugin
    - radix-vue
  - [ ] script
    -
    -
    -

```bash
story:dev
# find .histoire repo, run its story:dev script(histoire dev), and open
pnpm --filter histoire story:dev --open

```

```bash
build
# remove dist first
# find radix-vue repo, and run its build script
# find plugin repo, and run its build script (which rely on radix dist)
rimraf packages/radix-vue/dist  && pnpm run --filter radix-vue build && pnpm run --filter plugins build

build-only
# remove dist first
# -r means --recursive all packages, and run their build-only script
rimraf packages/radix-vue/dist  && pnpm run -r build-only
```

```bash
# find docs repo, and run its install script(install deps)
pnpm --filter docs install

# find docs repo, and run its docs:dev script(vitepress dev)
pnpm --filter docs docs:dev

# find docs repo, and run its docs:build script(vitepress build)
pnpm --filter docs docs:build

# find docs repo, and run its docs:gen script(tsx scripts/autogen.ts)
pnpm --filter docs docs:gen

#
pnpm --filter docs docs:contributors

# docs scripts
```
