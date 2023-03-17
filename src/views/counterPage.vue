<template>
  <div class="header-box">
    <header>
      <img
        alt="AltSchool logo"
        class="logo"
        src="@/assets/ada.jpg"
        width="125"
        height="125"
      />
      <div class="wrapper">
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/counter">Counter</RouterLink>
          <a href="https://github.com/itsadaeze/AltSchool-Exam"
            >Github</a
          >
          
            
        </nav>
      </div>
    </header>
  </div>
  <div class="counter-wrapper">
    <div class="counter-box">
      <div class="heading-count">
        <p class="count-heading">Counting App</p>
        <p class="count">{{ $store.state.counter }}</p>
      </div>
      <!-- <p class="count">{{$store.state.counter}}</p> -->
      <div class="button-box">
        <increment-counter />
        <decrement-counter />
        <reset-counter />
      </div>
      <div class="input-value">
        <input
          type="number"
          placeholder="type your counting"
          v-model="$store.state.counter"
        />
        <set-value />
      </div>
    </div>
  </div>
</template>

<script>
import incrementCounter from "@/components/incrementCounter";
import decrementCounter from "@/components/decrementCounter";
import resetCounter from "@/components/resetCounter";
import setValue from "@/components/setValue";

export default {
  components: {
    incrementCounter,
    decrementCounter,
    resetCounter,
    setValue,
  },
};
</script>
<style>
.header-box {
 
  background: #e009bc;
}
.logo{
  
  border-radius: 50px;
}
.counter-wrapper {
  border-top: 2px solid white;
  height: 100vh;
  margin-top: 0px;
  background-color: #e009bc;
}
.heading-count {
  height: 120px;
}
.counter-box {
  max-width: 350px;
  text-align: center;
  margin: 0 auto;
  margin-top: 60px;
  background-color: white;

  border: 2px solid rgba(100, 100, 111, 0.2);
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 50px;
  padding-bottom: 50px;
  padding-top: 30px;
}
.button-box {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.count-heading {
  color: #e009bc;
}
.count {
  font-size: 24px;
  color: #e009bc;
}
.input-value {
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
  justify-content: center;
}
</style>
