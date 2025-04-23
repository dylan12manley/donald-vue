<script setup>
import { ref } from 'vue';
import BreadMaker from './BreadMaker.vue';

defineProps({
  msg: String,
});

const count = ref(0);

const showBreadMaker = ref(false);

function getWeekNumber(date) {
  const start = new Date(date.getFullYear(), 0, 1);
  const days = Math.floor((date - start) / (24 * 60 * 60 * 1000));
  return Math.ceil((days + start.getDay() + 1) / 7);
}

const daysUntilOffWork = () => {
  const today = new Date();
  const workDays = [4, 5, 6];
  if (getWeekNumber(today) % 2 !== 0) {
    workDays.push(3);
    workDays.reverse();
  }
  if (!workDays.includes(today.getDay())) {
    const weekendDays = workDays[0] - today.getDay();
    return `Enjoy the ${weekendDays} day${weekendDays > 0 ? '' : 's'} left in your weekend!`;
  }
  const daysLeft = 7 - today.getDay();
  return `You have ${daysLeft} days left in your work week.`;
};
</script>

<template>
  <h1>Donald's App</h1>

  <!-- <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
    {{ daysUntilOffWork() }}
  </div> -->
  <h2>{{ daysUntilOffWork() }}</h2>
  <button type="button" @click="showBreadMaker = !showBreadMaker">{{ showBreadMaker ? 'Hide' : 'Show' }} Bread Maker</button>
  <BreadMaker v-if="showBreadMaker" />
  <!-- <img src="./assets/bread-maker.jpg" alt="Bread Maker" /> -->
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
