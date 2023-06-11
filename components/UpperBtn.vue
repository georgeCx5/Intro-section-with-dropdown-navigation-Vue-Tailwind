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
   props: {
      btnText: String,
   },
   components: {
      LowerBtn,
      ArrowUp,
      ArrowDown,
   }
}
</script>
<template>
   <div class=" relative flex flex-col gap-4">
      <!-- Features -->
      <button @click="showFeatures = !showFeatures" v-if="btnText == 'Features'"
         class=" flex items-center gap-4 hover:text-neo-black">
         <h3>{{ btnText }}</h3>
         <div>
            <ArrowDown v-show="!showFeatures" />
            <ArrowUp v-show="showFeatures" />
         </div>
      </button>
      <div v-show="showFeatures"
         class=" DT:absolute DT:top-11 DT:right-0 flex flex-col DT:justify-center DT:w-[153px] DT:h-[160px] DT:bg-white my-[8px] DT:m-0 gap-4 px-6 DT:rounded-[10px] DT:shadow-lower-btn">
         <LowerBtn textLine="Todo List" iconImg="IconToDo" />
         <LowerBtn textLine="Calendar" iconImg="IconCalendar" />
         <LowerBtn textLine="Reminders" iconImg="IconReminders" />
         <LowerBtn textLine="Planning" iconImg="IconPlanning" />
      </div>
      <!-- Companies -->
      <button @click="showCompanies = !showCompanies" v-if="btnText == 'Company'"
         class=" flex items-center gap-4 hover:text-neo-black">
         <h4>{{ btnText }}</h4>
         <div>
            <ArrowDown v-show="!showCompanies" />
            <ArrowUp v-show="showCompanies" />
         </div>
      </button>
      <div v-show="showCompanies"
         class=" DT:absolute DT:top-11 DT:right-0 flex flex-col DT:justify-center gap-4 DT:w-[116px] DT:h-[128px] DT:bg-white mt-[2px] mb-[8px] DT:m-0 px-6 DT:rounded-[10px] DT:shadow-lower-btn">
         <LowerBtn textLine="History" />
         <LowerBtn textLine="Our Team" />
         <LowerBtn textLine="Blog" />
      </div>
   </div>
</template>