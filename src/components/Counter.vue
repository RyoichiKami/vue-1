<template>
  <div>
    <h1 class="counter-heading">カウンターアプリ</h1>
    <p class="count-text">カウント: {{ count1 }}</p>
    <p class="count-text">カウント: {{ count2 }}</p>
    <div class="count1">
    <button @click="increment1" class="action-button">＋</button>
    <button @click="decrement1" class="action-button">ー</button>
    </div>
    <div class="count2">
    <button @click="increment2" class="action-button">＋</button>
    <button @click="decrement2" class="action-button">ー</button>
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
    decrement1() {
      if (this.count2 > 0) {
        this.count2--;
      }
    },
  },
};
</script>

<style scoped>
.counter-heading {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 16px;
}

.count-text {
  font-size: 18px;
  margin-bottom: 12px;
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
  cursor: pointer;
}

.action-button:hover {
  background-color: #0056b3;
}
</style>

