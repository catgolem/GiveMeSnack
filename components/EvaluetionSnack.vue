<template>
    <div class="grow shrink mt-2 mb-6" style="flex-basis: 600px;">
        <div class="flex mb-4">
            <div class="flex-1 text-2xl bg-white text-center py-2 rounded-lg">snackname</div>
            <div class="flex-1 text-2xl py-2 pl-2">平均</div>
        </div>
        <form class="w-1/3 m-2" style="margin-left: 19%">
            <input placeholder="点数" class="text-center rounded border border-black py-1" style="width: 45%;" type="number" v-model="textInput" @keydown.69.prevent>
            <button @click="clearText" class="rounded bg-white bg-gray-300 py-1 text-white" style="width: 45%;">
                決定
            </button>
        </form>
        

    </div>
</template>

<script>
export default {
  setup() {
  },
  data(){
    return {
  	    textInput: null,
    }
  },
    methods: {
        clearText () {
            console.log(this.textInput);
            this.textInput=null;
        },
    },
  computed: {

  }
}
</script>  
<style>


</style>