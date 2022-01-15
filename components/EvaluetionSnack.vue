<template>
    <div class="grow shrink mt-2 mb-6" style="flex-basis: 600px;">
        <div class="flex mb-4">
            <div class="flex-1 text-2xl shadow bg-white text-center py-2 rounded-lg">snackname</div>
            <div class="flex-1 text-2xl py-2 pl-2 text-shadow-sm">平均</div>
        </div>
        <form class="w-1/3 m-2" style="margin-left: 19%">
            <input placeholder="点数" class="text-center shadow rounded border border-black py-1" style="width: 45%;" type="number" v-model="textInput" @keydown.69.prevent>
            <button @click="clearText" class="rounded bg-choco shadow py-1 text-white" style="width: 45%;">
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

.bg-choco {
    background-color: #573a2e;
}

form input {
    text-align: center;

}
form input::-webkit-inner-spin-button,
form input::-webkit-outer-spin-button {
    -webkit-appearance: none !important;
    margin: 0 !important;
    -moz-appearance: textfield !important;
}

</style>