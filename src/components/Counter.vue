  <template>
    <div>
    　<div class="main">
      <div class="top">  
      <h1 class="counter-heading">カウンターアプリ</h1>
      </div>
      <div class="count-text">
      <p class="count-text1"> {{ count1 }}</p>
      <p class="count-text2"> {{ count2 }}</p>
      </div>
        <div class="count1">
        <button @click="increment1" class="action-button">＋</button>
        <button @click="decrement1" class="action-button">ー</button>
        </div>
        <div class="count2">
        <button @click="increment2" class="action-button">＋</button>
        <button @click="decrement2" class="action-button">ー</button>
        </div>
      <button @click="clear" class="clear-button">クリア</button> <!-- クリアボタンを追加 -->
      <div class="buzzer">
        <button @click="playSound">音を再生</button>
        <audio ref="audio">
        <source src="https://example.com/sound.mp3" type="audio/mpeg">
        <!-- 音声ファイルのURLを指定します -->
    </audio>
      </div>  
     </div>
    </div>
  </template>

  <script>
  export default {
    data() {
      return {
        count1: 0,
        count2: 0,
      };
    },
    methods: {
      increment1() {
        this.count1++;
      },
      decrement1() {
        if (this.count1 > 0) {
          this.count1--;
        }
      },
      increment2() {
        this.count2++;
      },
      decrement2() {
        if (this.count2 > 0) {
          this.count2--;
        }
      },
      clear() {
        this.count1 = 0; // カウント1をクリア
        this.count2 = 0; // カウント2をクリア
      },
      playSound() {
      // <audio>要素を取得
      const audioElement = this.$refs.audio;
      // 音声を再生
      audioElement.play();
       }
    },
  };
  </script>

  <style scoped>
  .main {
    background-color: ;
  }
  
  .top {
    text-align: center;
  }

  .counter-heading {
    font-size: 24px;
    font-weight: bold;
  }

  .count-text1 {
    height: 100px;
    font-size: 100px;
    display: inline-block; /* Change display property to inline-block */
  　margin-right: 20px; /* Add some right margin to separate them */
    position: absolute;
    bottom: 0;
    right: 30%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
    color: orange;
    font-family: 
  }

  .count-text2 {
    height: 100px;
    font-size: 100px;
    display: inline-bock; /* Change display property to inline-block */
  　margin-right: 20px; /* Add some right margin to separate them */
    position: absolute;
    bottom: 0;
    left: 30%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
    color: orange;
    font-family: "";
  }

  .count1 {
   display: flex;
  flex-direction: column;
  bottom: 0;
  left: 100%; /* 左下に移動 */
  transform: translateX(90%);
  }

  .count2 {
   display: flex;
   flex-direction: column;
   transform: translateX(2%);
  }

  .action-button {
    padding: 8px 16px;
    font-size: 16px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    margin-right: 8px;
    margin-top: 10px;
    margin-bottom: 10px;
    cursor: pointer;
    width: 100px; /* ボタンの横幅を100pxに設定 */
      font-size: 16px; /* テキストサイズを調整 */
    margin-right: 10px; /* ボタン間の間隔を設定 */
  }

  .action-button:hover {
    background-color: #0056b3;
  }

  .clear-button {
    padding: 10px 40px;
    font-size: 16px;
    background-color: red; /* ボタンの背景色を赤に変更 */
    color: white;
    border: none;
    border-radius: 4px;
    margin-right: 10px;
    margin-top: 10px;
    margin-bottom: 10px;
    cursor: pointer;
    position: absolute;
    bottom: 0;
    left: 45.5%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
  }
  </style>

