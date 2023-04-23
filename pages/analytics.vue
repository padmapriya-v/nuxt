<template>
  <div>
    <!-- Static sidebar for desktop -->

    <div class="">
      <div class="hidden lg:fixed lg:inset-y-0 lg:flex lg:w-64 lg:flex-col">
        <!-- Sidebar component, swap this element with another sidebar if you like -->
        <Sidebar />
      </div>
      <main>
        <div
          class="ml-96 absolute left-[550px] overflow-y-auto border-left-gray-900 h-screen w-[346px] border"
        >
          <div>History</div>
        </div>
        <div class="p-2 space-y-3 sm:p-6 lg:pl-72">
          <div
            class="text-xl font-bold leading-5 tracking-normal text-left font-inter"
          >
            Analytics
          </div>
          <div>
            <div class="grid grid-cols-3 gap-10 pt-4">
              <div class="border border-gray-300 h-44 rounded-xl">
                <span class="absolute mt-5 ml-3.5">
                  <!-- <img class="w-16 h-20 mt-5" src="/pdf.svg" alt="" /> -->
                </span>
                <div
                  class="px-5 mt-5 ml-20 text-lg font-bold leading-5 tracking-normal text-left text-gray-900 font-inter"
                ></div>
                <div
                  class="px-5 font-bold mt-1 ml-14 text-xl leading-5 tracking-normal text-left text-gray-900 font-inter"
                >
                  Over All Leads
                  <br />
                </div>

                <!-- <a target="_blank" download>
                  <div
                    class="h-8 mt-2 ml-24 text-xs font-semibold leading-5 tracking-normal text-blue-600 border border-blue-200 rounded-md w-36 font-inter"
                  >
                    <span class="absolute px-3 py-1 text-sm font-bold leading-5 tracking-normal text-center font-inter">
                      View
                      <span class="absolute w-6 h-6 px-1 py-0.5"><img src="/import1.svg" alt="" /></span>
                    </span>
                  </div>
                 </a> -->
              </div>
              <div class="border border-gray-300 h-44 rounded-xl">
                <span class="absolute mt-5 ml-3.5">
                  <!-- <img class="w-16 h-20 mt-5" src="/pdf.svg" alt="" /> -->
                </span>
                <div
                  class="px-5 mt-5 ml-20 text-lg font-bold leading-5 tracking-normal text-left text-gray-900 font-inter"
                ></div>
                <div
                  class="px-5 font-bold mt-1 ml-14 text-xl leading-5 tracking-normal text-left text-gray-900 font-inter"
                >
                  Recent Leads

                  <br />
                </div>

                <!-- <a target="_blank" download>
                  <div
                    class="h-8 mt-2 ml-24 text-xs font-semibold leading-5 tracking-normal text-blue-600 border border-blue-200 rounded-md w-36 font-inter"
                  >
                    <span class="absolute px-3 py-1 text-sm font-bold leading-5 tracking-normal text-center font-inter">
                      View
                      <span class="absolute w-6 h-6 px-1 py-0.5"><img src="/import1.svg" alt="" /></span>
                    </span>
                  </div>
                 </a> -->
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
