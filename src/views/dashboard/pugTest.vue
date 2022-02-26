<template lang='pug'>
div
  a(href='http://www.baidu.com') 百度
  |
  |
  a.button(href='http://www.baidu.com') 百度
  |
  |
  a.button(href='http://www.baidu.com') background
  input(type='text', placeholder='123')

  div
    button(@click='btn') 点击
  div
  - var url = "www.bilibili.com/"
    a(href="https://" + url, target='_blank') 哔哩哔哩

  - let friend = 8
  case friend
    when 0
    when 1
      p 您的朋友太少了
    default
      p 您有 #{ friend } 个朋友
  hr
  - for (let i = 0; i < 3; i++)
    li 我爱单车

  -
    let list = ['苏和扬', '单车']
  each item in list
    li= item
</template>

<script>
export default {
  data () {
    return {
      name: '苏和扬',
      url: 'www.bilibili.com/'
    }
  },
  methods: {
    btn () {
      console.log('aaa')
    }
  }
}
</script>

<style lang="less" scoped>
.container {
  font-size: 40px;
}
</style>
