<template>
  <NavBar />
  <div class="wrap">
    <div class="count">
      <div class="ui">
        <button @click="increment" class="add">+</button>
        <div class="interface">{{ count }}</div>
        <button @click="decrement" class="minus">-</button>
      </div>
      <div class="btn">
        <input
          type="number"
          v-model="value"
          placeholder="Enter a number"
          class="input"
        />
        <button @click="setValue(value)" class="set">Set Value</button>
        <button @click="reset" class="reset">Reset</button>
      </div>
    </div>
  </div>
</template>

<script>
import useCounter from "@/components/Counter.js";
import NavBar from "./NavBar.vue";

export default {
  setup() {
    const { count, increment, decrement, reset, setValue } = useCounter();

    let value = "";

    return {
      count,
      increment,
      decrement,
      reset,
      value,
      setValue,
    };
  },
  components: {
    NavBar,
  },
};
</script>

<style scoped>
.count {
  padding: 0.2% 7%;
  background-color: grey;
  color: #fff;
  color: black;
  width: max-content;
  height: auto;
  border-radius: 10px;
  box-shadow: 2xl red;
  margin-inline: auto;
  padding: 2%;
}

.ui {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 50px;
  margin-bottom: 30px;
}

.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 50px;
}

.add {
  background-color: green;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  font-size: 1.5rem;
  cursor: pointer;
  transition: 0.5s;
}

.add:hover {
  opacity: 0.8;
}

.minus {
  background-color: #fd3668;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  font-size: 1.5rem;
  cursor: pointer;
  transition: 0.5s;
}

.minus:hover {
  background-color: #ff0846;
}

.interface {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #ffffff;
  padding: 10px 25px;
  width: 50px;
  height: 50px;
  border: none;
  border-radius: 5px;
  font-size: 1.5rem;
  color: black;
  transition: 0.5s;
}
.reset {
  background-color: #fd3668;
  color: white;
  padding: 10px 25px;
  border: none;
  border-radius: 5px;
  font-size: 1.5rem;
  cursor: pointer;
  transition: 0.5s;
}

.reset:hover {
  background-color: #ff0846;
}

.input {
  background-color: #ffffff;
  padding: 10px 25px;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
  transition: 0.5s;
}

.set {
  background-color: green;
  color: white;
  padding: 10px 25px;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
  transition: 0.5s;
}
</style>
