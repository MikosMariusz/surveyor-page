<template>
  <section>
    <div class="eu-funding-container">
      <p>Sfinansowano ze Środków Unii Europejskiej w ramach Poddziałania 19.2 "Wsparcie na wdrażanie operacji pn. "Marcin Tylecki - podjęcie działalności gospodarczej w zakresie usług geodezyjnych" w ramach strategii rozwoju lokalnego kierowanego przez społeczność" objętego PROW na lata 2014-2020 z udziałem Środków Europejskiego Funduszu Rolnego na rzecz Rozwoju Obszarów Wiejskich: Europa inwestująca w obszary wiejskie.</p>
      <p>Operacja ma na celu podjęcie działalności gospodarczej w zakresie usług geodezyjnych, która pozwoli na rozwój gospodarczy Lokalnej Grupy Działania Ślężanie</p>

      <p class="founding-1-footer">"Europejski Fundusz Rolny na rzecz Rozwoju Obszarów Wiejskich: Europa inwestująca w obszary wiejskie"</p>
      <p class="founding-footer">Programu Rozwoju Obszarów Wiejskich na lata 2014-2020</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EUFundingSection',
  scrollToTop: true
}
</script>

<style scoped>
.eu-funding-container {
  width: 100%;
  height: 100%;
  margin-bottom: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.eu-funding-container p {
  font-size: 16px;
  font-family: Raleway, sans-serif;
  font-weight: 500;
  margin: 5px;
}
p.founding-1-footer {
  margin-top: 20px;
}

@media (min-width: 800px) {
  .eu-funding-container {
    width: 90%;
    height: 90%;
    padding: 30px;
    border: 1px solid #7c2c35;
    background-color: #fff;
    box-shadow: 0 5px 28px rgba(0, 0, 0, 0.3), 0 3px 10px rgba(0, 0, 0, 0.22);
  }
}

@media (min-width: 1200px) {
  .eu-funding-container {
    width: 70%;
  }
}
</style>