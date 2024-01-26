<template>
  <div>
    <ul>
      <li v-for="child in children" :key="child.name">
        Name: {{ child.name }}
      </li>
    </ul>
  </div>
</template>

<script>
  import {defineComponent} from "vue";

  export default defineComponent({
    name: 'Children',
    props: {
      children: {
        required: true,
        type: Array
      }
    }
  })
</script>