<template>
  <section :id="sectionid">
    <div class="about-wraper">
      <h2 class="about-title">
        Usługi Geodezyjne Marcin Tylecki jest debiutującą, prywatną firmą geodezyjną na terenie gminy Jordanów Śląski.
      </h2>
      <span class="about-desc">
        Dzięki współpracy z doświadczonymi geodetami jesteśmy w stanie sprostać wszelkim wymaganiom stawianym obecnie firmom. Posiadane doświadczenie oraz sprzęt i oprogramowanie pozwalają na wykonanie wszelkiego rodzaju prac geodezyjnych. W swojej pracy wykorzystujemy nowoczesny sprzęt pomiarowy m.in.: GPS-Topcon, tachimetry-Leica i Topcon, niwelatory-Leica i Nivel System.
      </span>
      <h2 class="about-sub-title">
        Swoje usługi świadczymy głównie na terenie Dolnego Śląska.
      </h2>
      <ul class="list-container">
        <li>
          Zapewniamy wysoką jakość oraz terminowość zamówionych u nas prac.
        </li>
        <li>
          Jesteśmy przygotowani do podejmowania  różnorodnych zadań, od niewielkich przeznaczonych dla klienta
          indywidualnego, do dużych, trudnych i nietypowych inwestycji.
        </li>
        <li>Wśród naszych Klientów znajdują się zarówno osoby prywatne oraz firmy . Nasze usługi kierujemy do firm:
          projektowych, architektonicznych, budowlanych oraz klientów indywidualnych.
        </li>
        <li>
          Deklarujemy, że prace zostaną wykonane z należytą starannością, zgodnie z wiedzą techniczną i zawodową.
        </li>
        <li>
          Zapraszamy do zapoznania się z naszą stroną internetową, oraz pełną ofertą. Mamy szczerą nadzieję, że informacje
          zawarte w ofercie zachęcą państwa do współpracy z naszą firmą.
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
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
  .about-wraper {
    width: 90%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .about-title {
    color: #7c2c35;
    font-family: Raleway, sans-serif;
    font-weight: 500;
    margin: 80px 30px 10px 30px;
  }
  .about-sub-title {
    color: #7c2c35;
    font-family: Raleway, sans-serif;
    font-weight: 500;
    margin: 20px 30px;
  }
  .about-desc {
    margin: 15px 45px;
    line-height: 1.5;
    font-size: 16px;
    font-family: Raleway, sans-serif;
    font-weight: 300;
  }

  @media (min-width: 1200px) {
    .about-title,
    .about-sub-title,
    .about-desc {
      margin-left: 200px;
      margin-right: 200px;
    }
  }
</style>
