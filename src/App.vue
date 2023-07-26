<template>
  <div class="counter">
    <p>{{ count }}</p>
  </div>
  <br />
  <div id="container" class="clear">
    <div id="increase" class="increase-box">
      <input type="number" v-model="inputValue" />
      <br />
      <br />
      <button @click="increaseCount">Arttır</button>
    </div>

    <div id="decrease" class="decrease-box">
      <input type="number1" v-model="inputValue" />
      <br />
      <br />
      <button @click="decreaseCount">Azalt</button>
    </div>
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
export default {
  components: {
    Counter,
  },
  data() {
    return {
      count: 1000,
    };
  },
  methods: {
    increaseCount() {
      this.count += this.inputValue;
      this.inputValue = 0;
    },
    decreaseCount() {
      this.count -= this.inputValue;
      this.inputValue = 0;
    },
  },
};
</script>

<style>
.counter {
  text-align: center;
  font-size: large;
  font-weight: bold;
  font-weight: 800;
  width: 500px;
  border: 15px solid rgb(9, 88, 192);
  padding: 50px;
}

.increase-box, .decrease-box {
  margin: 20px;
  padding: 0.5rem 0.5rem;
  margin-top: 20px;
  width: 200px;
  height: 100px;
}

.clear {
  overflow: auto;
}

#increase {
  float: left;
  border: 3px solid #a916ca;
}

#decrease {
  float: left;
  border: 3px solid #73ad21;
}


</style>
