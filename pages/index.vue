<template>
  <section class="container">
    <script src="https://cdn.jsdelivr.net/gh/GrabzIt/grabzit@js-3.2.9.4/javascript/grabzit.min.js"></script>
    <header>
      <app-logo/>
      <h1 class="utitle">
        <h2>p_status</h2>
      <h4 class="subtitle">
        Interface Status for all projects
      </h4>
      </h1>
    </header>
  <div class="main">
    <item 
    v-for="item in items" :key="item.id"
    :siteImage="item.siteImage" 
    :siteTitle="item.siteTitle"
      :id="item.id" 
      :siteDescrition="item.siteDescrition"
       />

  </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

import Item from '@/components/Item'

export default {
  components: {
    AppLogo,
    Item
  },

        props: ['siteTitle', 'siteDescrition', 'siteImage'],

  asyncData(){
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          items: [
            {
              id: "1",
              siteTitle: "Google",
              siteDescrition: "Google Google Google",
              siteImage: "http://127.0.0.1:8887/google.png"
            },
            {
              id: "2",
              siteTitle: "Twitter",
              siteDescrition: "Twitter Twitter Twitter",
              siteImage: "http://127.0.0.1:8887/twitter.png"
            },
            {
              id: "3",
              siteTitle: "Github",
              siteDescrition: "Github Github Github",
              siteImage: "http://127.0.0.1:8887/github.png"
            }
          ]
        })
      }, 1500)
    })
  }
};
GrabzIt("NmI3ZGU4ZGI5NTEzNGFjZWE5Y2JjMWNjMzZkOGY4Y2U=").ConvertURL("http://www.google.com", 
{"bwidth":1024,"bheight":768,"width":195,"height":146}).Create();
</script>

<style>
.container{
  margin:0;
  padding: 10px;
  border: 3px solid gray;
  min-height: 100vh;
}
header {
  /*min-height: 100vh;*/
  display: flex;
  justify-content: left;
  align-items: left;
  text-align: left;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: absolute;
  font-weight: 300;
  /* font-size: 100px; */
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  /* font-size: 42px; */
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.main{
  margin: 10px;
  background-color: #35495e;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

    .recipe {
        box-sizing: border-box;
        width: 280px;
        padding: 8px;
        border: 1px solid #ccc;
        box-shadow: 0 2px 2px #aaa;
    }
    
    .thumbnail {
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 200px;
    }
</style>
