# vue-embed-gist-nojquery
Vue component to embed Github Gists using jsonp, instead of jquery.  Inspired by and forked from Blair Vanderhoof's [gist-embed](https://github.com/sudhanshu-15/vue-embed-gist).


## Install

```bash
yarn add vue-embed-gist-nojquery
```
or
```bash
npm install --save vue-embed-gist-nojquery
```

<!-- CDN: [UNPKG](https://unpkg.com/vue-embed-gist-nojquery) | [jsDelivr](https://unpkg.com/vue-embed-gist-nojquery) (available as `window.VueEmbedGist`) -->

## Usage

```vue
<template>
  <vue-embed-gist 
      gist-id="your gist id" 
      file="your file name"/>
</template>

<script>
import VueEmbedGist from 'vue-embed-gist-nojquery'

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

MIT &copy;
