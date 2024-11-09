<template>
  <footer>
    <div class="footer__container">
      <div class="footer__title">
        <h1>Fine Dev</h1>
        <p>Copyright @2024. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style scoped>
  .footer__container {
      height: 133px;
      background-color: black;
      color: white;
      text-align: center;
      padding-top: 20px;
      width: 100%;
  }

  .footer__title h1 {
      margin: 0;
  }

  @media (max-width: 768px) {
      .footer__container {
          height: auto;
          padding: 10px 0;
      }
  }
</style>
