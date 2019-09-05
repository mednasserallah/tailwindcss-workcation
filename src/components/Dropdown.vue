<template>
  <div>
    <button
      @click="toggle"
      @focus="buttonHasFocus = true"
      @blur="buttonHasFocus = false"
      type="button"
      class="block focus:outline-none"
    >
      <slot name="trigger" :hasFocus="buttonHasFocus"></slot>
    </button>
    <div class="hidden" :class="{'sm:block' : isOpen}">
      <!-- Hack to close the dropdown when the user clicks away  -->
      <button
        @click="isOpen = false"
        type="button"
        class="fixed opacity-0 inset-0 h-full w-full z-30 bg-red-500 cursor-default"
      ></button>

      <div class="absolute z-40 right-0" :class="{'hidden': !isOpen}">
        <slot name="dropdown-items"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
      buttonHasFocus: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  },
  mounted() {
    const onEscape = e => {
      if (!this.isOpen || e.key !== "Escape") {
        return;
      }

      this.isOpen = false;
    };

    document.addEventListener("keydown", onEscape);

    this.$on("hook:destroyed", () => {
      document.removeEventListener("keydown", onEscape);
    });
  }
};
</script>

<style lang="scss" scoped>
</style>