<template>
  <svg class="svg-icon"
       aria-hidden="true"
       v-on="$listeners">
    <use :xlink:href="iconName" />
  </svg>
</template>

<script>

export default {
  name: 'SvgIcon',
  props: {
    iconClass: {
      type: String,
      required: true,
    }
  },
  computed: {
    iconName () {
      return `#icon-${this.iconClass}`
    },
    svgClass () {
      if (this.className) {
        return 'svg-icon ' + this.className
      } else {
        return 'svg-icon'
      }
    },

  },
}
</script>

<style scoped>
.svg-icon {
  width: 20px;
  height: 20px;
  vertical-align: -4px;
}
</style>