<template>
    <div class="shadow">
        <header class="border-b-2 border-gray-400 py-2 text-black font-bold flex justify-between">
          <h1 class="title pl-10">GiveMeSnack</h1>
          <nav class="nav pr-10" v-if = this.work.situation >勤務中</nav>
          <nav class="nav pr-10" v-else>休憩中</nav>
        </header>
    </div>
</template>

<script>
export default {
  setup() {
  },
  data(){
    return {
      work: {
        now_time_str:'',
        rest_time:50,
        now_time:0,
        situation:true,
      },
      show: false,
    }
  },
  methods: {
    async get_situation(){
      var d = new Date();
      var mm = ('0' + d.getMinutes()).slice(-2);
      this.work.now_time_str =mm;
      this.work.now_time = Number(this.work.now_time_str);
      if(this.work.now_time >= this.work.rest_time){
        this.work.situation = false;
      }
    }
  },

  async mounted(){
    await this.get_situation();
  },
}
</script>

<style>
.header {
  width: 100%;
  background-color: white;
}
 
.menu-item {
  list-style: none;
  display: inline-block;
  padding: 10px;
}
</style>