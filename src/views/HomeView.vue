<template>
  <div class="home page">
    <div class="back">
      <img class="sky" src="@/assets/home/home-desktop.png" alt="">
      <img class="planet" src="@/assets/home/background.png" alt="">
    </div>
    <header class="header container">
      <div class="left">
        <h5>SO, YOU WANT TO TRAVEL TO</h5>
        <h1>SPACE</h1>
        <p class="light-color">Let’s face it; if you want to go to space, you might as well genuinely go to outer space
          and not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this
          world experience!</p>
      </div>
      <div class="right">
        <button class="btn-explore dark-color">EXPLORE</button>
      </div>
    </header>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.home {
  display: flex;
  align-items: center;

  .header {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    padding-block:  10rem 5rem;
    .left {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
      gap: 1.5rem;
      p{
        max-width: 25rem;
      }
      
    }

    .right {

      .btn-explore {
        width: 15.2rem;
        height: 15.2rem;
        border-radius: 50%;
        font-family: 'Bellefair';
        font-style: normal;
        font-weight: 400;
        font-size: 32px;
        line-height: 37px;
        letter-spacing: 2px;
        background-color: #fff;
        border: none;
        outline: none;
        cursor: pointer;
      }
    }
  }
}
</style>