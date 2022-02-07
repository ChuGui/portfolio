<template>
  <section>
    <h2 style="text-align: center">Mes compétences à votre service</h2>
    <div class="section-container">
      <div class="tabs">
        <div>Besoin d'un site ecommerce rapidement?</div>
        <div>Besoin d'aide sur une application PHP/JS ?</div>
        <div>Travail en équipe et suivi des tâches</div>
      </div>
      <div class="main-content">
        <div class="text-container">
          ipsum dolor sit amet, consectetur adipisicing elit. Beatae minima modi qui! Accusamus, aperiam consequatur
          dolore doloribus earum incidunt iusto maiores quas quibusdam quis recusandae,
          saepe, sit vel. Eaque, praesentium?
        </div>
        <div class="image-container">
          <div class="image"></div>
          <div class="image"></div>
          <div class="image"></div>
        </div>
      </div>
    </div>

  </section>


</template>

<script>
export default {
  name: "FirstBlock"
}
</script>

<style scoped lang="scss">
section {
  background-color: white;
  padding: 50px;
  margin: 0;

  .section-container {
    margin-top: 40px;
    display: flex;
    gap: 60px;
    justify-content: center;

    .tabs {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      gap: 10px;

      div {
        width: 200px;
        padding: 10px;
        background-color: darkgrey;
        text-align: center;
        border-radius: 5px;

        &:hover {
          cursor: pointer;
        }
      }
    }
    .main-content {
      display: flex;
      gap: 40px;
      .text-container {
        flex: 2 1 0;
      }
      .image-container {
        flex: 1 1 0;
        position: relative;
        .image {
          position: absolute;
          top:0;
          left: 0;
          height: 40px;
          width: 40px;
          border-radius: 40px;
          background-color: #ffbaa0;
        }
      }
    }
  }
}
</style>
