<template>
  <!-- mobile view -->
  <a
    href="/documents/cv-manual-2025.pdf"
    class="text-white hover:text-yellow-300 md:hidden"
    download
  >
    <div
      class="rounded-2xl bg-yellow-500 px-3 py-2 text-center text-green-950 outline hover:bg-green-900 hover:text-yellow-500"
    >
      <b>Download My CV</b>
    </div>
  </a>

  <!-- desktop view -->
  <a
    href="/documents/cv-manual-2025.pdf"
    class="hidden text-white hover:text-yellow-300 md:block"
    download
  >
    <div
      class="rounded-2xl bg-green-900 px-3 py-2 text-center text-yellow-500 outline hover:bg-yellow-500 hover:text-green-950"
    >
      <b>Download My CV</b>
    </div>
  </a>
</template>
