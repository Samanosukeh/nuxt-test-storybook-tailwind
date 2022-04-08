<template>
  <div class="p-24">
    <h1 class="text-center mx-24 bg-blue">Teste</h1>
    <nuxt-logo></nuxt-logo>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import NuxtLogo from '~/components/NuxtLogo.vue'

interface UserInterface {
  name: string
  age: number
}

export default Vue.extend({
  name: 'NuxtTutorial',
  components: { NuxtLogo },

  data() {
    return {
      message: 'Welcome to Your Vue.js App',
      userTest: [] as UserInterface[],
    }
  },

  mounted() {
    this.setUser()
    // console.log(this.getAllUser())
    // printando um único usuário
    // console.log(this.getOneUser(0))
  },

  methods: {
    setUser() {
      this.userTest = [
        { name: 'teste', age: 15 },
        { name: 'teste2', age: 20 },
      ]
    },
    getAllUser() {
      return this.userTest
    },
    getOneUser(idx: number): string {
      return `User: ${this.userTest[idx].name}`
    },
  },
})
</script>
