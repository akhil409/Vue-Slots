<template>
     <v-main>
           <div class="card">
               <div class="card-header">
                    <slot name="header"></slot>   
               </div>
               <div class="card-content" id="img">
                    <slot name="default"></slot> 
               </div>
               <div class="card-footer">
                    <slot name="footer"></slot> 
               </div>
           </div>
     </v-main>
</template>

<script>
export default {

}
</script>

<style scoped>



</style>