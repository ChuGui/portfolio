<template>
  <section >
    <div class="tab-container">
      <div :class="{underlined: tabSelected === 0}" @click="tabSelected=0">
        Ma Formation
      </div>
      <div :class="{underlined: tabSelected === 1}" @click="tabSelected=1">
        Mon Parcours
      </div>
      <div :class="{underlined: tabSelected === 2}" @click="tabSelected=2">
        Mes Coordonnées
      </div>
    </div>
    <div class="main-content">
      <div class="ma-formation-container" :class="{hideIt: tabSelected !== 0, showIt: tabSelected === 0}">
        Ma formation
      </div>
      <div class="mon-parcours-container" :class="{hideIt: tabSelected !== 1, showIt: tabSelected === 1}">
        Mon parcours
      </div>
      <div class="mes-coordonnées-container" :class="{hideIt: tabSelected !== 2, showIt: tabSelected === 2}">
        Mes coordonnées
      </div>
    </div>
  </section>

</template>

<script>
export default {
  name: "FirstBlock",
  data() {
    return {
      tabSelected: 0,
    }
  }
}
</script>

<style scoped lang="scss">
section {
  padding: 50px;
  margin: 0;
  position: relative;

  .tab-container {
    display: flex;
    flex-wrap: wrap;

    div {
      padding: 20px;
      margin-right: 50px;

      &:hover {
        cursor: pointer;
      }
    }
  }
  .main-content {
    display: flex;
    position: relative;
    div {
      position: absolute;
      top: 0;
      left: 0;
    }
    .showIt {
      animation: slideIn .7s ease-in-out forwards;
    }
    .hideIt {
      animation: slideOut .7s ease-in-out forwards;
    }
  }

  &::after {
    content: "";
    position: absolute;
    top: 100%;
    left: 0;
    height: 20px;
    width: 100%;
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/3/rip.svg) bottom center #9471fd;
    background-size: 20%;
    transform: rotateX(180deg);
  }
}
</style>
