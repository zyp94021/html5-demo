<template>
  <aside id="sidebar">
    <ul>
      <li v-for="data in nav">
        <router-link :to="data.href">{{data.name}}</router-link>
        <ul>
          <li v-for="item in data.items">
            <router-link :to="data.href+item.hash">{{item.name}}</router-link>
          </li>
        </ul>
      </li>
    </ul>
  </aside>
</template>
<script>
  export default {
    name: 'Sidebar',
    data() {
      return {
        nav: [
          {
            name: '视频',
            href: '/video',
            items: [
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              }
            ]
          },
          {
            name: '视频',
            href: '/video',
            items: [
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              }
            ]
          },
          {
            name: '视频',
            href: '/video',
            items: [
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              },
              {
                name: '标签',
                hash:'#tag'
              }
            ]
          },
        ]
      }
    }
  }
</script>
<style lang="scss">
  #sidebar {
    position: fixed;
    top:0px;
    bottom:0px;
    width: 340px;
    overflow-y: auto;
    ul {
      list-style: none;
    }
  }
</style>
