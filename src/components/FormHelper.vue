<template>
        <v-container>
            <v-main>
                 <div>
                     <h1>Please fill out the form...!</h1>
                     <form>                         
                         <div id="form-header">
                            <slot name="form-header"></slot>
                         </div>
                         <div id="form-fields">
                            <slot name="form-fields"></slot>
                         </div>
                         <div id="form-controls">
                            <slot name="form-controls"></slot>
                         </div>
                         <div id="useful-links">
                              <ul>
                                <li><a href="#">Link 1</a></li>
                                <li><a href="#">Link 2</a></li>
                                <li><a href="#">Link 3</a></li>
                                <li><a href="#">Link 4</a></li>
                              </ul>
                         </div>
                     </form>
                 </div>
            </v-main>
        </v-container>
</template>

<script>
export default {
       name:'FormHelper',


}
</script>

<style scoped>
   h1{
    text-align: center;
   }

   form{
    width: 100%;
    max-width: 960px;
    margin: 0 auto;
   }

   #useful-links ul{
    padding: 0;
   }

   #useful-links li{
    display: inline-block;
    margin-right: 10px;
   }
  
   form >div{
    padding: 20px;
    background: #eee;
    margin: 20px o;
   }

   #form-header{
    background-color: #ddd;
    border: 1px solid #bbb;
   }

</style>