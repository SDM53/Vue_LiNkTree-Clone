<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  url: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    default: 'Need Text Here',
  },
})
</script>

<template>
  <a
    :href="url"
    target="_blank"
    rel="noopener noreferrer"
    class="group relative flex w-full items-center gap-4 rounded-xl border border-blue-400 bg-blue-200 p-4 shadow-lg shadow-blue-400/90 transition-all duration-200 hover:scale-[1.05] hover:border-blue-50 hover:shadow-xl hover:shadow-blue-100/90"
  >
    <!-- Icon -->
    <div
      class="item center round-lg group-hover:blue-600/90 flex h-12 w-12 shrink-0 justify-center bg-blue-100 text-blue-400 transition-all duration-200 group-hover:scale-120 group-hover:bg-blue-400 group-hover:text-blue-100 group-hover:shadow-xl group-hover:shadow-blue-500/40"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        class="h-10.5 w-10.5 transition-transform duration-200 group-hover:rotate-10"
      >
        <!-- Icon from SVG Spinners by Utkarsh Verma - https://github.com/n3r4zzurr0/svg-spinners/blob/main/LICENSE -->
        <rect
          width="10"
          height="10"
          x="1"
          y="1"
          fill="currentColor"
          rx="1"
        >
          <animate
            id="SVG7WybndBt"
            fill="freeze"
            attributeName="x"
            begin="0;SVGo3aOUHlJ.end"
            dur="0.2s"
            values="1;13"
          />
          <animate
            id="SVGVoKldbWM"
            fill="freeze"
            attributeName="y"
            begin="SVGFpk9ncYc.end"
            dur="0.2s"
            values="1;13"
          />
          <animate
            id="SVGKsXgPbui"
            fill="freeze"
            attributeName="x"
            begin="SVGaI8owdNK.end"
            dur="0.2s"
            values="13;1"
          />
          <animate
            id="SVG7JzAfdGT"
            fill="freeze"
            attributeName="y"
            begin="SVG28A4To9L.end"
            dur="0.2s"
            values="13;1"
          />
        </rect>
        <rect
          width="10"
          height="10"
          x="1"
          y="13"
          fill="currentColor"
          rx="1"
        >
          <animate
            id="SVGUiS2jeZq"
            fill="freeze"
            attributeName="y"
            begin="SVG7WybndBt.end"
            dur="0.2s"
            values="13;1"
          />
          <animate
            id="SVGU0vu2GEM"
            fill="freeze"
            attributeName="x"
            begin="SVGVoKldbWM.end"
            dur="0.2s"
            values="1;13"
          />
          <animate
            id="SVGOIboFeLf"
            fill="freeze"
            attributeName="y"
            begin="SVGKsXgPbui.end"
            dur="0.2s"
            values="1;13"
          />
          <animate
            id="SVG14lAaeuv"
            fill="freeze"
            attributeName="x"
            begin="SVG7JzAfdGT.end"
            dur="0.2s"
            values="13;1"
          />
        </rect>
        <rect
          width="10"
          height="10"
          x="13"
          y="13"
          fill="currentColor"
          rx="1"
        >
          <animate
            id="SVGFpk9ncYc"
            fill="freeze"
            attributeName="x"
            begin="SVGUiS2jeZq.end"
            dur="0.2s"
            values="13;1"
          />
          <animate
            id="SVGaI8owdNK"
            fill="freeze"
            attributeName="y"
            begin="SVGU0vu2GEM.end"
            dur="0.2s"
            values="13;1"
          />
          <animate
            id="SVG28A4To9L"
            fill="freeze"
            attributeName="x"
            begin="SVGOIboFeLf.end"
            dur="0.2s"
            values="1;13"
          />
          <animate
            id="SVGo3aOUHlJ"
            fill="freeze"
            attributeName="y"
            begin="SVG14lAaeuv.end"
            dur="0.2s"
            values="1;13"
          />
        </rect>
      </svg>
    </div>

    <!-- Text -->
    <div class="min-w-0 flex-1">
      <h3 class="truncate font-display font-semibold text-blue-500">{{ title }}</h3>
      <p class="test-sm truncate text-blue-400">{{ description }}</p>
    </div>

    <!-- Hover Glow Effect -->
    <div
      class="absolute inset-0 rounded-xl bg-linear-to-r from-blue-50/50 via-blue-400/20 to-blue-50/50 opacity-0 transition-opacity group-hover:opacity-100"
    />
  </a>
</template>
