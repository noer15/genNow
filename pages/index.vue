<template>
  <div>
    <Jumbotron />
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8 p-2">
      <Class />
      <section>
        <Testimoni />
      </section>
    </div>
    <!-- testimoni -->
  </div>
</template>

<script>
import Jumbotron from '~/components/Jumbotron'
import Testimoni from '~/components/Testimoni'
import Class from '~/components/Class'

export default {
  components: {
    Jumbotron,
    Testimoni,
    Class,
  },
  layout: 'default',
}
</script>
