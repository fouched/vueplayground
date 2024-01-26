<template>
  <h1>Me:</h1>
  <p>{{ name }} - {{ age }}</p>
  <button @click="changeName('Zelda')">Change Name</button>
  <br />
  <h2>Children:</h2>
  <Children :children="children"/>
</template>
<script>
import {defineComponent, ref} from "vue"
import Children from "@/components/Children.vue";

export default defineComponent({
  name: 'App',
  components: {Children},
  setup() {
    const name = ref('John')
    const age = ref(30)
    const children = ref([
      { name: 'Mary'},
      { name: 'Jane'},
      { name: 'Tom'},
      { name: 'Dick'},
      { name: 'Harry'},
    ])

    return {name, age, children}
  },
  methods: {
    changeName(name) {
      this.name = name
    }
  }
})

</script>