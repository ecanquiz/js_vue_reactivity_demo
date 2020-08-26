<template lang="pug">
  #app
    img(src="./assets/logo.png")
    h1 Reactividad
    p {{ person }}
    button(@click='addProp') Add Prop
</template>

<script>

export default {
  name: 'app',
  data () {
    return { 
      person: {
        name: 'Ignacio'
      }
    }
  },
  methods: {
    addProp () {
      //this.person.lastName = 'Anaya'
      this.$set(this.person, 'lastName', 'Anaya')
      this.person = Object.assign({}, this.person, { a:1, b:2 })
    }
  }
}
</script>

<style lang="scss">
  
</style>
