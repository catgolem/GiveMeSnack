<template>
  <div>
    <Header/>
    <nuxt-link to="/" class="admin-link ml-8">
        <span class="edit-icon" style="display:inline-block; width:2rem; height:2rem;">
            <img src="../assets/photo/round_keyboard_return_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem;">
        </span>
        <span class="admin-link-text align-top pr-2">戻る</span>
    </nuxt-link>
    <div class="submit">
        <div class="left ml-16" >
            <h1 class="mt-10 font-black text-2xl">今週買ったお菓子</h1>
            <h2 class="h2 mt-6"> 
                <input type="text" autocomplete="on" v-model="snack_name" class="shadow-md rounded-lg h21 pl-2 py-1 w-44" placeholder="入力"/>
                <button class="shadow-md ml-3 rounded-lg text-white bg-gray-400 p-1" @click="postSnack()">追加</button>
            </h2>
            <div class="added-snacks mt-8 ml-2">
                    <div class="added-snacks-title font-black text-lg mb-2">
                        登録済み
                    </div>
                    <div class="added-snacks-content">
                        <div class="added-snacks-container pl-4">
                            <div class="added-snacks-element flex py-2">
                                <div class="added-snacks-snack-name flex-1">
                                    <span id="snack-name" class="snack-name ml-2">キットカット</span>
                                    <img src="../assets/photo/round_done_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                                </div>
                            </div>
                            <div class="added-snacks-element flex py-2">
                                <div class="added-snacks-snack-name flex-1">
                                    <span id="snack-name" class="snack-name ml-2">せんべい</span>
                                    <img src="../assets/photo/round_done_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                                </div>
                            </div>
                            <div class="added-snacks-element flex py-2">
                                <div class="added-snacks-snack-name flex-1">
                                    <span id="snack-name" class="snack-name ml-2">カントリーマアム</span>
                                    <img src="../assets/photo/round_done_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                                </div>
                            </div>
                        </div>
                    </div>
            </div>
        </div>
        <div class="right ml-10 mr-16 mt-12 mb-5 bg-gray-200 p-3 rounded-lg w-80 shadow-md">
            <div>
                <h11 class="border-b-2 border-gray-400">当番表</h11>
                <h12 class="ml-5">今週の当番は</h12>
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
                    <button class="shadow-md bg-white rounded-full text-black mx-auton">編集</button>
                </div>
            </div>
        </div>
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
.submit{
    display: flex;
    flex-wrap: wrap;
}
.button{
    text-align: center;
}
</style>
