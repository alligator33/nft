<template>
  <div>
    <div
      style="height: 96%"
      class="absolute right-8 top-4 w-96 rounded-lg bg-white text-gray-900 shadow-lg dark:bg-secondary-900 dark:text-white"
    >
      <div>
        <button
          @click="useModalStore().hideModal()"
          class="absolute right-6 top-6"
        >
          <i class="fa-light fa-arrow-right-to-line text-2xl"></i>
        </button>
        <div class="space-y-4 pl-4 pt-4 text-2xl font-semibold">
          <NuxtLink
            :to="{ name: 'explore' }"
            class="block hover:text-primary-500"
            @click="useModalStore().hideModal()"
          >
            Marketplace<i class="fa-solid fa-store pl-4 text-primary-700"></i>
          </NuxtLink>
          <NuxtLink
            @click="useModalStore().hideModal()"
            :to="{ name: 'howItWorks' }"
            class="block hover:text-primary-500"
          >
            How it Works
          </NuxtLink>

          <NuxtLink
            @click="useModalStore().hideModal()"
            :to="{ name: 'about' }"
            class="block hover:text-primary-500"
          >
            About
          </NuxtLink>
          <NuxtLink
            @click="useModalStore().hideModal()"
            to="/blog"
            class="block hover:text-primary-500"
          >
            Blog
          </NuxtLink>
          <div class="flex flex-col space-y-8">
            <NuxtLink @click="useModalStore().hideModal()" to="/login">
              Sign In
              <i class="fa-duotone fa-right-to-bracket"></i>
            </NuxtLink>
          </div>
        </div>
      </div>
      <div class="absolute bottom-0 w-full">
        <div id="footer">
          <div class="flex">
            <NuxtLink
              @click="useModalStore().hideModal()"
              to="/signup"
              class="btn1 mx-4 w-full text-center"
            >
              Get Started
              <i class="fa-sharp fa-solid fa-user-plus"></i>
            </NuxtLink>
          </div>
          <div class="border-b pt-2"></div>
          <div class="flex justify-between px-4 py-4">
            <div>
              <i class="fa-brands fa-instagram"></i>
              <a :href="appStore.appConfigData.instagram_url"></a>
            </div>
            <div>
              <i class="fa-brands fa-facebook">
                <a :href="appStore.appConfigData.facebook_url"></a>
              </i>
            </div>
            <div>
              <i class="fa-brands fa-twitter">
                <a :href="appStore.appConfigData.twitter_url"></a>
              </i>
            </div>
            <div>
              <i class="fa-brands fa-telegram">
                <a :href="appStore.appConfigData.telegram_url"></a>
              </i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useModalStore } from "~/store/appStore";
import { useAppStore } from "~/store/appStore";

const appStore = useAppStore();
</script>

<style scoped></style>
