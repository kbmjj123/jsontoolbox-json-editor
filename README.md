# @jsontoolbox/json-editor

A privacy-first, browser-based JSON editor and viewer for Vue 3.

- Format, validate, and inspect JSON
- Tree view and search
- Local processing, no data sent to servers

## Live Demo

[https://jsontoolbox.cc](https://jsontoolbox.cc)

## Installation

```bash
npm install @jsontoolbox/json-editor
```

## Usage

```vue
<script setup lang="ts">
import { JsonEditor } from '@jsontoolbox/json-editor'

const json = ref('{"hello":"world"}')
</script>

<template>
  <JsonEditor
    v-model="json"
    mode="editor"
    theme="auto"
    :show-toolbar="true"
  />
</template>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `modelValue` | `string \| object` | `''` | JSON content (supports v-model) |
| `mode` | `'viewer' \| 'editor'` | `'editor'` | Viewer or editor mode |
| `theme` | `'auto' \| 'light' \| 'dark'` | `'auto'` | Color theme |
| `readonly` | `boolean` | `false` | Disable editing |
| `showToolbar` | `boolean` | `true` | Show toolbar |

## Events

| Event | Payload | Description |
|-------|---------|-------------|
| `update:modelValue` | `string` | Emitted when JSON content changes |
| `error` | `{ message, line, column }` | Emitted on parse error |

## License

MIT

---

**Built by** [jsontoolbox.cc](https://jsontoolbox.cc)
