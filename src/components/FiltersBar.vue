<template>
  <div class="md:h-16 flex flex-col md:flex-row justify-between items-center bg-white border-b border-gray-200 px-4 sm:px-5 py-2.5">
<!--    Filters-->
    <div class="flex order-2 md:order-1 items-center max-w-md lg:max-w-lg w-full">
      <div class="w-full relative">
        <div class="w-full flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
          <SearchIcon class="w-5 h-5 text-gray-500" />
        </div>
        <input type="text" placeholder="Agreement"
               class="h-11 bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg
                    focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 pr-2.5">
      </div>
      <button type="button"
              class="text-gray-500 bg-gray-50 whitespace-nowrap
              border border-gray-200 ml-7 h-11
              hover:bg-gray-100 hover:text-gray-900 focus:ring-4 focus:ring-gray-300
              font-normal rounded-lg text-base px-3 py-2.5 text-center inline-flex items-center">
        Add Filter
        <ChevronUpIcon class="ml-1 -mr-1 w-5 h-5" />
      </button>

    </div>

    <div class="flex order-1 md:order-2 items-center mb-3 md:mb-0">
      <button type="button">
        <ViewGridIcon class="w-9 h-9 text-blue-500" />
      </button>
      <button>
        <ViewListIcon class="w-9 h-9 text-gray-400 ml-2" />
      </button>

      <button type="button"
              class="ml-10 text-white bg-blue-500 hover:bg-blue-700 h-9
              focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-xs px-3 py-2 text-center">

        <PlusSmIcon class="w-5 h-5 text-white inline mr-2" />Nouveau contrat
      </button>
    </div>
  </div>

</template>

<script>
import { SearchIcon, ChevronUpIcon, ViewGridIcon, ViewListIcon, PlusSmIcon } from "@vue-hero-icons/solid";
export default {
  name: "FiltersBar",
  components: {
    SearchIcon, ChevronUpIcon, ViewGridIcon, ViewListIcon, PlusSmIcon
  },
}
</script>

<style>
</style>
