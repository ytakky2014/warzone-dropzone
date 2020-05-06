<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="center">
      <img src="@/assets/warzone.png" width="1024" height="500"/>
    </div>
    <div class="text-center">
      <v-btn x-large dark @click="generate">Button</v-btn>
    </div>
    <h2>{{ drop_zone }}</h2>
  </div>
</template>

<script>
export default {
  name: 'MW WarZone Drop Zone Generate',
  data () {
    return {
      msg: 'MW WarZone Drop Zone Generate',
      drop_zone: ''
    }
  },
  methods: {
    generate () {
      const dz = ['B5','B6','B7','C1','C2','C3','C4','C5','C6','C7','C8','D1','D2','D3','D4','D5','D6','D7','D8','E1','E2','E3','E4','E5','E6','E7','E8','F1','F2','F3','F4','F5','F6','F7','F8','G2','G3','G4','G5','G6','G7','G8','H2','H3','H4','H5','H6','H7','H8','I4','I5','I6','I7','I8','Named','Named']
      const nz = ['Dam','StorageTown','Airport','Superstore','Boneyard','Train Station','Promenade West','Promenade East','Hills','Millitary Base','TV Station', 'Hospital', 'Downtown','Park','Stadium','Quarry','Port','Prison','Farmland','Lumbar','Quarry']
      var tz = Math.floor(Math.random() * dz.length)
      this.drop_zone = dz[tz]
      if (this.drop_zone === 'Named') {
        tz = Math.floor(Math.random() * nz.length) 
        this.drop_zone = nz[tz]
      }
     
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
.center {
  text-align:center;
}
</style>