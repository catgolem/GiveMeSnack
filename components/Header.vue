<template>
    <div>
        <header class="text-black">
          <h1 class="title">GiveMeSnack</h1>
          <nav class="nav" v-if = this.work.situation >勤務中</nav>
          <nav class="nav" v-else>休憩中</nav>
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
header {
  display: flex;
  width: 100%;
  height: 100px;
  background-color: white;
  align-items: center;
}
 
.title {
  margin:5%
}

.nav {
  margin:10%;

}
 
.menu-item {
  list-style: none;
  display: inline-block;
  padding: 10px;
}
</style>