<template>
  <div class="px-12">
    <VueSlickCarousel v-bind="settings">
      <div>
        <p
          class="text-gray-600 serif font-normal italic px-4 py-6 md:px-16 md:py-10 text-xl md:text-2xl"
          x-show.transition="testimonialActive == 1"
        >
          Leverage agile frameworks to provide a robust synopsis for high level
          overviews. Iterative approaches to corporate strategy foster
          collaborative thinking to further the overall value proposition.
          Organically grow the holistic world view of disruptive innovation via
          workplace diversity and empowerment.
        </p>
        <div>
          <img
            alt="Placeholder"
            class="block rounded-full"
            src="https://picsum.photos/32/32/?random"
          />
          <p class="ml-2 text-sm">Author Name</p>
          <div class="visibility"></div>
        </div>
      </div>
      <div>
        <p
          class="text-gray-600 serif font-normal italic px-4 py-6 md:px-16 md:py-10 text-xl md:text-2xl"
          x-show.transition="testimonialActive == 2"
        >
          Bring to the table win-win survival strategies to ensure proactive
          domination. At the end of the day, going forward, a new normal that
          has evolved from generation X is on the runway heading towards a
          streamlined cloud solution. User generated content in real-time will
          have multiple touchpoints for offshoring.
        </p>
        <div>
          <img
            alt="Placeholder"
            class="block rounded-full"
            src="https://picsum.photos/32/32/?random"
          />
          <p class="ml-2 text-sm">Author Name</p>
          <div class="visibility"></div>
        </div>
      </div>
      <div>
        <p
          class="text-gray-600 serif font-normal italic px-4 py-6 md:px-16 md:py-10 text-xl md:text-2xl"
          x-show.transition="testimonialActive == 3"
        >
          Capitalize on low hanging fruit to identify a ballpark value added
          activity to beta test. Override the digital divide with additional
          clickthroughs from DevOps. Nanotechnology immersion along the
          information highway will close the loop on focusing solely on the
          bottom line.
        </p>
        <div>
          <img
            alt="Placeholder"
            class="block rounded-full"
            src="https://picsum.photos/32/32/?random"
          />
          <p class="ml-2 text-sm">Author Name</p>
          <div class="visibility"></div>
        </div>
      </div>
    </VueSlickCarousel>
  </div>
</template>
<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
  components: { VueSlickCarousel },
  data() {
    return {
      settings: {
        arrows: true,
        dots: true,
      },
    }
  },
}
</script>
