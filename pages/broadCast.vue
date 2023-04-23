<template>
  <div>
    <!-- Static sidebar for desktop -->
    <div class="hidden lg:fixed lg:inset-y-0 lg:flex lg:w-64 lg:flex-col">
      <!-- Sidebar component, swap this element with another sidebar if you like -->
      <Sidebar />
    </div>
    <div class="flex flex-col flex-1 lg:pl-64">
      <main class="flex-1">
        <div class="py-6">
          <div class="p-2 sm:p-6">
            <h1 class="font-bold text-xl font-inter">BroadCast</h1>

            <div
              class="h-16 top-[20px] absolute left-[1080px] rounded-2xl w-48 bg-blue-800 font-normal cursor-pointer border-2"
              @click="clickModel = !clickModel"
            >
              <div class="text-center mt-4 text-white font-bold font-inter">
                Create Broadcast
              </div>
            </div>
            <div
              v-if="clickModel"
              class="h-[220px] bg-white rounded-2xl w-96 absolute border-2 top-[120px] left-[550px]"
            >
              <div
                class="bg-gray-100 h-12 font-inter font-bold text-md py-3 px-5"
              >
                CREATE
              </div>
              <div
                class="absolute top-3 bg-slate-300 h-6 w-6 rounded-full left-[340px]"
                @click="clickModel = !clickModel"
              >
                <span class="py-1.5 px-1.5">X</span>
              </div>
              <div
                class="py-3 font-bold leading-5 text-left ml-20 font-inter text-md"
              >
                Broadcast Name
              </div>
              <div class=" ">
                <input
                  class="h-10 border border-slate-300 rounded-md absolute text-left px-5 outline-none left-20 top-26 w-56"
                  type="text"
                  placeholder="Enter broadcast name"
                />
              </div>
              <button
                class="absolute top-40 ml-36 text-white font-inter rounded-md h-10 w-20 bg-blue-800"
              >
                Save
              </button>
            </div>
            <div class="grid grid-cols-3 gap-4 pt-4 mt-12">
              <nuxt-link to="/import">
                <div class="border border-gray-300 h-44 rounded-xl">
                  <span class="absolute mt-5 ml-3.5">
                    <!-- <img class="w-16 h-20 mt-5" src="/pdf.svg" alt="" /> -->
                  </span>
                  <div
                    class="px-5 mt-5 ml-20 text-lg font-bold leading-5 tracking-normal text-left text-gray-900 font-inter"
                  ></div>
                  <div
                    class="text-center font-bold text-xl leading-5 tracking-normal py-12 text-gray-900 font-inter"
                  >
                    Grade 1
                    <br />
                  </div>
                </div>
              </nuxt-link>

              <div class="border border-gray-300 h-44 rounded-xl">
                <span class="absolute mt-5 ml-3.5">
                  <!-- <img class="w-16 h-20 mt-5" src="/pdf.svg" alt="" /> -->
                </span>
                <div
                  class="px-5 mt-5 ml-20 text-lg font-bold leading-5 tracking-normal text-left text-gray-900 font-inter"
                ></div>
                <div
                  class="text-center font-bold text-xl leading-5 tracking-normal py-12 text-gray-900 font-inter"
                >
                  Grade 2
                  <br />
                </div>
              </div>
              <div class="border border-gray-300 h-44 rounded-xl">
                <span class="absolute mt-5 ml-3.5">
                  <!-- <img class="w-16 h-20 mt-5" src="/pdf.svg" alt="" /> -->
                </span>
                <div
                  class="px-5 mt-5 ml-20 text-lg font-bold leading-5 tracking-normal text-left text-gray-900 font-inter"
                ></div>
                <div
                  class="text-center font-bold text-xl leading-5 tracking-normal py-12 text-gray-900 font-inter"
                >
                  Grade 3
                  <br />
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      clickModel: false,
    };
  },
  methods: {
    closeModal() {
      this.clickModel = false;
    },
  },
};
</script>
