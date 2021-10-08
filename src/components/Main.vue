<template>
<div class="grid grid-cols-3 gap-4">
  <div>
  <span class="mr-12">A</span>
    <input
          v-model="a"
          type="number"
          class="inline  rounded sm:text-sm" >

          <br> <br> <br>
           <span class="mr-12">B</span>
    <input
          v-model="b"
          type="number"
          class="inline  rounded sm:text-sm" >

           <br> <br> <br>
           <span  class="mr-5">SUM</span>
    <input
          v-model="sum"
          type="text"
          class="inline  rounded sm:text-sm" >
       
  </div>
  <!-- ... -->
  <div>
 <button
          type="button"
          class="inline-flex items-center mt-40 px-3 py-2 text-sm font-medium leading-4 text-white bg-red-600 border border-transparent rounded-md shadow-sm hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 tabular-nums"
          @click="sumdata" >
       
         Click
        </button>
  </div>
</div>
</template>

<script lang="ts">
import { defineComponent, toRef, ref } from 'vue'
import { globalState } from '../store'

export default defineComponent({
   data: () => ({
    a:'',
      b:'',
      sum:'',
  }),

  methods: {
  sumdata: function () {
    if(this.a==""){
    alert('Input Value in A');
    }
    else if(this.b==""){
    alert('Input Value in B');
    }else{
    let result=parseFloat(this.a)+parseFloat(this.b);
    this.sum=result;
    }
}
  },
})
</script>

<style>
.prose a {
  @apply text-gray-900 underline !important;
}
</style>
