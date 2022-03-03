<template>
  <div id="app">
    <div class="flex flex-col bg-gray-50 min-h-screen min-h-full">

      <Header />

      <FiltersBar />

      <main class="flex flex-col flex-1 min-h-full p-4 sm:p-5 pb-0 sm:pb-0">
        <!--  Selected filters-->
        <div class="selected-filters">
          <div class="bg-blue-50 text-xs py-2.5 px-3.5 inline-block rounded-lg">
            <span class="text-blue-500 mr-1">Client:</span>
            <span class="text-gray-700">Novartis</span>
            <XIcon class="inline ml-2 w-4 h-4 text-blue-400" />
          </div>
        </div>

        <!--      Columns-->
        <div class="columns">
          <div class="column">

            <AppBadge class="mb-4">En attente d’approbation</AppBadge>

            <div class="column-card">
              <p class="text-gray-600 mb-1">Master Service Agreement</p>
              <p class="text-gray-500 mb-1 text-xs font-normal">Modifié le Apr 23 ,2021</p>
              <p class="text-gray-700 mb-1 text-sm font-normal">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                et dolore magna aliqua. Ut enim ad minim veniam
              </p>

              <div class="column-card-footer">
                <UserAvatars />
              </div>
            </div>
          </div>
          <div class="column">
            <AppBadge class="mb-4" :color="'orange'">En cours de préparation</AppBadge>
            <div class="column-card">
              <p class="text-gray-600 mb-1">Master Service Agreement</p>
              <p class="text-gray-500 mb-1 text-xs font-normal">Modifié le Apr 23 ,2021</p>
              <p class="text-gray-700 mb-1 text-sm font-normal">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                et dolore magna aliqua. Ut enim ad minim veniam
              </p>

              <div class="column-card-footer">
                <UserAvatars />

                <div class="ml-auto">
                  <AppBadge :color="'gray'">
                    <ClockIcon class="w-4 h-4 mr-1 text-gray-900" /> 1 approbation(s)
                  </AppBadge>
                </div>
              </div>
            </div>
          </div>
          <div class="column">
            <AppBadge class="mb-4" :color="'purple'">En attente de signature</AppBadge>
            <div class="column-card">
              <p class="text-gray-600 mb-1">Master Service Agreement</p>
              <p class="text-gray-500 mb-1 text-xs font-normal">Modifié le Apr 23 ,2021</p>
              <p class="text-gray-700 mb-1 text-sm font-normal">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                et dolore magna aliqua. Ut enim ad minim veniam
              </p>

              <div class="column-card-footer">
                <UserAvatars />

                <div class="ml-auto">
                  <AppBadge :color="'red'">Click here to sign</AppBadge>
                </div>
              </div>
            </div>
            <div class="column-card">
              <p class="text-gray-600 mb-1">Master Service Agreement</p>
              <p class="text-gray-500 mb-1 text-xs font-normal">Modifié le Apr 23 ,2021</p>
              <p class="text-gray-700 mb-1 text-sm font-normal">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                et dolore magna aliqua. Ut enim ad minim veniam
              </p>

              <div class="column-card-footer">
                <UserAvatars />

                <div class="ml-auto">
                  <AppBadge :color="'gray'">
                    <ClockIcon class="w-4 h-4 mr-1 text-gray-900" /> 1 signature(s)</AppBadge>
                </div>
              </div>
            </div>
          </div>
          <div class="column">
            <AppBadge class="mb-4" :color="'green'">Effectif</AppBadge>
            <div class="column-card">
              <p class="text-gray-600 mb-1">Master Service Agreement</p>
              <p class="text-gray-500 mb-1 text-xs font-normal">Modifié le Apr 23 ,2021</p>
              <p class="text-gray-700 mb-1 text-sm font-normal">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                et dolore magna aliqua. Ut enim ad minim veniam
              </p>

              <div class="column-card-footer">
                <UserAvatars />

                <div class="ml-auto">
                  <AppBadge :color="'gray'">
                    <ClockIcon class="w-4 h-4 mr-1 text-gray-900" /> 22 jours restant(s)</AppBadge>
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
import Header from "@/components/Header";
import FiltersBar from "@/components/FiltersBar";
import { ClockIcon, XIcon } from "@vue-hero-icons/solid";
import UserAvatars from "@/components/UserAvatars";
import AppBadge from "@/components/AppBadge";

export default {
  name: 'App',
  components: {
    AppBadge,
    UserAvatars,
    Header,
    FiltersBar,
    XIcon, ClockIcon,
  }
}
</script>

<style>
.columns{
  @apply mt-4 flex flex-1 items-start overflow-x-auto;
}

.column{
  @apply w-96 pb-6 mr-4;
  min-width: 24rem;
}
.column-card{
  @apply bg-white rounded-lg shadow p-4 mb-4;
}

.column-card-footer{
  @apply flex items-center mt-4;
}

.bg-orange-100{
  background-color: rgb(255 237 213);
}
.text-orange-800{
  color: rgb(154 52 18);
}
</style>
