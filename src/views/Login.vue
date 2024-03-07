<template>
  <div id="sign_in">
    <div id="sign_in_card">
      <img class="logo_img" src="../assets/icons/logo_alone.png" alt="" />
      <h1 class="company_name">Medol</h1>
      <form @submit.prevent="handleSubmit()" action="">
        <input class="login-input" type="text" placeholder="login" v-model="username" />
        <input class="login-input" type="password" placeholder="parol" v-model="password" />
        <button class="login-btn">Kirish</button>

        <!-- <div class="form_links">
          <RouterLink to="/">Регистрация</RouterLink>
          <div></div>
          <RouterLink to="/">Забили парол?</RouterLink>
        </div> -->
      </form>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'
import Swal from 'sweetalert2'
// localStorage.removeItem('token')
// localStorage.removeItem('role')
// localStorage.removeItem('userId')
const username = ref('login')
const password = ref('parol')

function handleSubmit() {
  if (username.value == 'login' && password.value == 'parol') {
    location.href = '/home'
  } else {
    Swal.fire({
      icon: 'error',
      title: 'Login yoki parol xato'
    })
  }
  // axios
  //   .post('/token/', { username: username.value, password: password.value })
  //   .then((res) => {
  //     localStorage.setItem('token', res.data.token)
  //     localStorage.setItem('role', res.data.role)
  //     localStorage.setItem('userId', res.data.id)
  //     if (res.data.role == 'apteka') {
  //       location.href = '/filial'
  //     } else if (res.data.role == 'admin' || res.data.role == 'superadmin') {
  //       location.href = '/admin'
  //     } else {
  //       Swal.fire({
  //         icon: 'error',
  //         title: 'Login yoki parol xato'
  //       })
  //     }
  //   })
  //   .catch((err) => {
  //     Swal.fire({
  //       icon: 'error',
  //       title: 'Login yoki parol xato'
  //     })
  //     console.log(err.message)
  //   })
}
</script>
<style scoped lang="scss">
#sign_in {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 40px;
  padding: 30px 10px;
  background-color: $main_fon;
  background-image: url('../assets/img/login_fon.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
  @include media('<=LGdesktop') {
  }
  #sign_in_card {
    width: 500px;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 40px;
    padding: 50px 50px;
    // background-color: $kok;
    background-color: $kokhover;
    // background-color: #a11fb0;
    border-radius: 10px;
    .logo_img {
      height: 100px;
      filter: drop-shadow(0px 0px 10px #fff);
    }
    .company_name {
      font-size: 36px;
      font-weight: 600;
      color: #fff;
    }
    form {
      width: 100%;
      display: flex;
      flex-direction: column;
      gap: 20px;
      .login-input {
        appearance: none;
        width: 100%;
        padding: 13px 16px;
        border: none;
        background-color: $oq;
        border-radius: 5px;
        font-size: 15px;
        font-weight: 500;
        line-height: 1.4;
        color: var();
        transition:
          border 0.25s ease-in-out,
          color 0.25s ease-in-out;
        &:focus {
          box-shadow: 0px 0px 15px black;
          outline: 1px solid #171818;
        }
      }
      .login-btn {
        padding: 13px 16px;
        background-color: $oq;
        color: $text_black;
        border-radius: 5px !important;

        &:focus {
          box-shadow: 0px 0px 15px $text_black;
          outline: 1px solid $text_black;
        }
        &:hover {
          box-shadow: 0px 0px 15px $text_black;
        }
        &:active {
          box-shadow: 0px 0px 15px $oq;
          color: $oq;
          background-color: $kok;
        }
      }
      a {
        font-size: 15px;
        font-weight: 500;
        text-align: center;
        color: #1e88e5;
      }
      .form_links {
        display: flex;
        justify-content: center;
        gap: 10px;
        > div {
          border-left: 1px solid #171818;
        }
      }
    }
  }
}
</style>
