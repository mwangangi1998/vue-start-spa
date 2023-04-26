<template>
       
       <nav class="navbar navbar-inverse ">
                     <div class="container-fluid">
                       <div class="navbar-header">
                         <a class="navbar-brand" V-bind:href=" ">MyVueApp</a>
                       </div>
                       <ul class="nav navbar-nav">
                         <li v-for="(page , index) in pages" class="nav-item" 
                         
                         :key="index">
                             <a 
                             :class="{active: activePage==index}"
                             :href="page.link.url"
                             :title="`This link goes to ${page.link.text  }`"
                             @click.prevent="navLinkClick(index)"
                             >{{ page.link.text }}</a></li>
                        
                       </ul>
                       
                     </div>
                   </nav> 
</template>
<script>
export default{
    props: ['pages', 'activePage', 'navLinkClick'],
          

}
</script>