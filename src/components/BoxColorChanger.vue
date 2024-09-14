<template>
  <div class="box" :style="{ backgroundColor: currentColor }"></div>
  <button @click="changeColor">Change Color</button>
</template>

<script>
export default {
  data() {
    return {
      currentColor: "#42b983",
      colors: ["#42b983", "#ff0000", "#0000ff", "#ffff00", "#ff00ff", "#00ffff"],
    };
  },
  methods: {
    changeColor() {
      const randomIndex = Math.floor(Math.random() * this.colors.length);
      this.currentColor = this.colors[randomIndex];
    },
  },
};
</script>

<style scoped>
/* Box styling */
.box {
  width: 200px;
  height: 200px;
  background-color: #42b983;
  margin-bottom: 10px;
  border-radius: 10px;
}

/* Button styling */
button {
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  font-size: 16px;
}

button:hover {
  background-color: #35936d;
}
</style>
