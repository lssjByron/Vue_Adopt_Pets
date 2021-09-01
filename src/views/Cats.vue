<template>
  <div>
    <h1>Cats for Adoption</h1>
    <b-table striped hover :items="cats" />
  </div>
</template>

<script>
// @ is a shortcut that vue cli sets up for you, its a reference to the 'src' directory
// so that you don't have to do ../../ and so on to get back to the 'src' directory
import cats from '@/data/cats'

export default {
  data () {
    return {
      // cats is equivlant to cats: cats (where the first 'cats' is the variable
      // we're declaring and the second cats value is imported cats array)
      cats
    }
  }
}
</script>
