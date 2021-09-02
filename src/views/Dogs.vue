<template>
  <div>
    <h1>Dogs for Adoption</h1>
    <b-table striped hover :items="dogs">
        <template #cell(name)="data">
            <router-link :to="`/pets/dogs/${data.index}`">
                {{ data.value }}
            </router-link>
        </template>
    </b-table>
  </div>
</template>

<script>

import { mapState } from 'vuex'

export default {
  data () {
    return {}
  },
  computed: {
      // Using ... (spread operator) includes all props of mapState.
      // mapState itself returns an object, and we want to combine it
      // with the cats/dogs object which is what the ... does
      ...mapState([
          'dogs'
      ])
  }
}
</script>
