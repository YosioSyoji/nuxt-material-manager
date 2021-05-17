<template>
  <v-container fluid>
    <v-toolbar dense height="60" color="#CEF">
      <v-btn-toggle
        v-model="toggleCategory"
        mandatory
        color="red"
        rounded
        dense
      >
        <v-btn
          v-for="n in categorysize"
          :key="n"
          :value="n"
          x-largei
          height="60"
          elevation="5"
          class="headline"
        >
          {{ getCategoryName(n) }}
        </v-btn>
      </v-btn-toggle>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    categorysize: 2,
    strPre: '前へ',
    catgoryInfos: [
      { id: 1, name: 'items1', disp: [1, 2, 3, 4, 5, 35] },
      { id: 2, name: 'items2', disp: [1, 2, 3, 4, 5, 35] },
    ],
  }),
  methods: {
    getCategoryName(i) {
      try {
        const x = Number(i) - 1
        const name = this.catgoryInfos[Number(x)].name
        return name
      } catch (e) {
        return e
      }
    },
  },
}
</script>
