<template>
    <div>
        {{ pet().name }}
    </div>
</template>

<script>

// mapstate imports all data/store files
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
          'cats',
          'dogs'
      ])
  },
  methods: {
      pet () {
          const animal = this[this.$route.params.species][this.$route.params.id]
          return animal
      }
  }
}
</script>
