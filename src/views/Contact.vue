<template>
  <div class="contact flex">
    <Header />
    <div class="form">
      <h2 class="section-ttl">Contact</h2>
      <form method="post"  @submit.prevent="sendContact()">
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" name="user_name"  v-model="name"/>
        </div>
        <div>
          <label for="mail">Email:</label>
          <input type="email" id="mail" name="user_mail" v-model="email" />
        </div>
        <div>
          <label for="tel">TEL:</label>
          <input type="tel" id="tel" name="user_tel" v-model="tel" maxlength="15" />
        </div>
        <div>
          <label for="msg">Message:</label>
          <textarea id="msg" name="user_message" v-model="msg"></textarea>
        </div>
        <div class="button-submit">
          <button class="button" >Send</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header.vue'

export default {
  data() {
    return {
      name: "",
      email: "",
      tel: "",
      msg: "",
    }
  },
  methods: {
    sendContact() {
      if(
        this.name == "" ||
        this.email == "" ||
        this.tel == "" ||
        this.msg == "" 
      ){
        alert("入力されていない項目があります")
      }else {
        this.name = "";
        this.email = "";
        this.tel = "" ;
        this.msg = "" ;
        alert("送信しました")
      }
    }
  },
  components: { 
    Header, 
  },
}
</script>

<style scoped>
.contact {
  width: 80%;
  margin: 0px auto;
}
.flex {
  display: flex;
  justify-content: center;
}
.form {
  width: 70%;
  margin-top: 20px;
}
.section-ttl {
  text-align: center;
}
form {
  width: 100%;
  margin: 50px auto;
  text-align: center;
}
label {
  display:inline-block;
  width: 25%;
  text-align: left;
}
input,
textarea {
  box-sizing: border-box;
  border: 1px solid #999;
  width: 65%;
}
input {
  margin-bottom: 25px;
  padding: 7px;
}
textarea {
  vertical-align: top;
  height: 200px;
}
.button{
  width: 25%;
  margin-top: 50px;
  text-align: center;
  padding: 10px 50px;
  font-size: 15px;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 2px;
  outline: none;
}
.button:hover {
  opacity: 0.8;
}

/* --------------
-----Responsive----
-------------- */

@media screen and (max-width: 768px) {
  .contact {
    width: 100%;
  }
  .flex {
    display: block;
  }
  .form {
    width: 95%;
    margin: 50px auto;
  }
  .section-ttl {
    font-size: 1.3rem;
  }
  form{
    width: 90%;
    margin-top: 30px;
    margin-bottom: 20px;
  }
  label {
    display: block;
    margin: 10px auto;
    width: 80%;
    text-align: center;
    font-size: 1rem;
  }
  input,
  textarea {
    width: 90%;
  }
  .button {
    width: 80%;
    margin-bottom: 20px;
  }
}
</style>