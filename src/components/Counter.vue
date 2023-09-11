  <template>
    <div>
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
    },
  };
  </script>

  <style scoped>
  .top {
    text-align: center;
  }

  .counter-heading {
    font-size: 24px;
    font-weight: bold;
  }

  .count-text1 {
    font-size: 50px;
    display: inline-block; /* Change display property to inline-block */
  　margin-right: 20px; /* Add some right margin to separate them */
    position: absolute;
    bottom: 0;
    right: 30%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
  }

  .count-text2 {
    
    font-size: 100px;
    display: inline-bock; /* Change display property to inline-block */
  　margin-right: 20px; /* Add some right margin to separate them */
    position: absolute;
    bottom: 0;
    left: 30%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
  }

  .count1 {
   display: flex;
  flex-direction: column;
  }

  .count2 {
      display: flex;
  flex-direction: column;
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
    padding: 30px 50px;
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
    left: 44%; /* Center horizontally */
  　transform: translateX(-50%); /* Center horizontally */
  }
  </style>

