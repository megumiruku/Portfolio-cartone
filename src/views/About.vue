<template>
  <div class="about flex">
    <Header />
    <div class="profile">
      <div class="flex">
        <img src="../assets/profile-pic.jpg" alt="プロフィール写真" class="profile-img"/>
        <div class="content">
          <div class="content-eng">
            <h2 class="name">Cartone Geatno</h2>
            <p>1988 Born in Giulianova,Italy</p>
            <p>2013 Graduated Istituto Italiano di Fotografia in Milano</p>
            <p class="indent">2013 Worked as assistant of Sonny Vandevelde,Alessandro Dealberto,Nicola serafini and Lior Susana. </p>
            <p class="indent">2014 Started working specialized in fashion and Portrait Photography</p>
          </div>
          <div class="content-jap">
            <h2 class="name">ガエタノ カルトネ</h2>
            <p>1988 イタリア ジュリアノ‐ヴァ生まれ</p>
            <p>2013 ミラノの写真学校 Istituto Italiano di Fotografia を卒業</p>
            <p class="indent">2013 イタリアの有名な写真家、ニコラ・セラフィー二、リオール・スザナのアシスタントを務める</p>
            <p>2014 ファッションやポートレート写真を主に活動を開始
            </p>
          </div>
        </div>
      </div>
      <div class="clients">
        <h2 class="clients-ttl">Works and Clients</h2>
        <p class="clients-eng">VOGUE.DE (web), ZINK Magazine (usa), Kaltblut Magazine (ger), Zodiac Magazine (nl), Unfolded Magazine (uk), Institute Magazine, Rude Magazine (spa), Superior Magazine (ger), Sicky Magazine (spa), Eclectic Magazine (fra),  Elléments Magazine (usa), Mint Magazine, Indie Magazine (aut), Fashiongrunge Magazine (usa), Van Der Love Magazine, InCover Magazine (spa), Impostor Magazine (usa),Trend Prive Magazine (usa), Slang Magazine</p>
        <p class="clients-jap">株式会社Conde`Nast (VOGUE.DE), 株式会社Start Today (ZOZOTOWN), 株式会社B４F (Milleporte), 株式会社GLADD (Glamour Sales), 株式会社Abraham K Hangul, 株式会社エムアップ (Roen), 株式会社Modamania Japan, 株式会社AYURA (Plain Clothing), 株式会社Pampaloni, 株式会社Viviano Sue Couture,  株式会社Chiral, 株式会社Lalu, Fee Tokyo, Sho Sakota, Capuano, 株式会社Rinkan, 株式会社Atelier Polline, 株式会社Anna Galaganenko, Hope Milano, Sonia Galiano, The Eye Society, Vicky Griva, Chikuma Koyama for Wella Itva, E.G</p>
      </div>
      <img class="clients-img" src="../assets/clients.jpg" alt="クライアント">
    </div>
  </div>
</template>

<script>
import Header from "../components/Header";

export default {
  components: {
    Header,
  }
}
</script>

<style scoped>
.about {
  width: 80%;
  margin: 0 auto;
}
.profile {
  padding-top:25px;
  width: 80%;
}
.profile-img {
  padding-top: 20px;
}
.flex {
  display: flex;
  justify-content: center;
  align-items:flex-start;
}
.content {
  text-align: left;
  margin-left: 30px;
  width:50%;
}
.name {
  padding-bottom: 10px;
}
.content p {
  text-indent: -2.5em;
  padding-left: 2.5em;
}
.content-eng {
  margin-bottom: 10%;
  font-family:serif;
  line-height: 1.2em;
}
.content-jap {
  font-size: 15px;
  line-height:1.2em;
  font-family: Georgia, 'Times New Roman', Times, serif;
}
.clients {
  width: 90%;
  margin: 50px auto;
}
.clients-ttl {
  text-align: center;
  font-size: 1.3rem;
}
.clients-eng {
  margin: 30px 0;
  font-family: serif;
  font-size:0.9rem;
  line-height: 1.5rem;
}
.clients-jap {
  font-family: Georgia, 'Times New Roman', Times, serif;
  font-size: 0.8rem;
  line-height: 1.5rem;
}
.clients-img {
  display: block;
  width: 70%;
  margin: 0 auto;
}
@media screen and (max-width: 767px) {
  .flex {
    display: block;
  }
  .about,
  .profile {
    width: 100%;
  }
  .profile-img {
    display: block;
    margin: 0 auto;
    padding: 0;
  }
  .content {
    width: 90%;
    margin: 20px auto;
  }
  .name {
    text-align: center;
    padding-top: 5px;
    padding-bottom: 20px;
  }
  .content-jap {
    font-size: 14px;
  }
  .clients {
    width: 90%;
    margin: 0 auto;
    margin-top: 50px;
    margin-bottom: 10px;
  }
  .clients-eng {
  font-size:0.8rem;
  line-height: 1.3rem;
  }
  .clients-jap {
  font-size: 0.7rem;
  line-height: 1.4rem;
  }
.clients-img {
  display: block;
  width: 90%;
  margin: 20px auto;
}





}
</style>