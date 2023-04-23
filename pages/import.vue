<template>
  <div>
    <!-- Static sidebar for desktop -->

    <div class="">
      <div class="hidden lg:fixed lg:inset-y-0 lg:flex lg:w-64 lg:flex-col">
        <!-- Sidebar component, swap this element with another sidebar if you like -->
        <Sidebar />
      </div>
      <main>
        <div class="p-2 space-y-3 sm:p-6 lg:pl-72">
          <div
            class="text-xl font-bold leading-5 mt-7 tracking-normal text-left font-inter"
          >
            Import Excel Sheet
          </div>
          <div
            class="h-auto w-96 bg-white-500 border rounded-2xl absolute top-[100px] left-[320px] border-slate-300"
          >
            <div class="font-inter px-5 py-10">
              <span
                class="absolute top-4 text-sm text-red-400 left-32 font-inter"
                >File formate should be xsxl</span
              >
              <label>Choose File :</label>
              <input
                class="h-10 py-1 border border-slate-300 rounded-md absolute text-left px-2 outline-none left-32 top-26 w-56"
                type="file"
                placeholder="Select file"
              />
              <div class="mt-10 hidden">hi</div>
              <div>
                <input
                  class="h-10 px-5 py-1 border border-slate-300 rounded-md mt-20 text-left outline-none left-32 top-36 w-64"
                  type="text"
                  placeholder="Type message"
                />
              </div>
              <!-- <div class="absolute h-8 w-8 bg-black rounded-full left-[280px] top-[147px]"></div> -->
              <div
                class="absolute h-10 w-16 text-white text-sm px-3.5 py-2 bg-black rounded-md left-[290px] top-[145px]"
              >
                SEND
              </div>
            </div>
            <div></div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
