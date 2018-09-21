<template>
  <div>
    <h1>{{totalcomut}}</h1>
    <button @click="addStoreCount">Add</button>
  </div>  
</template>

<script>
  import {mapState, mapMutations} from 'vuex';
  export default {
    data(){
      return{
        localCount: 10,
      };
    },
    computed:{
      // count(){
      //   return this.$store.state.count;
      // },
      ...mapState({
        totalcomut(state){
          return this.localCount + state.count;
        },
      }),
    },
    methods:{
      // addcount(){
      //   // this.$store.commit('addCount');
      // },
      ...mapMutations(['addStoreCount']),
    },
  }
</script>


<style>
</style>