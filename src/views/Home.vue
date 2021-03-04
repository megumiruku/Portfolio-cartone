<template>
  <div class="home flex">
    <Header />
    <div class="grid">
      <div class="header-img" v-for="(item) in images" :key="item">
        <div class="card">
          <img :src="item.src" @click="openModal(item)" alt="作品の写真" />
        </div>
        <HomeModal :val="postItem" v-show="showContent" @close="closeModal" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header'
import HomeModal from '../components/HomeModal'

export default {
  data() {
    return {
      showContent: false,
      postItem: "",
      images: [
        {
          src: require("../assets/HOME/43627-3967143-Ph_GaetanoCartone_ThisMeansWar_fashioneditorial05.jpg"),
        },
        {
          src: require("../assets/HOME/Ph.GaetanoCartone_KABUKI-72_g8etg8.jpg"),
        },
        {
          src: require("../assets/HOME/gaetanocartone_310.jpg"),
        },
        {
          src: require("../assets/HOME//Frida_ph.GaetanoCartone-22_xdkxg3.jpg"),
        },
        {
          src: require("../assets/HOME/Frida_ph.GaetanoCartone-48_igh3pe.jpg"),
        },
        {
          src: require("../assets/HOME/_MG_3668.jpg.jpg"),
        },
        {
          src: require("../assets/HOME/HolyGrace_ph_GaetanoCartone-19.jpg"),
        },
        {
          src: require("../assets/HOME/JapaneseBliss_Ph_GaetanoCartone-36.jpg"),
        }
      ]
    }
  },
  components: {
    Header,
    HomeModal,
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
};
</script>

<style scoped>
.home {
  width: 80%;
  margin: 10px auto;
  position: relative;
}
.flex {
  display: flex;
  justify-content: center;
}
.grid {
  display: grid;
  grid-template-columns: 200px 180px 220px 190px;
  grid-template-rows: 320px;
  width: 70%;
}
.header-img {
  margin:5px;
  padding:5px;
}
.header-img img {
  width: 100%;
}
.header-img img:hover {
  opacity: 0.7;
  cursor: pointer;
  box-shadow: 10px 10px 10px rgba(0,0,0,0.5);
  transform: translateY(-5px);
  transition-duration: 0.5s;
}

@media screen and (max-width: 767px) {
  .home {
    width: 100%;
  }
  .flex {
    display: block;
  }
  .grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 100%;
    margin-top: 5%;
  }
  .header-img{
    width: 40%;
  }
}
</style>
HomeModal