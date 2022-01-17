<template>
    <div class="background-rd font-new">
        <Header/>
        <nuxt-link to="/" class="admin-link ml-8">
            <span class="edit-icon" style="display:inline-block; width:2rem; height:2rem;">
                <img src="../assets/photo/round_keyboard_return_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem;">
            </span>
            <span class="admin-link-text align-top pr-2 font-black">戻る</span>
        </nuxt-link>
        <div class="submit flex justify-center">
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
                    <div class="added-snacks-content font-black">
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
            <div class="left background-white rounded-lg roleboard shadow-md text-xl ml-8 font-black">
                <div class="flex titlesize">
                    <div class="border-b-2 border-gray-400 inline">当番表</div>
                    <div class="ml-5">今週の当番は</div>
                </div>
                <div class="m-4">
                    <div class ="boardfont">
                        <div class="ml-10 font-black">
                            <div class="textbottom">１．イヌさん</div>
                            <div class="textbottom">２．ハトさん</div>
                            <div class="textbottom">３．ネコさん</div>
                            <div class="textbottom">４．ドジョウさん</div>
                            <div class="textbottom">５．ヤギさん</div>
                            <div class="textbottom">６．フライゴンさん</div>
                        </div>
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

@media screen and ( max-width:667px){
    .boardfont{
        font-size: 10px !important;
        transition: 1s;
    }
    .textbottom{
        margin-bottom: 0em;
        transition: 1s;
    }
    .titlesize{
        font-size: 10px !important;
        transition: 1s;
    }
    .roleboard{
        padding: 50px;
    }
}
@media screen and (min-width:667px) {
    .boardfont{
        font-size: 16px !important;
        transition: 1s;
    }
    .textbottom{
        margin-bottom: 2em;
        transition: 1s;
    }
    .titlesize{
        font-size: 16px !important;
        transition: 1s;
    }
    .roleboard{
        padding: 150px;
    }
}

.right{
    width: 50%;
}
.left{
    width: calc(50%-612px);
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
.background-rd {
    background: repeating-linear-gradient(-45deg, #d0546a22, #d0546a22 40px, #d0546a 40px, #d0546a 80px);
    min-height: 100vh;
}
.background-white{
  border-radius: 20px;
  background: #f3f3f3;
  box-sizing: border-box;
  border: solid 24px #e0e0e0;
  border-top: solid 24px #ccc;
  border-bottom: solid 24px #fff;
} 
</style>
