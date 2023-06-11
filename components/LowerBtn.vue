<script>
import IconToDo from '@/assets/images/icon-todo.svg?component';
import IconCalendar from '@/assets/images/icon-calendar.svg?component';
import IconReminders from '@/assets/images/icon-reminders.svg?component';
import IconPlanning from '@/assets/images/icon-planning.svg?component';

export default {
   props: {
      textLine: String,
      iconImg: String,
   },
   components: {
      IconToDo,
      IconCalendar,
      IconReminders,
      IconPlanning,
   }
}
</script>
<template>
   <button class=" flex items-start gap-4 hover:text-neo-black ">
      <component :is="iconImg" class=" mt-[2px] DT:m-0" />
      <h4>{{ textLine }}</h4>
   </button>
</template>