<template>
  <div class="user-con">
    <div>
      <div class="grid">
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
        <p>Sign in</p>
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
      data: ""
    };
  },
  mounted() {
    fetch("https://dummyjson.com/users", {
      headers: {
        Accept: "application/json"
      }
    })
      .then((res) => res.json())
      .then((data) => (this.data = data));
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
  background-color: blue;
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
  background-color: rgb(241, 241, 250);
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
}

.user-con .sign p:last-child {
  cursor: pointer;
}

.user-con .sign p:first-child:hover {
  background-color: white;
  color: black;
}

.up {
  position: absolute;
  right: 3vw;
  /* top: 2px; */
  /* z-index: -1; */
}
</style>
