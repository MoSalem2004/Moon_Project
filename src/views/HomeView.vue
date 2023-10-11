<template>
  <header>
    <h2><a href="#" class="logo">SALEM TEAM</a></h2>
    <ul>
      <li class="active"><a href="#">Home</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">portfolio</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </header>
  <section class="main">
    <img src="../../assets/stars1.png" id="Starts" title="Starts" />
    <img src="../../assets/moon2.png" id="moon" title="moon" />
    <div class="monthem">SALEM TEAM</div>
    <img src="../../assets/mountains3.png" id="mountains3" title="mountains3" />
    <img src="../../assets/mountains4.png" id="mountains4" title="mountains4" />
    <img src="../../assets/river5.png" id="river" title="river" />
    <img src="../../assets/boat6.png" id="boat" title="boat" />
    <img src="../../assets/mountains7.png" id="mountains7" title="mountains7" />
  </section>
  <section class="lorem">
    <h2>Hello In Salem Team</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque
      placeat ab pariatur, tenetur facilis provident architecto, sed optio eaque
      eligendi id voluptatem alias odit. Dolorem vero pariatur labore ipsam
      rerum iure ratione, magnam dolor rem, eveniet eum voluptatem aut
      blanditiis aliquid aperiam excepturi nam non amet provident quis
      necessitatibus tempora doloribus ab. Nostrum ut modi, maiores harum
      explicabo enim id ducimus reiciendis. Omnis tempora dolorem tempore
      officiis delectus laboriosam nesciunt suscipit, cumque adipisci, hic quas
      consectetur! Necessitatibus, praesentium quas sed labore dolorem, nemo,
      quidem exercitationem quis obcaecati distinctio hic vero? Veniam non
      consequatur amet doloribus eaque aspernatur, ipsum error cupiditate? Lorem
      ipsum dolor sit amet consectetur adipisicing elit. Fuga officiis
      recusandae reprehenderit placeat ut accusantium sunt repellendus inventore
      esse perferendis vitae ipsam excepturi nihil et harum soluta libero at
      dolorem doloremque rerum, rem optio! Harum ullam veniam, iure odit
      laboriosam officiis incidunt earum magnam quam temporibus amet. Fuga,
      voluptas libero! Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Ipsum velit vel amet at iure ipsa nisi ad nulla non dolor officiis quo
      voluptatem, deserunt, ut fugiat voluptatum placeat accusantium
      consequuntur! Fuga id, illum veniam cum perspiciatis harum sint nesciunt
      ratione temporibus voluptatibus a molestias vero suscipit quos? Quod,
      reprehenderit dolores.
    </p>
  </section>
</template>
<script>
export default {
  name: "HomeView",
  mounted() {
    let Starts = document.getElementById("Starts");
    let moon = document.getElementById("moon");
    let mountains3 = document.getElementById("mountains3");
    let mountains4 = document.getElementById("mountains4");
    let river = document.getElementById("river");
    let boat = document.getElementById("boat");
    let monthem = document.querySelector(".monthem");
    window.onscroll = function () {
      let value = window.scrollY;
      Starts.style.left = `${value}px`;
      moon.style.top = `${value * 4}px`;
      mountains3.style.top = `${value * 2}px`;
      mountains4.style.top = `${value * 1.5}px`;
      river.style.top = `${value}px`;
      boat.style.top = `${value}px`;
      boat.style.left = `${value * 3}px`;
      monthem.style.fontSize = `${value}px`;
      monthem.style.bottom = `${value}px`;
      if (scrollY >= 67) {
        monthem.style.fontSize = `67px`;
        monthem.style.position = `fixed`;
        if (scrollY >= 451) {
          monthem.style.display = "none";
        } else {
          monthem.style.display = "block";
        }
        if (scrollY >= 127) {
          document.querySelector("body").style.background =
            "linear-gradient( #376281, #10001f)";
        } else {
          document.querySelector("body").style.background =
            "linear-gradient(#200016 , #10001f)";
        }
      } else {
        monthem.style.position = `absolute`;
      }
    };
  },
};
</script>
<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 95%;
  margin: 30px;
  position: absolute;
  top: 0;
  z-index: 1;
}
header .logo {
  font-size: 30px;
  text-transform: uppercase;
}
header ul {
  display: flex;
  justify-content: space-between;
  list-style: none;
}
header ul li {
  margin-left: 10px;
  padding: 10px;
  border-radius: 20px;
  transition: 0.5s;
  cursor: pointer;
}

header ul li:hover,
header ul li.active {
  background-color: #fff;
}
header ul li:hover a {
  color: #200016;
}
header ul li.active a {
  color: #200016;
}
.main {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.main::after {
  content: "";
  position: absolute;
  bottom: 0;
  height: 100px;
  width: 100%;
  background: linear-gradient(to top, #200016, transparent);
}
.main img {
  position: absolute;
  width: 100%;
  height: 100vh;
  object-fit: cover;
}
.main img#river {
  filter: hue-rotate(298deg);
}
.main img#moon {
  mix-blend-mode: screen;
  transform: translateY(80px);
}
.monthem {
  color: #fff;
  font-size: 24px;
  text-transform: uppercase;
  transform: translate(-50%, -167px);
  position: absolute;
  top: 50%;
  left: 50%;
  text-align: center;
}
/*  */
.lorem {
  color: #fff;
  padding: 30px;
  background: linear-gradient(#200016, #10001f);
}
.lorem h2 {
  font-size: 30px;
}
.lorem h2,
.lorem p {
  padding: 20px 0;
}

@media (max-width: 676px) {
  header ul {
    display: none;
  }
}
</style>
