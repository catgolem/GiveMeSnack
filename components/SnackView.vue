<template>
    <div class="relative w-9/12 m-auto rounded-lg pr-0 pt-6 pl-14 pb-28 shadow-xl" style="background: rgb(252 222 108)">
        <div class="underbar-choco text-4xl p-8 pl-0 mb-4 text-shadow-sm"><img class="inline" src="../assets/photo/cookie.png">今日のカントリーマアム</div>
        <div class="flex flex-wrap">
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
        </div>
        <div class="float-right text-4xl underbar-pink mr-20 mb-30 text-shadow-sm">今日の当番：犬さん</div>
    </div>
</template>
<script>
import EvaluetionSnack from '../components/EvaluetionSnack.vue';
export default {
  components: { 
    EvaluetionSnack
  }
}

</script>
<style>
.underbar-choco {
    position: relative
}
.underbar-choco::after {
    content: '';
    position: absolute;
    top: 80%;
    left: 0;
    width: 90%;
    height: 8px;
    border-radius: 4px;
    background: linear-gradient(to right, #240905 80%, #f2ba48 80%);
    box-shadow: 0 3px 8px #0008, 0 -3px 2px #0005 inset, 0 1px 2px #0001 inset;
}

.underbar-pink {
    position: relative
}
.underbar-pink::after {
    content: '';
    position: absolute;
    top: 120%;
    left: -5%;
    width: 110%;
    height: 8px;
    border-radius: 4px;
    background: linear-gradient(to left, #d98280 80%, #f2cc91 80%);
    box-shadow: 0 3px 8px #0008, 0 -3px 2px #0005 inset, 0 1px 2px #0001 inset;
}

</style>