<template>
<div id="app">
  <div class="container">
      <div class="main-container">
        <div class="title">
          <h1>XX Days Left Till 2021!!</h1>
          <p>00:00:00:00</p>
          <p>December xx xx</p>
          </div>
          <div class="input-container">
            <h3>Enter your new year's resolution</h3>
            <input type="text"  placeholder="Type here." id="input-text" v-on:keypress ='getMsg' v-model="msg" >
          </div>
          <div class="result-container">
            <ul>
              <li>{{ msg }}</li>
              <li>Hydrate</li>
            </ul>
          </div>
      </div>
  </div>
</div>
</template>

<script>


export default {
name: 'App',
data(){
  return {
    msg: ''
  }
}, methods: 
{
  getMsg(e)
  {
    if(e.key == 'Enter')
    {
      console.log(this.msg)
      return this.msg
    }
  }
}




}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
* 
{
  padding: 0;
  margin: 0;
  font-family: 'Roboto',sans-serif;
}
.container
{
  width: 100vw;
  height: 100vh;
  background: linear-gradient(46.19deg, #ACB4E7 5.66%, #B1E0B0 94.35%);
  display: grid;
  place-items: center;
}
h1 
{
  font-weight: 700;
  color: #4F6AFF;
}
h3 
{
  font-weight: 400;
}
#input-text
{
  height: 52px;
  width: 250px;
  border: none;
  background: rgba(255, 255, 255, 0.34);
  border-radius: none;
}
.title
{
  text-align: center;
}

.title p:nth-child(2)
{
  font-weight: 700;
  font-size: 42px;
}
.title p:nth-child(3)
{
  font-size: 21px;
  color: rgba(255, 255, 255, .85);
}
.main-container
{
  max-width: 500px;
  height: 80vh;
  display: flex;
  flex-direction:  column;
  align-items: center;
  justify-content: space-evenly;
}
@media  (max-width: 500px)
{
  .main-container
  {
    width: 100%;
  }  
  .result-container ul
  {
    display: grid;
    grid-template-rows: 1fr 1fr 1fr 1fr;
    grid-template-columns: 1fr;
    grid-gap: 0;
  }
  .result-container
  {
    width: 100%;
  }
}
.result-container ul
{
  list-style: none;
  display: grid;
  grid-template-rows: repeat(4,60px);
  grid-template-columns:  200px 200px;
  grid-gap:  1rem;
}
.result-container ul li
{

  background: rgba(255, 255, 255, 0.34);
  display: flex;
  align-content: center;
}
.result-container ul li p
{
  padding: 0;
  margin: 0;
}
</style>
