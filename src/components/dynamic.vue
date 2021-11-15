<template>
<p>hai</p>
    <b-breadcrumb>
        <b-breadcrumb-item v-for="(item, index) in breadList" :key="index" :active="!(item.name !== name && index !== 1)">
          <router-link
            v-if="item.name !== name"
            :to="{ path: item.path === '' ? '/' : item.path }"
          >{{ item.meta.title }}</router-link>
          <span v-else>{{ item.meta.title }}</span>
        </b-breadcrumb-item>
      </b-breadcrumb>
    </template>
    
    <script>
    export default {
      data () {
        return {
          name: '',
          hash: '',
          breadList: []
        }
      },
      created () {
        this.getBreadcrumb()
      },
      methods: {
        getBreadcrumb () {
          this.breadList = []
          this.hash = this.$route.hash
          
          this.$route.matched.forEach(item => {
            if (item.name) {
              if (item.name === "CharDBManage") {
                item.query = { bar: 'datasheet' }
              }
              this.breadList.push(item)
            }
          })
          if (this.hash.includes('#')) {
            let lst = this.hash.split('#')
            let hashItems = []
            if (lst.length < 7) {
              lst.forEach(e => {
              if(e !== '') {
              hashItems.push(e)
              let item = {
                name: e.includes('-') ? e.split('-')[1] : e,
                path: `${this.$route.path}#${hashItems.join('#')}` ,
                meta: {
                  title: e.includes('-') ? e.split('-')[1].replace(/%20/g, ' ') : e.replace(/%20/g, ' ')
                }
              }
              this.breadList.push(item)
            }
          })
        }
      }
      this.name = this.breadList[this.breadList.length - 1].name
    }
  },
  watch: {
    $route () {
      this.getBreadcrumb()
    }
  }
}
</script>