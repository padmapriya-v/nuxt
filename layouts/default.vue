<template>
  <div id="app">
    <div class="flex h-screen overflow-hidden bg-gray-50 text-dark-color">
      <Sidebar class="" :show="sidebarOpen" :items.sync="items" />

      <div class="relative flex flex-col flex-1 overflow-hidden">
        <main
          class="relative z-0 flex-1 overflow-y-auto focus:outline-none"
          tabindex="0"
        >
          <div class="px-8 py-10 mx-auto max-w-8xl">
            <slot />
          </div>
        </main>
      </div>
    </div>
  </div>
</template>

<script>
import _ from "lodash";

import baseSidebarItems from "sidebar.js"; /* DO NOT REMOVE base PREFIX AS IT WAS USED MY CHILD REPO */
import sidebarItems from "sidebar.js";

export default {
  name: "AppLayout",
  data() {
    let _sidebarItems = sidebarItems;

    const runtimeConfig = useRuntimeConfig();

    console.log("runtimeConfig.public", runtimeConfig.public);

    if (this.$config.APP === "root") {
      // server - root project
      _sidebarItems = sidebarItems;
    } else if (runtimeConfig.public && runtimeConfig.public.APP_BASE_URL) {
      // server - child projects
      const index = _.findIndex(_sidebarItems, (item) => item.group === true);
      _sidebarItems.splice(index, 1);
      _sidebarItems = [..._sidebarItems, ...baseSidebarItems];
    }

    // else - local mode
    return {
      items: _sidebarItems,
      sidebarOpen: false,
    };
  },
  mounted() {
    const auth = useAuth();
    console.log(auth.loggedIn);
    route.push(login);
  },
};
</script>
