<template>
  <div class="container">
    <div class="s-f">
      <select>
        <option>Popular</option>
        <option>New & Noteworthy</option>
        <br />
        <option>Marketplace</option>
      </select>
      <button @click="showFilter()"><i class="fa fa-filter"></i>Filter</button>
    </div>
    <div class="p-i-s" v-if="show">
      <div class="p-i">
        <p>Tags</p>
        <i class="fas regular fa-magnifying-glass"></i>
        <input type="text" />
      </div>
      <div class="p-i-one">
        <p>color</p>
        <input type="text" placeholder="Enter hex or select"/>
      </div>
      <div class="p-i-two">
        <p>Timeframe</p>
        <select>
          <option>Now</option>
          <option>This past week</option>
          <option>This past month</option>
          <option>This past year</option>
          <option>All Time</option>
        </select>
      </div>
      <div class="p-i-three">
        <p>Downloads</p>
        <select>
          <option>Adobe Illustrator</option>
          <option>Adobe Photoshop</option>
          <option>Adobe XD</option>
          <option>Figma</option>
          <option>Invision</option>
          <option>Sketch</option>
        </select>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BodyTwo",
  data(){
	return{
		show: true
	}
  },
  methods:{
	showFilter(){
		this.show = !this.show
	}
  }
 
};
</script>

<style scoped>
.container {
  margin-top: 12vh;
}

.s-f select {
  margin-left: 5vw;
  padding: 1.5vh 0.5vw;
  border: 4px solid rgb(253, 226, 231);
  border-radius: 10px;
  cursor: pointer;
}

.s-f button {
  float: right;
  margin-right: 5vw;
  padding: 2vh 1vw;
  border-radius: 10px;
  border: none;
  cursor: pointer;
}

.p-i-s {
  display: flex;
  justify-content: space-around;
}

.p-i input {
  position: relative;
  padding: 2.1vh 1.5vw 1vh 1.5vw;
  border: 4px solid rgb(253, 226, 231);
  border-radius: 10px;
  cursor: pointer;
  /* border-radius: 20px; */
  /* border: none; */
}

/* .p-i div{
	display: flex
} */

.p-i i {
  position: absolute;
  left: 8vw;
  z-index: 1;
  padding-top: 1.1vh;
  /* top: 1vh */
  /* padding-top: 3vh; */
  /* color: rgb(121, 120, 120); */
}

.p-i-one input {
  padding: 2.1vh 1.5vw 1vh 1.5vw;
  border: 4px solid rgb(253, 226, 231);
  border-radius: 10px;
  cursor: pointer;
}

.p-i-two select {
  padding: 2.1vh 1.5vw 1vh 1.5vw;
  border: 4px solid rgb(253, 226, 231);
  border-radius: 10px;
  cursor: pointer;
}
.p-i-three select {
  padding: 2.1vh 1.5vw 1vh 1.5vw;
  border: 4px solid rgb(253, 226, 231);
  border-radius: 10px;
  cursor: pointer;
}
</style>
