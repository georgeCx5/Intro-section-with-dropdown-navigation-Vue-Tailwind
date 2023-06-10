<script>
import clientData from '@/assets/images/client-databiz.svg?url';
import clientAudio from '@/assets/images/client-audiophile.svg?url';
import clientMeet from '@/assets/images/client-meet.svg?url';
import clientMaker from '@/assets/images/client-maker.svg?url';

export default {
   data() {
      return {

         brands: [
            clientData,
            clientAudio,
            clientMeet,
            clientMaker
         ]
      }
   },
   props: {
      index: String,
      wSize: String,
   }
}
</script>
<template>
   <img :class="`${wSize}`" :src="brands[index]" draggable="false" alt="Brand logo">
</template>