  <template>
  <div class="bio-box">
    <img class="bio-box__pfp" src="/imgs/profilepic2.jpg" alt="" />
    <h3 class="bio-box__title">'Zer0Power</h3>
    <p class="bio-box__subtitle">Maxgaming Dev</p>
    <form action="http://localhost:3000/auth/get-data/" method="POST">
      <div class="container">
        <UserCircleIcon style="width:2rem;height: 2rem;" />
        <input type="email" class="input" placeholder="Email" name="email" required>
      </div>
      
      <div class="container">
        <LockClosedIcon style="width:2rem;height: 2rem;" />
        <input type="password" class="input" placeholder="Password" name="password" required>
      </div>
      <button class="submit-btn" type="submit">Continue</button>
    </form>
  </div>
</template>

<script setup>
import { UserCircleIcon, LockClosedIcon } from "@heroicons/vue/outline";
import { ref } from "vue";
</script>

<style lang="scss" scoped>
@import "@/assets/scss/variables";

.bio-box {
  font-family: "Roboto", sans-serif;
  background: $boxes-color;
  padding: 1rem;
  border-radius: 0.5rem;
  width: 76%;
  color: white;
  position: relative;
  margin: 0.8rem 0;
  max-width: $boxes-width;
  backdrop-filter: blur(0.8rem);
  z-index: 10;

  @media screen and (min-width: $md) {
    width: $boxes-width;
  }

  .bio-box__pfp {
    display: block;
    width: 40%;
    margin: auto;
    border-radius: 0.3rem;
  }

  .bio-box__title {
    font-family: "Macondo", cursive;
    font-size: 20px;
    text-align: center;
    color: white;
    margin: 0.3rem;
  }

  .bio-box__subtitle {
    font-family: "Roboto", sans-serif;
    font-size: 12px;
    color: #131415;
    text-align: center;
    margin: 0;
  }

  .input {
    font-family: "Roboto", sans-serif;
    flex-grow: 1;
    background: transparent;
    color: white;

    &::placeholder {
      font-family: "Roboto", sans-serif;
      color: white;
    }
  }

  .container {
    display: flex;
    flex-direction: row;
    border-radius: 0.5rem;
    border: solid 1px white; 
    padding: 0.2rem 0.3rem; 
    margin: 0.5rem 0; 
    gap: 0.2rem;
  }
  
  .submit-btn {
    display: block;width:100%;
    background: #A9A9A9;
    text-align: center;
    border-radius: 0.5rem;
    padding: 0.6rem;
    box-sizing: border-box;
  }
}
</style>
