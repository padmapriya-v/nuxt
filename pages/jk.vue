<template>
  <div>
    <!-- Static sidebar for desktop -->
    <div class="hidden lg:fixed lg:inset-y-0 lg:flex lg:w-64 lg:flex-col">
      <!-- Sidebar component, swap this element with another sidebar if you like -->
      <Rightbar />
    </div>
    <div class="flex flex-col flex-1 lg:pl-64">
      <main class="flex-1">
        <div class="py-6">
          <div class="p-2 sm:p-6">
            <div>hi</div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
