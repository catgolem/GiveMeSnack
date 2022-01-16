<template>
    <div class="shadow mb-10 font-text">
        <header class="py-8 font-bold flex justify-between">
          <nuxt-link to="/">
            <h1 class="title text-3xl pl-20">GiveMeSnack</h1>
          </nuxt-link>
          <nav class="nav work-mode text-2xl pr-20" v-if = this.work.situation >
            <img src="../assets/photo/round_laptop_white_24dp.png" alt="" class="mode-icon">
            勤務中
          </nav>
          <nav class="nav break-mode text-2xl pr-20" v-else>
            <img src="../assets/photo/round_coffee_white_24dp.png" alt="" class="mode-icon">
            休憩中
          </nav>
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
  width: 100%;
  background-color: #573a2e;
  color: white;
}

.mode-icon {
  display: inline;
}
 
.menu-item {
  list-style: none;
  display: inline-block;
  padding: 10px;
}

@media screen and (max-width: 600px) {
  header h1 {
    font-size: 6vw !important;
    padding-left: 10vw !important;
  }

  header nav {
    font-size: 4vw !important;
    padding-right: 10vw !important;
  }
}
</style>