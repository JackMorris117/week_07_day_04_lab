<template>
  <li v-on:click="handleClick"> {{beer.name}} </li>
</template>

<script>
import { eventBus } from '../main.js'
export default {
    name: 'beers-list-item',
    props: ['beer'],
    methods: {
        handleClick(){
           eventBus.$emit('beer-selected', this.beer);
            
        }
    }
}
</script>

<style scoped>
 list-style-type: none;

</style>