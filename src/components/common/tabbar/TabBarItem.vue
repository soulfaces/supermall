<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="isActive">
      <slot name="slot-icon"></slot>
    </div>
    <div v-else>
      <slot name="slot-icon-active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="slot-text"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "tab-bar-item",
    props: {
      path: String,
      activeColor: {
        type: String,
        default: '#f00'
      }
    },
    data(){
      return {}
    },
    computed: {
      isActive() {
        return this.$route.path.indexOf(this.path)
      },
      activeStyle(){
        return this.isActive? {} : {color: this.activeColor}
      }
    },
    methods: {
      itemClick() {
        this.$router.replace(this.path)
        document.title = this.$route.matched[0].meta
      }
    }
  };
</script>

<style scoped>
  .tab-bar-item {
    font-size: 12px;
    flex: 1;
    text-align: center;
  }

  .tab-bar-item img {
    width: 22px;
    height: 22px;
    margin-top: 5px;
  }

</style>
