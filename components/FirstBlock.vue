<template>
  <section>
    <div class="image-container">
      IMAGE
    </div>
    <div class="text-container">
      <div>
        Guillaume Churlet
      </div>
      <div>
        GCH Creative Web Studio
      </div>
      <div>Developpeur FullStack</div>
      <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium aut consequatur culpa dolorem ea
        esse fugit illo incidunt minima
        obcaecati odit provident quibusdam repellat sed soluta suscipit, tenetur velit voluptate.
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
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 50px;
  margin: 0;
  background: white;
  position: relative;

  .image-container {
    width: 200px;
    height: 200px;
    margin: 20px;
    border-radius: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #5d24ff;
  }

  .text-container {
    width: 600px;
    padding: 20px;
    margin: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #ffbaa0;
  }

  &::after {
    content: "";
    position: absolute;
    top: 100%;
    left: 0;
    height: 20px;
    width: 100%;
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/3/rip.svg) bottom center;
    background-size: 10%;
  }

}
</style>
