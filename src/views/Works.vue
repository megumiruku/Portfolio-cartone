<template>
  <div class="works flex">
    <Header />
    <div class="gallery">
      <div class="images" v-for="(item) in images" :key="item">
        <div class="card">
          <img :src="item.src" @click="openModal(item)" alt="作品の写真" />
          <p class="ttl">{{item.ttl}}</p>
        </div>
        <WorksModal :val="postItem" v-show="showContent" @close="closeModal" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import WorksModal from '../components/WorksModal'

export default {
  data() {
    return {
      showContent: false,
      postItem: "",
      images : [
        {
          src:require("../assets/WORK/1.Pagine_da_RUDEMagazine.jpg"),
          ttl:"Japanese bliss"
        }, 
        {
          src:require("../assets/WORK/2.traintedlove_medie-206.jpg"),
          ttl:"Love"
        }, 
        {
          src:require("../assets/WORK/3.TOKYONEON 41_jpg.jpg"),
          ttl:"Tokyo Neon"
        }, 
        {
          src:require("../assets/WORK/4. jaxss8.jpg"),
          ttl:"Frida"
        }, 
        {
          src:require("../assets/WORK/5.Screenshot.jpg"),
          ttl:"Holy Grace"
        }, 
        {
          src:require("../assets/WORK/6.cabinet.jpg"),
          ttl:"いろ IRO"
        }, 
        {
          src:require("../assets/WORK/7.FASHION_GUN.jpg"),
          ttl:"Rubik's Cube"
        }, 
        {
          src:require("../assets/WORK/8.oneday.jpg"),
          ttl:"One day"
        }, 
        {
          src:require("../assets/WORK/9.kabuki.jpg"),
          ttl:"Kabuki"
        }, 
        {
          src:require("../assets/WORK/10.Metamorphosis.jpg"),
          ttl:"Metamorphosis"
        }, 
        {
          src:require("../assets/WORK/11.floral.jpg"),
          ttl:"Floral"
        }, 
        {
          src:require("../assets/WORK/12.serenad.jpg"),
          ttl:"Serenade"
        }, 
        {
          src:require("../assets/WORK/13.air.jpg"),
          ttl:"AIR"
        }, 
        {
          src:require("../assets/WORK/14.sweetdance.jpg"),
          ttl:"Sweet Dance"
        }, 
        {
          src:require("../assets/WORK/15MirroronTheWall.jpg"),
          ttl:"Mirror"
        }, 
        {
          src:require("../assets/WORK/16.marbel.jpg"),
          ttl:"Marble"
        }, 
        {
          src:require("../assets/WORK/17.untitledcolors.jpg"),
          ttl:"Untitled Colors"
        }, 
        {
          src:require("../assets/WORK/18.sicklove_medie.jpg"),
          ttl:"Love Sick"
        }, 
        {
          src:require("../assets/WORK/19.sporty.jpg"),
          ttl:"Sporty"
        }, 
        {
          src:require("../assets/WORK/20.INSOMNIA_.jpg"),
          ttl:"Insomnia"
        }, 
        {
          src:require("../assets/WORK/21.wildchild.jpg"),
          ttl:"Wild Child"
        }, 
        {
          src:require("../assets/WORK/22.Fashion_13_jpg1.jpg"),
          ttl:"Ironheart"
        }, 
        {
          src:require("../assets/WORK/23vogue.jpg"),
          ttl:"Vogue"
        }, 
        {
          src:require("../assets/WORK/24.nowhere.jpg"),
          ttl:"Nowhere"
        }, 
        {
          src:require("../assets/WORK/25.Abraham_highRes41.jpg"),
          ttl:"ECDYSIS"
        }, 
        {
          src:require("../assets/WORK/26.ametsubi_extra-54.jpg"),
          ttl:"Blind & Imagined"
        }, 
        {
          src:require("../assets/WORK/27.chiral.jpg"),
          ttl:"Chiral"
        }, 
        {
          src:require("../assets/WORK/28.house.jpg"),
          ttl:"House of Viviano"
        }, 
        {
          src:require("../assets/WORK/29.dresscamp.jpg"),
          ttl:"Dresscamp"
        }, 
        {
          src:require("../assets/WORK/30.smoking.jpg"),
          ttl:"E.G."
        }, 
        {
          src:require("../assets/WORK/31.yay.jpg"),
          ttl:"YaY"
        }, 
        {
          src:require("../assets/WORK/32.make-up.jpg"),
          ttl:"Style Make-up"
        }, 
        {
          src:require("../assets/WORK/33.sara.jpg"),
          ttl:"Sara Deli Castelli"
        }, 
        {
          src:require("../assets/WORK/34.fee.jpg"),
          ttl:"FEE"
        }, 
        {
          src:require("../assets/WORK/35.dress.jpg"),
          ttl:"Sonia Galiano 2014"
        }, 
        {
          src:require("../assets/WORK/36.modern.jpg"),
          ttl:"Modamania Japan"
        }, 
        {
          src:require("../assets/WORK/37.The-Space-Invaders.jpg"),
          ttl:"Saya for Eye Society"
        }, 
        {
          src:require("../assets/WORK/38.HOPEmilan.jpg"),
          ttl:"HOPE"
        }, 
        {
          src:require("../assets/WORK/39.eye.jpg"),
          ttl:"The Eye Society"
        }, 
        {
          src:require("../assets/WORK/40.annaGalaganenko.jpg"),
          ttl:"Anna Galaganenko"
        }, 
        
      ]
    };
  },
  components: { 
    Header,
    WorksModal,
  },
  methods: {
    openModal(item) {
      this.showContent = true;
      this.postItem = item;
    },
    closeModal() {
      this.showContent = false;
    }
  }
}
</script>

<style scoped>
.works {
  width: 80%;
  margin: 0 auto;
}
.flex {
  display: flex;
  justify-content: center;
}
.gallery {
  width: 100%;
  padding-top:25px;
  display: flex; 
  flex-wrap: wrap;
  justify-content: center;
}
.images {
  width: 23%;
  margin: 5px;
}
.gallery img {
  width: 95%;
  vertical-align: bottom;
}
.gallery img:hover {
  opacity: 0.7;
  cursor: pointer;
}
.ttl {
  color: #333;
  font-size: 11px;
  text-align: center;
  padding-bottom: 5px;
}
@media screen and (max-width: 767px) {
  .works {
    width: 100%;
  }
  .flex {
    display: block;
  }
}
</style>