<template>
    <div class="login-container">
      <div class="login-box">
        <h1 class="logo">COOING</h1>
        <p class="subtitle">로그인하여 인플루언서가 되기 위한<br>솔루션을 바로 제공 받으세요!</p>
        <div class="social-login">
          <span>소셜 계정으로 로그인</span>
          <div class="social-icons">
            <KakaoLogin/>
            <GoogleLogin/>
            <GithubLogin/>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import KakaoLogin  from '../login/ui/KakaoLogin.vue';
import GoogleLogin  from '../login/ui/GoogleLogin.vue';
import GithubLogin from "~/account/pages/login/ui/GithubLogin.vue";
export default {
    name: 'LoginPage',
    components: {
        KakaoLogin,
        GoogleLogin,
        GithubLogin,
    }
}
</script>

<style scoped>

.login-container {
  display:flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.7);
  background-image: url("@/assets/fixed/login/login_background.png");
  background-size: cover;
  background-blend-mode: darken;
}

.login-box {
  width:400px;
  background-color: #202020;
  padding: 2rem;
  border-radius: 8px;
  text-align: center;
  color: white;
}

.logo {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: 0.9rem;
  margin-bottom: 2rem;
  line-height: 1.4;
}

.email-login {
  background-color: #ff9033;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  font-size: 1rem;
  cursor: pointer;
  width: 80%;
  margin-bottom: 1rem;
}

hr {
  width: 70%;
  margin-left: 50px;
  opacity: 0.5;
}

.social-login {
  font-size: 0.9rem;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 1rem;
}
</style>