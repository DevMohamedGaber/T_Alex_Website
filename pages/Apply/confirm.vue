<template>
  <div id="Apply">
    <div class="container">
      <h2>اكمال البيانات</h2>
      <p class="color-grey">يرجي مليء النموذج ادناه بالبيانات الصحيحة من بطاقة الرقم القومي و شهادة الثانوية</p>
      <br>
      <div class="row">
        <span>اسم الطالب:</span>
        <p style="margin-right: 4%;">{{ $route.params['name'] }}</p>
      </div>

      <div class="row">
        <div>
          <label for="nationality">الجنسية</label>
          <input type="text" name="nationality" v-model="nationality"/>
        </div>
        <div>
          <label for="religion">الديانة</label>
          <input type="text" name="religion" v-model="religion"/>
        </div>
        <div>
          <label for="gender">النوع</label>
          <select name="gender" v-model="gender">
            <option value="0" selected>ذكر</option>
            <option value="1">انثي</option>
          </select>
        </div>
      </div>
    
      <div class="row">
        <div>
          <label for="birthDay">تاريخ الميلاد</label>
          <input type="date" name="birthDay" v-model="birthDay">
        </div>
        <div>
          <label for="birthPlace">جهة الميلاد</label>
          <input type="text" name="birthPlace" v-model="birthPlace">
        </div>
        <div>
          <label for="birthGovern">محافظة</label>
          <input type="text" name="birthGovern" v-model="birthGovern">
        </div>
      </div>

      <div class="row">
        <div>
          <label for="address">العنوان</label>
          <input type="text" name="address" v-model="address">
        </div>
        <div>
          <label for="division">قسم/مركز</label>
          <input type="text" name="division" v-model="division">
        </div>
        <div>
          <label for="addressGovern">محافظة</label>
          <input type="text" name="addressGovern" v-model="addressGovern">
        </div>
      </div>

      <div class="row">
        <div class="ignor-row">
          <span>الرقم القومي:</span>
          <p style="margin-right: 11%;">{{ $route.params['nID'] }}</p>
        </div>
        <div>
          <label for="nationalIDaddress">جهة صدورها</label>
          <input type="text" name="nationalIDaddress" v-model="nationalIDaddress">
        </div>
        <div>
          <label for="nationalIDGovern">محافظة</label>
          <input type="text" name="nationalIDGovern" v-model="nationalIDGovern">
        </div>
      </div>

      <div class="row">
        <div>
          <label for="phone">رقم موبايل الطالب</label>
          <input type="number" size="11" name="phone" v-model="phone">
        </div>
        <div>
          <label for="landline">رقم ارضي</label>
          <input type="number" size="7" name="landline" v-model="landline">
        </div>
        <div>
          <label for="parentPhone">رقم موبايل ولي الاول</label>
          <input type="number" size="11" name="parentPhone" v-model="parentPhone">
        </div>
      </div>
      
      <div class="row">
        <div>
          <label for="parentName">اسم ولي امر الطالب</label>
          <input type="text" name="parentName" v-model="parentName">
        </div>
        <div>
          <label for="profession">صناعته</label>
          <input type="text" name="profession" v-model="profession">
        </div>
        <div>
          <label for="parentAddress">عنوانه</label>
          <input type="text" name="parentAddress" v-model="parentAddress">
        </div>
      </div>
      
      <div class="row">
        <div>
          <label for="highschool">الثانوية</label>
          <select name="highschool" v-model="highschool">
            <option value="0" selected>صناعي</option>
            <option value="1">تعليم و تدريب مزدوج</option>
            <option value="2">تلمذة صناعية</option>
            <option value="3">دون بوسكو</option>
            <option value="4">عامة رياضة</option>
            <option value="5">عامة علوم</option>
          </select>
        </div>
        <div>
          <label for="otherHighscool">اخري</label>
          <input type="text" name="otherHighscool" v-model="otherHighscool">
        </div>
        <div>
          <label for="highschoolYear">عام</label>
          <input type="text" name="highschoolYear" v-model="highschoolYear">
        </div>
      </div>

      <div class="row">
        <div>
          <label for="diplomeDepartment">التخصص</label>
          <input type="text" name="diplomeDepartment" v-model="diplomeDepartment">
        </div>
        <div>
          <label for="diplomeScore">المجموع</label>
          <input type="number" name="diplomeScore" v-model="diplomeScore">
        </div>
        <div>
          <label for="diplomeSeatNumber">رقم الجلوس</label>
          <input type="number" name="diplomeSeatNumber" v-model="diplomeSeatNumber">
        </div>
      </div>

      <div class="row">
        <p class="btn bg-main" @click="Submit">تـاكـيـد الـبيـانـات</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'confirm',
  data: () => ({
    nationality: "",
    religion: "",
    gender: 0,
    birthDay: "",
    birthPlace: "",
    birthGovern: "",
    address: "",
    division: "",
    addressGovern: "",
    nationalIDaddress: "",
    nationalIDGovern: "",
    phone: "",
    landline: "",
    parentPhone: "",
    parentName: "",
    profession: "",
    parentAddress: "",
    highschool: 0,
    otherHighscool: "",
    highschoolYear: "",
    diplomeDepartment: "",
    diplomeScore: "",
    diplomeSeatNumber: ""
  }),
  methods: {
    Submit()
    {

    }
  }
}
</script>