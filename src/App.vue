<template>
  <Form :schemas="schemas"></Form>
  <Icon icon="octicon:file-submodule"></Icon>
</template>

<script lang="ts">
import { defineComponent,ref } from 'vue'
import Form from '/@/components/Form/form'
import Icon from '/@/components/Icon/icon'

export default defineComponent({
  name: 'App',
  components:{
    Form,
    Icon
  },
  setup() {
    const schemas = ref([
            {
                key: '用户名称',
                label: '用户名称',
                component: 'Input'
            },
            { key: 'companyName', label: '客户名称', component: 'Input', slots: { prefix: () => '$' } },
            { key: 'socialCreditCode', label: '信用代码', component: 'Input' }
        ])
      return {
        schemas
      }
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>