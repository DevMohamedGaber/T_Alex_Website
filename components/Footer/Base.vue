<template>
  <footer id="footer">
    <FooterSVG />
    <div class="body">
      <p>جميع الحقوق محفوظة &copy; {{ year }}</p>
    </div>
  </footer>
</template>
<script>
export default {
  data: () => ({
    year: 2022
  })
}
</script>