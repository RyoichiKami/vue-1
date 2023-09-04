<template>
  <div>
    <h1 class="counter-heading">カウンターアプリ</h1>
    <p class="count-text">カウント: {{ count }}</p>
    <button @click="increment" class="action-button">増やす</button>
    <button @click="decrement" class="action-button">減らす</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
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
  cursor: pointer;
}

.action-button:hover {
  background-color: #0056b3;
}
</style>

