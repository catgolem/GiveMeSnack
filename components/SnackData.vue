<template>
  <div class=" shadow-xl mt-10 w-3/4 mx-auto py-4 background-white">
    <div class="next-duty-container p-4">
      <div class="next-duty leading-8">
        <div class="next-duty-wrapper">
          <span class="next-duty-text align-top">次の当番</span>
          <span class="right-arrow-icon" style="display:inline-block; width:2rem; height:2rem;">
            <img src="../assets/photo/round_keyboard_double_arrow_right_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem;">
          </span>
          <span id="next-name" class="next-name align-top">ネコさん</span>
        </div>
        <nuxt-link to="/admin" class="admin-link ml-8">
          <span class="edit-icon" style="display:inline-block; width:2rem; height:2rem;">
            <img src="../assets/photo/round_edit_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem;">
          </span>
          <span class="admin-link-text align-top pr-2">adminへ移動</span>
        </nuxt-link>
      </div>
    </div>
    <div class="snack-data-container flex">
      <div class="snack-vote flex-1 p-4">
        <div class="snack-vote-title font-semibold text-lg mb-2">
          お菓子の投票
        </div>
        <div class="snack-vote-content pl-4">
          <div class="snack-vote-add flex py-2">
            <div class="snack-vote-add-title pr-4 py-2">
              ＋提案
            </div>
            <form class="snack-vote-add-content" action="#" method="post">
              <input class="vote-input p-2 border-2 rounded shadow" type="text" placeholder="入力" required>
              <input class="vote-submit px-4 py-2 border-2 rounded shadow" type="submit" value="追加">
            </form>
          </div>
          <div id="snack-vote-element" class="snack-vote-element">
            <div class="snack-vote-element flex">
              <div class="snack-vote-list flex-1 leading-8">
                ・
                <span id="snack-vote-name" class="snack-vote-name">ポテチ</span>
              </div>
              <div class="snack-like flex-1">
                <button class="like-button">
                  <img src="../assets/photo/round_thumb_up_alt_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                </button>
                <span id="snack-like-num" class="snack-like-num">2</span>
              </div>
            </div>
            <div class="snack-vote-element flex">
              <div class="snack-vote-list flex-1 leading-8">
                ・
                <span id="snack-vote-name" class="snack-vote-name">キットカット</span>
              </div>
              <div class="snack-like flex-1">
                <button class="like-button">
                  <img src="../assets/photo/round_thumb_up_alt_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                </button>
                <span id="snack-like-num" class="snack-like-num">4</span>
              </div>
            </div>
            <div class="snack-vote-element flex">
              <div class="snack-vote-list flex-1 leading-8">
                ・
                <span id="snack-vote-name" class="snack-vote-name">せんべい</span>
              </div>
              <div class="snack-like flex-1">
                <button class="like-button">
                  <img src="../assets/photo/round_thumb_up_alt_black_24dp.png" alt="" class="p-2" style="width: 2rem; height: 2rem; display: inline;">
                </button>
                <span id="snack-like-num" class="snack-like-num">0</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="snack-rank flex-1 p-4">
        <div class="snack-rank-title font-semibold text-lg mb-2">
          人気だったお菓子
        </div>
        <div class="snack-rank-content">
          <div class="snack-rank-container pl-4">
            <div class="snack-rank-element flex py-2">
              <img src="../assets/photo/round_emoji_events_black_24dp.png" alt="" class="flex-none opacity-50 mr-2" style="">
              <div class="snack-rank-snack-name flex-1">
                1.
                <span id="snack-name" class="snack-name ml-2">キットカット</span>
              </div>
              <div class="snack-rank-score flex-1">
                <span class="snack-score ml-4 mr-2">90</span>
                点
              </div>
            </div>
            <div class="snack-rank-element flex py-2">
              <img src="../assets/photo/round_military_tech_black_24dp.png" alt="" class="flex-none opacity-50 mr-2" style="">
              <div class="snack-rank-snack-name flex-1">
                2.
                <span id="snack-name" class="snack-name ml-2">オレオ</span>
              </div>
              <div class="snack-rank-score flex-1">
                <span class="snack-score ml-4 mr-2">85</span>
                点
              </div>
            </div>
            <div class="snack-rank-element flex py-2">
              <img src="../assets/photo/round_military_tech_black_24dp.png" alt="" class="flex-none opacity-50 mr-2" style="">
              <div class="snack-rank-snack-name flex-1">
                3.
                <span id="snack-name" class="snack-name ml-2">ポテチ</span>
              </div>
              <div class="snack-rank-score flex-1">
                <span class="snack-score ml-4 mr-2">80</span>
                点
              </div>
            </div>
            <div class="snack-rank-element flex py-2">
              <img src="../assets/photo/round_icecream_black_24dp.png" alt="" class="flex-none opacity-50 mr-2" style="">
              <div class="snack-rank-snack-name flex-1">
                4.
                <span id="snack-name" class="snack-name ml-2">小枝</span>
              </div>
              <div class="snack-rank-score flex-1">
                <span class="snack-score ml-4 mr-2">75</span>
                点
              </div>
            </div>
            <div class="snack-rank-element flex py-2">
              <img src="../assets/photo/round_icecream_black_24dp.png" alt="" class="flex-none opacity-50 mr-2" style="">
              <div class="snack-rank-snack-name flex-1">
                5.
                <span id="snack-name" class="snack-name ml-2">せんべい</span>
              </div>
              <div class="snack-rank-score flex-1">
                <span class="snack-score ml-4 mr-2">70</span>
                点
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.background-white {
  border-radius: 20px;
  background: #f3f3f3;
  box-sizing: border-box;
  border: solid 24px #e0e0e0;
  border-top: solid 24px #ccc;
  border-bottom: solid 24px #fff;
}

.next-duty-wrapper {
  display: inline;
}

.admin-link {
  position: relative;
  opacity: 0.5;
  transition: 0.3s;
}

.admin-link:hover {
  opacity: 0.9;
}

.admin-link::before {
  content: '';
  width: 100%;
  height: 2px;
  position: absolute;
  bottom: 20%;
  left: 0;
  border-radius: 1px;
  background: #aaa;
}

.admin-link::after {
  content: '';
  width: 0%;
  height: 2px;
  position: absolute;
  bottom: 20%;
  left: 50%;
  border-radius: 1px;
  background: #555;
  transition: 0.3s;
}

.admin-link:hover::after {
  content: '';
  width: 100%;
  height: 2px;
  position: absolute;
  bottom: 20%;
  left: 0;
  border-radius: 1px;
  background: #555;
}

.vote-submit {
  color: #888;
}

.vote-input:valid + input {
  color: #fff;
  background: #573a2e;
  border-color: #573a2e;
}

@media screen and (max-width:1200px) {
  .snack-data-container {
    flex-direction: column;
  }  
}

@media screen and (max-width: 600px) {
  .next-duty-wrapper {
    display: block;
  }

  .snack-vote-add {
    flex-direction: column;
  }

  .vote-input {
    width: 50%;
    width: calc(100% - 80px);
  }
}
</style>