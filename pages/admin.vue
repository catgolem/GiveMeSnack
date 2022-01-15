<template>
  <div>
    <Header/>
    <div class="ml-16" >
        <h1 class="mt-10 font-black text-2xl">今週買ったお菓子</h1>
        <h2 class="h2 mt-6"> 
            <input type="text" autocomplete="on" v-model="snack_name" class="shadow-md rounded-lg h21 pl-2 py-1 w-44" placeholder="入力"/>
            <button class="hover:bg-black shadow-md button ml-3 rounded-lg text-white bg-gray-400 p-1" @click="postSnack()">追加</button>
        </h2>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
export default{
    components: { Header },
    data(){
        return{
            snack_name:'',
            name: 'IndexPage'
        }
    },
    methods: {
        postSnack(){
            console.log(this.snack_name)
            this.snack_name = ''
        },
    },
}

</script>

<style>
.h2{
    font-size: 1em;
}

.h21{
    border-radius: 5px;
    border: solid;
}

</style>