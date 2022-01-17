<template>
    <div class="modal">
        <div class="bg" @click="$emit('closeModal')" />
        <div class="bg-white rounded border-2 border-gray-300 mt-20">
            <button @click="$emit('closeModal')" class="mr-30 locate p-3 rounded bg-glay"> 
                <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24"><path d="M24 20.188l-8.315-8.209 8.2-8.282-3.697-3.697-8.212 8.318-8.31-8.203-3.666 3.666 8.321 8.24-8.206 8.313 3.666 3.666 8.237-8.318 8.285 8.203z"/></svg>
            </button>
            <div class="w-1/2 font-black mt-3 small">当番表の編集</div>
            <div class="ml-8 small">
                <div class="line">
                    <div class="mb-5 ">
                        <h1>追加
                            <input type="text" v-model="user_name" class="rounded-lg border pl-2 py-1" style="width:auto"  placeholder="名前を入力">さん
                        </h1>
                    </div>
                    <div class="mb-5">
                        <h1>削除
                            <input type="text" v-model="user_number" class="rounded-lg border pl-2 py-1" style="width:auto" placeholder="番号を入力">
                        </h1>
                    </div>
                    <div class="mb-5">
                        <h1>変更
                            <input type="text" v-model="input_number" class="rounded-lg border pl-2 py-1" style="width:auto">
                        </h1>
                    </div>
                </div>
                <button class="w-1/4 rounded-lg h21 ml-24 mb-3 w-10 bg-red-500" @click="$emit('closeModal')">確定</button>
            </div>
        </div>
    </div>
</template>

<style>
    .locate{
        position: absolute !important;
        top:4em !important;
        left: 1em !important;
    }
    
    
    @media screen and ( max-width:667px) {
        .small{
            font-size: 6px !important;
            transition:1s;
        }
        .modal{
            position: absolute !important;
            top: 28em !important;
            right:56vw !important;
            width: 240px !important;
            transition:1s;
        }
    }
    @media screen and (min-width:667px) {
        .small{
            font-size: 16px !important;
            transition: 1s;
        }
        .modal{
            position: absolute !important;
            top: 5em !important;
            left: 2em !important;
            width: 300px !important;
            transition: 1s;
        }
    }
    .border{
        border-radius: 5px;
        border: solid;
    }
    .line{
        text-align: left;
    }
    
    .large{
        border-radius: 5px;
        border: solid;
        padding: 2em;
        padding-block-end: 1em;
        width: 44em;
        font-size: 5em;
    }
</style>

<script>
export default {
    function () {
        return {
            width: window.innerWidth,
            height: window.innerHeight
        }
    },
    methods: {
        handleResize: function() {
            this.width = window.innerWidth;
            this.height = window.innerHeight;
            if(this.width<500){
                
            }
        }
    }
}
</script>