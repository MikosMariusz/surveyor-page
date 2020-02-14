<template>
  <section :id="sectionid">
    <div class="offers-wraper">
      <h2 class="offer-title">
        Oferta:
      </h2>
      <h3 class="offer-sub-title">
        Pomiary do celów projektowych
      </h3>
      <ul class="list-container">
        <li class="list-element">
          Mapy sytuacyjno-wysokościowe do celów projektowych wykonywane w formie cyfrowej (DWG, DXF, DGN)
        </li>
      </ul>
      <h3 class="offer-sub-title">
        Tyczenie, inwentaryzacja obiektów naziemnych i podziemnych
      </h3>
      <ul class="list-container">
        <li>
          wyznaczanie budynku
        </li>
        <li>
          wyznaczanie reperu roboczego
        </li>
        <li>
          wyznaczanie punktów głównych
        </li>
        <li>
          inwentaryzacja powykonawcza budynku
        </li>
        <li>
          inwentaryzacja powykonawcza dróg, parkingów, itp.
        </li>
        <li>
          tyczenie i inwentaryzacje przyłączy wod-kan., gazu, kabla energetycznego
        </li>
        <li>
          inwentaryzacje zagospodarowania działki – do odbioru budynku w nadzorze budowlanym
        </li>
        <li>
          tyczenie i inwentaryzacja sieci liniowych wodno – kanalizacyjnych, gazowych, energetycznych
        </li>
      </ul>
      <h3 class="offer-sub-title">
        Przygotowanie materiałów dla celów prawnych
      </h3>
      <ul class="list-container">
        <li>
          podziały działek
        </li>
        <li>
          wznowienia i wyznaczenia punktów granicznych
        </li>
        <li>
          wykazy zmian gruntownych
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'OfferSection',
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
  .offers-wraper {
    width: 90%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .offer-title {
    color: #7c2c35;
    font-family: Raleway, sans-serif;
    font-weight: 500;
    margin: 80px 30px 10px 30px;
  }
  .offer-sub-title {
    color: #7c2c35;
    font-family: Raleway, sans-serif;
    font-weight: 500;
    margin: 20px 30px;
  }
  .offer-desc {
    margin: 15px 45px;
    line-height: 1.5;
    font-size: 16px;
    font-family: Raleway, sans-serif;
    font-weight: 300;
  }
</style>
