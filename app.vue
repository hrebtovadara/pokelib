<template>
  <div class="mem">
    {{store.count}}
    <button class="t" @click="store.increment">lol</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { useCounterStore } from '@/store/test'

export default defineComponent ({
  name: 'app',
  setup() {
    const store = useCounterStore()

    return {
      store,
    }
  }
})
</script>


<style lang="scss">
.mem {
  background: red;

  .t {
    background: blue;
  }
}

</style>