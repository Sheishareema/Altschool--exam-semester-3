<template>
  <NavBar />
  <div class="home">
    <div class="txt">
      <p>
        Counter App - Altschool Africa School of Engineering, Frontend Stack
        Third Semester Exam
      </p>
      <router-link to="/counter">Go to Counter</router-link>
    </div>
  </div>
  <FooterApp />
</template>

<style scoped>
.home {
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: center;
  margin: 7% 9%;
}
.img {
  max-width: 700px;
  margin-left: 3%;
}

.img img {
  width: 100%;
  height: 30%;
  opacity: 0.3;
  border-radius: 10px;
}
.txt {
  display: flex;
  flex-direction: column;

  max-width: 400px;
}

.txt h1 {
  background-image: -webkit-linear-gradient(45deg, #fa84a2, #64bffc);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
span {
  color: #fa84a2;
}
.txt p {
  margin-bottom: 26px;
  font-size: 1.5rem;
  color: #c5c5c5;
}
.txt a {
  text-decoration: none;
  padding: 10px 25px;
  background-color: blue;
  color: #fff;
  transition: 0.5s;
}
.txt a:hover {
  background-color: #fa84a2;
}
</style>

<script>
import NavBar from "./NavBar.vue";

export default {
  components: {
    NavBar,
  },
};
</script>
