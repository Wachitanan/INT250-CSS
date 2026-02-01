<script setup>
import { ref } from 'vue';

const count = ref(0);
const step = ref(1);

function increment(){
    if(count.value + step.value <= 100){
        count.value += step.value;
    } else {
        count.value = 100;
    }
    
}

function decrement(){
    if(count.value - step.value >= 0 ) {
        count.value -= step.value;
    } else {
        count.value = 0;
    }

}

function reset(){
    count.value = 0;
}
</script>

<template>
    <div class="page">
        <div class="card">
            <h1>Counter App</h1>
            <p>Click buttons to change the number.</p>

        <div class="count">{{ count }}</div>
        
        
        <div class="row">
            <button class="btn inc" @click="increment">+ Increase</button>
            <button class="btn dec" @click="decrement">- Decrease</button>
        </div>

        <div class="row">
            <button class="btn reset" @click="reset">Reset</button>
        </div>

        <div class="hint">
            Step: <input type="number" min="1" max="100" v-model.number="step">
        </div>

    </div>
</div>

</template>

<style scoped>

.page{
    display: flex;
    justify-content: center;
    align-items: center;
    background: url(https://4kwallpapers.com/images/wallpapers/blue-abstract-waves-1920x1080-17108.jpeg) center / cover no-repeat;
    min-height: 100vh;
    
}

.card {
    width: min(480px, 92vw);
    background-color: white;
    border-radius: 16px;
    padding: 24px;
    box-shadow: 0 8px 30px rgba(0,0,0,0.08);
    display: grid;
    place-items: center;
    transition: box-shadow 0.3s ease,transform 0.3s ease;

}
.card:hover {
  box-shadow: 0 16px 50px rgba(0,0,0,0.30);
  transform: translateY(-3px);
}
h1{
    margin: 0 0 6px;
    text-align: center;
    font-size: 36px;
}
</style>