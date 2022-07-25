<template>
     <v-main>
            <div v-for="slot in slotsData" :key="slot.id" class="main">
                 <!-- <p> {{slot.username}} & {{slot.lastname}} </p> -->
                 <slot :username="slot.username" :lastname='slot.lastname'></slot>
            </div>
    </v-main>
</template>

<script>
export default {
    name:'SlotsProps',
    data(){
        return{
            slotsData:[
                {id: 1,
                 name: "Leanne Graham",
                 username: "Bret",
                 lastname:'Chris',
                 email: "Sincere@april.biz"},
                 {id: 2,
                 name: "Ervin Howell",
                 username: "Antonette",
                 lastname:'Hemsworth',
                 email: "Shanna@melissa.tv"},
                 {id: 3,
                 name: "Clementine Bauch",
                 username: "Samantha",
                 lastname:'Smith',
                 email: "Nathan@yesenia.net"}
            ]
        }
    }

}
</script>

<style scoped>

  .slotsData{
    justify-content: center;
    align-items: center;
  }

</style>