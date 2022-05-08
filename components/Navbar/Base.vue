<template>
  <div id="Navbar">
    <div class="container">
      <ul class="links">
        <li>
          <nuxt-link to="/" class="active">الرئيسية</nuxt-link>
        </li>
        <NavbarDropdown label="عن الكلية" :list="aboutList"/>
        <NavbarDropdown label="البرامج الاكاديمية" :list="programsList"/>
        <NavbarDropdown label="الطـلاب" :list="studentsList"/>
        <li class="apply">
          <nuxt-link to="/apply">تقدم الان </nuxt-link>
        </li>
      </ul>
      <!-- Logo -->
      <nuxt-link class="logo" to="/">
        <img src="/Logo.jpg" alt="">
      </nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "NavBar",
  data() {
    return {
      aboutList: [
        ["كلمة مدير الكلية", "/about/manager_word"],
        ["أهداف الكلية", "/about/goals"],
        ["الدرجات العلمية", "/about/degrees"],
        ["ادارة الكلية", "/about/managment"],
        ["هيئة التدريس", "/about/managment"]
      ],
      programsList: [
        ["شروط القبول", "/about/manager_word"],
        ["مستويات الدراسة", "/about/manager_word"],
        ["المواظبة ", "/about/manager_word"],
        ["التخرج", "/about/manager_word"],
      ],
      studentsList: [
        ["الاقسام العلمية", "/departments"],
        ["النتائج", "/results"],
      ]
    }
  }
}
</script>