<template>
  <div>
    <app-gist-core :gist-div="gistData" />
  </div>
</template>

<script>
var gistUrl = "https://gist.github.com/";
var data = {};

import VueGistCore from "./VueGistCore.vue";
import jsonp from 'jsonp';

export default {
  components: {
    appGistCore: VueGistCore
  },
  props: {
    gistId: {
      type: String,
      required: true
    },
    file: {
      type: String,
      required: false,
      default: ""
    }
  },
  data() {
    return {
      gistData: "loading..."
    };
  },
  created() {
    this.getGistData(this.gistId);
  },
  methods: {
    getGistData(gistId) {
      var self = this;
      if (this.file.length > 0) {
        data.file = this.file;
      }

    jsonp(gistUrl + gistId + ".json", data, (err, response) => {
    if (err) {
        console.error(err.message);
    } else {
        self.gistData = response.div;
    }
    });
    }
  }
};
</script>