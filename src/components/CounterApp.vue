<template>
  <div class="counter">
    <h2 class="heading-secondary">Counter: {{ count }}</h2>
    <div class="btn-wrapper">
      <button class="btn decrement" @click="decrement">-</button>
      <button class="btn increment" @click="increment">+</button>
    </div>
    <div class="input-wrapper">
      <input class="input-field" type="number" v-model="value" />
      <input
        class="setvalue"
        type="submit"
        @click="setValue(value)"
        value="Set Value"
      />
    </div>
    <button class="btn reset" @click="reset">Reset</button>
  </div>
</template>

<script>
import useCounter from "@/composables/counter";

export default {
  setup() {
    const { count, increment, decrement, reset, setValue } = useCounter();

    return {
      count,
      increment,
      decrement,
      reset,
      setValue,
      value: 0,
    };
  },
};
</script>

<style scoped>
.counter {
  animation: easeIn 1s ease-in-out;
}
.heading-secondary {
  font-size: 3.5rem;
  text-transform: uppercase;
  font-weight: 700;
  display: inline-block;
  color: #fff;
  letter-spacing: 0.2rem;
  transition: all 0.2s;
}
.heading-secondary:hover {
  transform: skewY(2deg) skewX(15deg) scale(1.1);
  text-shadow: 0.5rem 1rem 2rem rgba(0, 0, 0, 0.2);
}

.btn {
  text-transform: uppercase;
  text-decoration: none;
  padding: 2rem 5rem;
  margin: 3rem;
  background-color: #7ed56f;
  color: #000;
  display: inline-block;
  border-radius: 10rem;
  border: none;
  transition: all 0.2s;
  font-size: 1.8rem;
  font-weight: 600;
  transition: all 0.2s;
}

.btn:hover {
  transform: translateY(-0.3rem);
  box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.2);
  background-color: #28b485;
  color: #fff;
}

@keyframes easeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.input-wrapper {
  width: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

input {
  border: none;
  height: 4rem;
  padding: 1rem;
  width: 17rem;
  margin: 2rem 0;
  font-size: 1.8rem;
}
.input-field {
  border-radius: 1rem 0 0 1rem;
  outline: none;
}
.setvalue {
  border-radius: 0 1rem 1rem 0;
  border-left: 0.1rem solid #fff;
  font-weight: 700;
  width: 10rem;
  padding: 1rem;
  background-color: #7ed56f;
  color: #000;
}
.setvalue:hover {
  background-color: #28b485;
  transition: all 0.4s;
}
</style>
