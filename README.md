# vue-embed-gist

# This was forked from https://github.com/sudhanshu-15/vue-embed-gist

# I literally just wanted to remove jquery.

Vue component to embed Github Gists, inspired by Blair Vanderhoof's gist-embed. (https://github.com/blairvanderhoof/gist-embed)

## Install

```bash
yarn add vue-embed-gist
```
or
```bash
npm install --save vue-embed-gist
```

<!-- CDN: [UNPKG](https://unpkg.com/vue-embed-gist/) | [jsDelivr](https://cdn.jsdelivr.net/npm/vue-embed-gist/) (available as `window.VueEmbedGist`) -->

## Usage

```vue
<template>
  <vue-embed-gist 
      gist-id="your gist id" 
      file="your file name"/>
</template>

<script>
import VueEmbedGist from 'vue-embed-gist'

export default {
  components: {
    VueEmbedGist
  }
}
</script>
```

### Props

#### gist-Id
**Type:** `String`
**Required:** `true`

:octocat: Github gist Id

#### file
**Type:** `String`
**Required:** `false` 

File name in the gist

## License

MIT &copy; [Sudhanshu Siddh](www.ssiddh.me)
