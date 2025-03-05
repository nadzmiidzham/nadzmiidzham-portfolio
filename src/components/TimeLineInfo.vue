<template>
  <div class="flex flex-col gap-2">
    <div class="flex flex-row text-white gap-3">
      <div class="bg-green-900 px-3 py-2 rounded-xl">
        <b>
          <slot name="time" class="uppercase"></slot>
        </b>
      </div>
      <div class="bg-green-900 px-3 py-2 rounded-xl">
        <b>
          <slot name="label" class="uppercase"></slot>
        </b>
      </div>
    </div>
    <div class="bg-yellow-200 ml-10 p-1 rounded-md outline outline-yellow-600">
      <slot name="description"></slot>
    </div>
  </div>
</template>
