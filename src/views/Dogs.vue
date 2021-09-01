<template>
  <div>
    <h1>Dogs for Adoption</h1>
    <b-table striped hover :items="dogs" />
  </div>
</template>

<script>
// @ is a shortcut that vue cli sets up for you, its a reference to the 'src' directory
// so that you don't have to do ../../ and so on to get back to the 'src' directory
import dogs from '@/data/dogs'

export default {
  data () {
    return {
      // dogs is equivlant to dogs: dogs (where the first 'dogs' is the variable
      // we're declaring and the second dogs value is imported dogs array)
      dogs
    }
  }
}
</script>
