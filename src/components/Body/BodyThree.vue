<template>
  <div class="user-con">
    <div>
      <div class="loading" v-if="isLoading">Loading...</div>
      <div v-else class="grid">
        <div class="user" v-for="item in data.users" :key="item">
          <div class="i-p">
            <div class="i">
              <img :src="item.image" alt="User's profile picture" />
            </div>
            <div class="p">
              <p>
                Name: {{ item.firstName }} {{ item.lastName }}
                {{ item.maidenName }}
              </p>
              <p>Gender: {{ item.gender }}</p>
              <p>Department: {{ item.company.department }}</p>
              <p>
                Title: <span>{{ item.company.title }}</span>
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="sign">
        <p>Sign up to continue</p>
        <p>or sign in</p>
      </div>
      <div class="up">
        <i v-on:click="top" class="fa-sharp fa-solid fa-circle-chevron-up"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BodyThree",
  data() {
    return {
      data: "",
      isLoading: true
    };
  },
  mounted() {
    fetch("https://dummyjson.com/users", {
      headers: {
        Accept: "application/json"
      }
    })
      .then((res) => res.json())
      .then((data) => (this.data = data))
      .finally(()=>{
        this.isLoading = false
      });
  },
  methods: {
    top() {
      document.getElementById("top").scrollIntoView();
      return true;
    }
  }
};
</script>

<style scoped>
.user-con {
  height: 100%;
  background-color: rgb(240, 240, 255);
  position: relative;
}

.user-con .loading{
  text-align: center;
  font-size: 38px;
}
.grid {
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-column-gap: 50px;
  grid-row-gap: 10px;
  padding: 10px;
}

.user {
  max-width: 30vw;
  background-color: rgb(231, 231, 255);
  border-radius: 20px;
}

.user .i-p {
  display: flex;
}

img {
  max-width: 10vw;
}

p {
  margin-left: 1vw;
  font-size: 14px;
}

p span {
  color: red;
}

.user-con .sign {
  display: flex;
  justify-content: center;
  align-items: center;
}

.user-con .sign p:first-child {
  padding: 2vh 3vw;
  background-color: black;
  color: white;
  transition: background-color 0.5s ease-in;
  cursor: pointer;
  border-radius: 20px;
  margin-right: 3vw;
}

.user-con .sign p:last-child {
  cursor: pointer;
  color: red;
}

.user-con .sign p:first-child:hover {
  background-color: white;
  color: black;
}

.up {
  position: absolute;
  right: 3vw;
  bottom: 2vh;
}

.up i{
    font-size: 38px;
  }
</style>
