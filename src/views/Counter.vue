<template>
  <h1>Counter View</h1>
  <h2>{{ counter }}</h2>

  <button @click="increase">+1</button>
  <button @click="decrease">-1</button>
  
</template>

<script>
import useCounter from '@/composables/useCounter'

export default {
    name: 'Counter',
    props: {},
    emits: [],
    setup() {

        const { counter, increase, decrease } = useCounter(25)
       

        return {
            counter, increase, decrease
        }
    },
}
</script>

<style>

</style>