<template>
    <div class="relative w-9/12 m-auto bg-gray-100 rounded-lg pr-0 pt-8 pl-14 pb-20 shadow">
        <div class="underline text-5xl p-8 pl-0 mb-4">今日のお菓子</div>
        <div class="flex flex-wrap">
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
            <EvaluetionSnack></EvaluetionSnack>
        </div>
        <div class="float-right text-5xl underline mr-20 mb-3">今日の当番：犬さん</div>
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
/*.snack-board {
    background-color: #ffd78c;
    box-shadow: 4px 4px 4px gray;
    /*border: ;
    border-color: rgb(165, 149, 149);
    border-radius: 10px;
    text-align: center;
    margin: 10px;
}
*/


</style>