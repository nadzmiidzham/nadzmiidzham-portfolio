<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { ChevronUpIcon } from "@heroicons/vue/20/solid";
</script>

<template>
  <div class="w-full px-4 pt-16">
    <div class="mx-auto w-full max-w-md rounded-2xl bg-white p-2">
      <Disclosure v-slot="{ open }">
        <DisclosureButton
          class="flex w-full justify-between rounded-lg bg-purple-100 px-4 py-2 text-left text-sm font-medium text-purple-900 hover:bg-purple-200 focus:outline-none focus-visible:ring focus-visible:ring-purple-500/75"
        >
          <span>Bachelor</span>
          <ChevronUpIcon
            :class="open ? 'rotate-180 transform' : ''"
            class="h-5 w-5 text-purple-500"
          />
        </DisclosureButton>

        <DisclosurePanel class="px-4 pb-2 pt-4 text-sm text-gray-500">
          <h3><b>UiTM Shah Alam</b> (<u>Selangor, Malaysia</u>)</h3>
          <p>Bachelor in Computer Science (Hons.)</p>
        </DisclosurePanel>
      </Disclosure>

      <Disclosure as="div" class="mt-2" v-slot="{ open }">
        <DisclosureButton
          class="flex w-full justify-between rounded-lg bg-purple-100 px-4 py-2 text-left text-sm font-medium text-purple-900 hover:bg-purple-200 focus:outline-none focus-visible:ring focus-visible:ring-purple-500/75"
        >
          <span>Diploma and O-Level</span>
          <ChevronUpIcon
            :class="open ? 'rotate-180 transform' : ''"
            class="h-5 w-5 text-purple-500"
          />
        </DisclosureButton>

        <DisclosurePanel class="px-4 pb-2 pt-4 text-sm text-gray-500">
          <h3><b>UiTM Merbok</b> (<u>Kedah, Malaysia</u>)</h3>
          <p>Diploma in Computer Science</p>

          <h3><b>Royal Military College</b> (<u>Selangor, Malaysia</u>)</h3>
          <p>O-Level</p>
        </DisclosurePanel>
      </Disclosure>
    </div>
  </div>
</template>
