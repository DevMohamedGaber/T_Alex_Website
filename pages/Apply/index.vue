<template>
  <div id="Apply">
    <div class="container">
      <h1>قم بالتقديم الان</h1>
      <p>يمكنك استكمال بيانات الالتحاق بالمعهد الفني الصناعي بادخال الرقم القومي للطالب</p>
      <div>
        <label for="nID">الرقم القومي</label>
        <input type="number" name="nID" placeholder="الرقم القومي 14 رقم" v-model="nID" @keyup="ClearErrors">
        <span class="btn bg-main" @click="CheckNationalID">تاكيد</span>
      </div>
      <div v-if="errors.length > 0">
        <p class="error" v-for="(error, index) in errors" :key="index">{{ error }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  head: () => ({
    title: "الالتحاق"
  }),
  data: () => ({
    nID: "",
    errors: [],
  }),
  methods: {
    async CheckNationalID() {
      this.ClearErrors();
      
      if(this.nID.length === 0) {
        this.errors.push("يجب ادراج الرقم القومي");
        return;
      }
      if(this.nID.length < 14) {
        this.errors.push("الرقم القومي اقل من 14 رقم");
        return;
      }
      if(this.nID.length > 14) {
        this.errors.push("الرقم القومي اكبر من 14 رقم");
        return;
      }
      var params = new URLSearchParams();
      params.append('nID', this.nID);
      const res = await this.$axios.$post('http://localhost/api/checkNationalID.php', params);
      if(res['error'])
      {
        this.errors.push(res.error)
        return;
      }
      this.$router.push({path: '/apply/confirm', name: 'Apply-confirm', params: { name: res['name'], nID: this.nID }})
    },
    ClearErrors() {
      if(this.errors.length > 0)
      {
        this.errors = [];
      }
    }
  }
}
</script>