<template>
  <div class="container">
    <div class="card">
      <div class="imgBx">
        <img src="https://picsum.photos/600/800" alt="" />
      </div>
      <div class="content">
        <div class="contentBx">
          <h3>
            Random Image <br />
            <span>Nisiquiera se que</span>
          </h3>
        </div>
        <ul class="sci">
          <li style="--i:1;">
            <a href="#"><i class="fab fa-facebook"></i></a>
          </li>
          <li style="--i:2;">
            <a href="#"><i class="fab fa-twitter"></i></a>
          </li>
          <li style="--i:3;">
            <a href="#"><i class="fab fa-instagram"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DatosPokemon',
  props: ['datosFromRequest'],
  methods: {},
  data () {
    return {
      dataPokemon: ''
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
}

.container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin: 40px 0;
}

.container .card {
  position: relative;
  width: 300px;
  height: 400px;
  margin: 20px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
  border-radius: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container .card .content {
  position: absolute;
  bottom: -160px;
  width: 100%;
  height: 160px;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 100;
  flex-direction: column;
  backdrop-filter: blur(15px);
  box-shadow: 0 -10px 10px rgba(0, 0, 0, 0.15);
  border: 1px solid rgba(255, 255, 255, 0.2);
  transition: bottom 0.5s;
  transition-delay: 0.8s;
}

.container .card:hover .content {
  bottom: 0;
  transition-delay: 0s;
}

.container .card .content .contentBx h3 {
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-weight: 700;
  font-size: 18px;
  text-align: center;
  margin: 20px 0 15px;
  line-height: 1.1em;
  transition: 0.5s;
  opacity: 0;
  transform: translateY(-20px);
  transition-delay: 0.6s;
}

.container .card:hover .content .contentBx h3 {
  opacity: 1;
  transform: translateY(0px);
}

.container .card .content .contentBx h3 span {
  font-size: 12px;
  font-weight: 300;
  text-transform: initial;
}

.container .card .content .sci {
  position: relative;
  bottom: 10px;
  display: flex;
}

.container .card .content .sci li {
  list-style: none;
  margin: 0 10px;
  transform: translateY(40px);
  transition: 0.5s;
  opacity: 0;
  transition-delay: calc(0.2s * var(--i));
}

.container .card:hover .content .sci li {
  opacity: 1;
  transform: translateY(0px);
}

.container .card .content .sci li a {
  color: #fff;
  font-size: 24px;
}
</style>
