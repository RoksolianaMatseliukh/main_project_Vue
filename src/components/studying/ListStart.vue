<template>
  <div id="general">

     <h5 class="nameView"> <b> Go to other pages: </b> </h5>
     <ul>

        <router-link v-for="(page, index) in navigation"
                     :key="index"
                     :to='`/MyStudying${page.path}`'
                     tag="li"
                     class="cursor"> 
                     {{ page.name }} 
        </router-link > 

    </ul> 
        
  </div>
</template>

<script>
export default {
  name: 'ListStart',
  data() {
      return {
          navigation: [{path: '/program', name: 'Program'}, 
                       {path: '/learned', name: 'Learned'},
                       {path: '/calculator', name: 'Calculator'},
                       {path: '/todo_done_lists', name: 'Todo_Done_Lists'}]
      }
  }

}
</script>

<style scoped>

    #general {
        margin-top: 10px;
    }

    .nameView {
        color: rgb(18, 68, 92);
    }

    .cursor {
        cursor: pointer;
    }

</style>

