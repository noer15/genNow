<template>
  <div class="flex flex-col m-auto p-auto">
    <h1
      class="flex py-5 lg:px-8 md:px-10 px-0 lg:px-5 lg:mx-1 md:mx-20 mx-5 font-bold text-2xl lg:text-4xl text-gray-800"
    >
      Kelas Online
    </h1>
    <div class="flex overflow-x-scroll pb-10 hide-scroll-bar">
      <div
        v-for="i in 6"
        :key="i"
        class="flex flex-nowrap lg:ml-4 md:ml-20 ml-2"
      >
        <a href="#">
          <div class="inline-block px-3 group">
            <div
              class="slide-source rounded-xl overflow-hidden card-shadow relative"
            >
              <div
                class="absolute opacity-0 group-hover:opacity-50 transition duration-200 flex items-center justify-center w-full h-full bg-black bg-opacity-35"
              ></div>
              <div class="rounded-t-xl w-full h-full text-center">
                <div
                  class="bg-gray-300 rounded-t-xl w-full h-full text-center border-solid border border-gray-300"
                >
                  <svg
                    class="animate-pulse mt-20 mx-auto feather feather-image"
                    xmlns="http://www.w3.org/2000/svg"
                    width="140"
                    height="140"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  >
                    <rect
                      x="3"
                      y="3"
                      width="18"
                      height="18"
                      rx="2"
                      ry="2"
                    ></rect>
                    <circle cx="8.5" cy="8.5" r="1.5"></circle>
                    <polyline points="21 15 16 10 5 21"></polyline>
                  </svg>
                  <div class="py-4 animate-pulse">Tidak ada gambar</div>
                </div>
              </div>
            </div>
            <div
              class="bg-section-gen rounded-b-xl shadow-md mb-3 w-full lg:w-80 text-white -mt-2"
            >
              <div class="px-2 py-4">
                <div
                  class="flex items-center justify-between leading-tight"
                  style="padding: 0.5rem"
                >
                  <h1 class="text-xl lg:text-2xl">Matematika</h1>
                  <div class="gen-now-opacity">
                    <span class="lg:font-light py-2 px-4 leading-loose text-sm"
                      >12 Video</span
                    >
                  </div>
                </div>
                <div
                  class="flex items-center justify-between leading-tight"
                  style="padding: 0.5rem"
                >
                  <h5 class="font-light">Theory Phitagoras</h5>
                  <div class="flex justify-between">
                    <img
                      src="/star.png"
                      alt="rating"
                      style="width: 18px; height: 18px"
                    />
                    <span class="ml-2">4.5</span>
                  </div>
                </div>
                <hr
                  class="mb-2 mt-2 border border-gray-400 mx-auto"
                  style="width: 95%"
                />

                <div
                  class="flex items-center justify-between leading-none p-2 md:p-4"
                >
                  <img
                    alt="Placeholder"
                    class="block rounded-full"
                    src="https://picsum.photos/32/32/?random"
                  />
                  <p class="ml-2 text-sm">Author Name</p>
                  <div class="visibility"></div>
                </div>
              </div>
            </div>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>
