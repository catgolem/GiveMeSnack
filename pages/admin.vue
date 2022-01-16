<template>
    <div>
        <Header/>
        <div class="submit m-16">
            <div class="left p-12 mx-16" >
                <h1 class="mt-10 font-black text-2xl">今週買ったお菓子</h1>
                <h2 class="h2 mt-6"> 
                    <input type="text" autocomplete="on" v-model="snack_name" class="shadow-md rounded-lg h21 pl-2 py-1 w-44" placeholder="入力"/>
                    <button class="shadow-md ml-3 rounded-lg text-white bg-gray-400 p-1" @click="postSnack()">追加</button>
                </h2>
            </div>
            <div class="right bg-gray-200 rounded-lg py-5 px-5 shadow-md text-xl">
                <div class="flex">
                    <div class="border-b-2 border-gray-400 inline">当番表</div>
                    <div class="ml-5">今週の当番は</div>
                </div>
                <div class="m-7">
                        <div class="ml-5">
                        <div class="mb-3">１．イヌさん</div>
                        <div class="mb-3">２．ハトさん</div>
                        <div class="mb-3">３．ネコさん</div>
                        <div class="mb-3">４．ドジョウさん</div>
                        <div class="mb-3">５．ヤギさん</div>
                        <div class="mb-3">６．フライゴンさん</div>
                    </div>
                    <div class="text-center">
                        <button class="shadow-md bg-white rounded-full text-black mx-auto px-5" @click="show=true">編集</button>
                        <FormMember @closeModal="show=false" v-if="show"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Header from '../components/Header.vue'
import FormMember from '../components/FormMember.vue'

export default{
    components: { 
        Header,
        FormMember 
    },
    data(){
        return{
            snack_name:'',
            name: 'IndexPage',
            show: false,
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
.right{
    width: 50%;
}
.left{
    width: calc(100%-612px);
}
.h2{
    font-size: 1em;
}

.h21{
    border-radius: 5px;
    border: solid;
}
.submit{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
}
.button{
    text-align: center;
}
</style>