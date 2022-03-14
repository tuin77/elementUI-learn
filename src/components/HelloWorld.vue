<template>
  <div>
    <e-button>默认按钮</e-button>
    <e-button type="primary">主要按钮</e-button>
    <e-button type="success">成功按钮</e-button>
    <e-button type="info">信息按钮</e-button>
    <e-button type="warning">警告按钮</e-button>
    <e-button type="danger">危险按钮</e-button>
    <input type="text" class="input-name">
  </div>
</template>
<script>
import eButton from './button.vue';
export default {
  components: { eButton },
  data() {
    return { active: 2 };
  },
  methods: {
  },
};
</script>
<style lang="scss">
.input-name{
  
}
</style>
