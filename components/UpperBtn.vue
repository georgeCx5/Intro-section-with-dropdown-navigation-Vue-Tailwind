<script>
import ArrowUp from '@/assets/images/icon-arrow-up.svg?component';
import ArrowDown from '@/assets/images/icon-arrow-down.svg?component';

import LowerBtn from '@/components/LowerBtn.vue';

export default {
   data() {
      return {
         showFeatures: false,
         showCompanies: false,
      }
   },
   components: {
      LowerBtn,
      ArrowUp,
      ArrowDown,
   }
}
</script>
<template>
   <!-- Features -->
   <button @click=" showFeatures = !showFeatures" class=" flex items-center gap-4">
      <h3 class=" hover:text-neo-black">Features</h3>
      <div>
         <ArrowDown v-show="!showFeatures" />
         <ArrowUp v-show="showFeatures" />
      </div>
   </button>
   <div v-show="showFeatures" class=" flex flex-col my-[8px] gap-4 px-6">
      <LowerBtn textLine="Todo List" iconImg="IconToDo" />
      <LowerBtn textLine="Calendar" iconImg="IconCalendar" />
      <LowerBtn textLine="Reminders" iconImg="IconReminders" />
      <LowerBtn textLine="Planning" iconImg="IconPlanning" />
   </div>
   <!-- Companies -->
   <button @click="showCompanies = !showCompanies" class=" flex items-center gap-4">
      <h4 class=" hover:text-neo-black">Company</h4>
      <div>
         <ArrowDown v-show="!showCompanies" />
         <ArrowUp v-show="showCompanies" />
      </div>
   </button>
   <div v-show="showCompanies" class=" flex flex-col gap-4 mt-[2px] mb-[8px] px-6">
      <LowerBtn textLine="History" />
      <LowerBtn textLine="Our Team" />
      <LowerBtn textLine="Blog" />
   </div>
</template>