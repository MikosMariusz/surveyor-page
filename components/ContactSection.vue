<template>
  <section :id="sectionid">
    <div class="contact-container">
      <div class="contact-desc">
        <h2 class="contact-title">
          Kontakt
        </h2>
        <span>
          Jeśli szukasz usług sprawdzonego geodety, bądź masz pomysł na współpracę napisz lub zadzwoń.
        </span>
        <div class="contact-details">
          <div class="detail">
            <span class="material-icons">phone</span>
            <span>(+48) 508 843 246</span>
          </div>
          <div class="detail">
            <span class="material-icons">mail_outline</span>
            <span>tyleckimarcin@gmail.com</span>
          </div>
          <div class="detail">
            <span class="material-icons">language</span>
            <span>www.geodezjatylecki.pl</span>
          </div>
          <div class="detail">
            <span class="material-icons">home</span>
            <span>JANÓWEK 11 55-065 JORDANÓW ŚLĄSKI</span>
          </div>
        </div>
      </div>
      <div class="contact-map">
        <no-ssr>
          <l-map :zoom=12 :center="[50.848986, 16.832425]">
            <l-tile-layer url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"></l-tile-layer>
            <l-marker :lat-lng="[50.848986, 16.832425]"></l-marker>
          </l-map>
        </no-ssr>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
  props: {
    sectionid: {
      type: String,
      required: true
    }
  },
  scrollToTop: true
}
</script>

<style scoped>
.contact-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.contact-title {
  color: #7c2c35;
  font-family: Raleway, sans-serif;
  font-weight: 500;
  margin-bottom: 15px;
}
.contact-desc {
  margin: 0 30px 30px 30px;
  line-height: 1.5;
  font-size: 20px;
  font-family: Raleway, sans-serif;
  font-weight: 300;
}
.contact-map {
  display: none;
  width: 90%;
  min-height: 400px;
  box-shadow: 0 5px 28px rgba(0, 0, 0, 0.3), 0 3px 10px rgba(0, 0, 0, 0.22);
  margin-bottom: 40px;
}
.contact-details {
  margin: 30px;
  display: flex;
  flex-direction: column;
  justify-content: left;
  line-height: 1.5;
  font-size: 20px;
  font-family: Raleway, sans-serif;
  font-weight: 300;
  color: #7c2c35;
}
.material-icons {
  font-size: 36px !important;
}
.detail {
  padding: 5px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  font-size: 16px;
}

.detail span {
  margin-right: 10px;
}

@media (min-width: 800px) {
  .contact-container {
    width: 70%;
    height: 70%;
    padding: 30px;
    flex-direction: row;
    border: 1px solid #7c2c35;
    box-shadow: 0 5px 28px rgba(0, 0, 0, 0.3), 0 3px 10px rgba(0, 0, 0, 0.22);
  }
  .contact-desc {
    width: 50%;
    text-align: left
  }
  .detail {
  justify-content: left;
  }
  .contact-map {
    display: block;
    width: 50%;
    margin-bottom: 0px;
  }
}
</style>
