<template>
  <v-layout wrap>
    <itemMenu></itemMenu>
  </v-layout>
</template>
<script>
import itemMenu from '~/components/itemMenu.vue'
export default {
  components: {
    itemMenu,
  },
  data() {
    return {
      test: 'test',
    }
  },
}
</script>
