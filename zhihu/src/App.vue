<template>
  <div class="container">
    <global-header :user="currentUser"></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'
import GlobalHeader, { UserProps } from './components/GlobalHeader.vue'

const currentUser: UserProps = {
  isLogin: true,
  name: 'viking'
}
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test专栏',
    description: '简介',
    avatar: 'https://img0.baidu.com/it/u=1431034659,526231739&fm=253&fmt=auto&app=138&f=JPEG?w=640&h=360'
  },
  {
    id: 2,
    title: 'test专栏',
    description: '简介',
    avatar: 'https://img0.baidu.com/it/u=1431034659,526231739&fm=253&fmt=auto&app=138&f=JPEG?w=640&h=360'
  },
  {
    id: 3,
    title: 'test专栏',
    description: '简介'
    // avatar: 'https://img0.baidu.com/it/u=1431034659,526231739&fm=253&fmt=auto&app=138&f=JPEG?w=640&h=360'
  },
  {
    id: 4,
    title: 'test专栏',
    description: '简介',
    avatar: 'https://img0.baidu.com/it/u=1431034659,526231739&fm=253&fmt=auto&app=138&f=JPEG?w=640&h=360'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList,
    GlobalHeader
  },
  setup () {
    return {
      list: testData,
      currentUser
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
