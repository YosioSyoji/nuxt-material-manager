<template>
  <v-card outlined elevation="9">
    <v-img :src="getimg()" :max-width="getwide()" :height="getheight()"></v-img>
    <v-card-title class="display-1">
      {{ name }}
    </v-card-title>
    <v-card-sub-title>
      {{ msg }}
    </v-card-sub-title>
  </v-card>
</template>
<script>
export default {
  props: {
    id: {
      type: Number,
      default: 0,
    },
    name: {
      type: String,
      default: '',
    },
    msg: {
      type: String,
      default: '',
    },
    setwide: {
      type: Number,
      default: 10,
    },
    setheight: {
      type: Number,
      default: 10,
    },
    setFontSize: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    getimg() {
      return require(`@/static/${this.id}.jpg`)
    },
  },
}
</script>
