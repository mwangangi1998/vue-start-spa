<template>

<div>
    <nav-bar
    :pages="pages" 
    :activePage="activePage" 
    :nav-Link-Click="(index)=>activePage=index">
  </nav-bar>
  </div>
    <div class="container">
        <page-viewer :page="pages[activePage]">

        </page-viewer>

    </div>

</template>
<script>

import navbar from './components/navbar.vue';
import pageviewer from './components/pageviewer.vue';
export default{
components: {
  navbar,
  pageviewer
},
  data() {          
          return {
                    activePage: 0,
                    pages: [


                        {
                            link: { text: 'index', url: 'index.html' },
                            pageTitle: 'home page',
                            content: 'this is home page',
                        },
                        {
                            link: { text: 'about', url: 'about.html' },
                            pageTitle: 'About us',
                            content: 'this is about page',
                        },
                        {
                            link: { text: 'contact', url: 'contact.html' },
                            pageTitle: 'contact page',
                            content: 'this is contact page',
                        },
                    ],
                    message: 'Hello Vue!',
                    content: 'this is my first vue app'
                }
        }
  
}

</script>