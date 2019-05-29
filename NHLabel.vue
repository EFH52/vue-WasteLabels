<template>
  <div class="NHOutset">
    <div class="NHLabel">
      <div class="NHTopbar">
        <div class="position-relative">
          <h1 class="NHH1Tilt p-1">
            &nbsp;&nbsp;&nbsp;NON-
            <br>HAZARDOUS
          </h1>
          <h1 class="NHH1">Waste</h1>
        </div>
      </div>
      <div class="d-flex">
        <div
          class="NHInsetLeft align-self-center"
        >SOLID WASTE EXCLUEDED FROM REGULATION UNDER 40CFR 261.4 (B)</div>
        <div class="NHInsetRight">
          <div class="row">
            <h2 class="NHH2">OPTIONAL INFORMATION</h2>
          </div>
          <div class="row m-0 no-gutters">
            <h2 class="col-3 NHH2 NHbody">SHIPPER</h2>
            <span class="col-8 text-info align-self-end">{{facility}}</span>
          </div>
          <div class="row m-0 no-gutters">
            <h2 class="col-2 NHH2 NHbody">ADDRESS</h2>
          </div>
          <div class="row m-0 no-gutters">
            <h2 class="col-4 NHH2 NHbody">CITY, STATE, ZIP</h2>
          </div>
          <div class="row m-0 no-gutters">
            <h2 class="col-3 NHH2 NHbody">CONTENTS</h2>
            <span class="col-8 text-info align-self-end">{{contents}}</span>
          </div>
          <div class="row m-0 no-gutters">
            <h2 class="col-2 NHH2 NHbody"></h2>
          </div>
        </div>
      </div>
      <div class="NHSpacer"></div>
      <div class="NHFooter d-flex justify-content-center align-items-center">
        <div style="transform: scale(1.073,1.2)">NON-HAZARDOUS WASTE</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NHLabel",
  data: function() {
    return {};
  },
  props: {
    facility: String,
    address: String,
    citystatezip: String,
    asd: String,
    contents: String
  }
};
</script>

<style scoped>
.NHLabel {
  width: 500px;
  height: 500px;
  background-color: green;
}
.NHOutset {
  background-color: white;
  width: 520px;
  height: 520px;
  padding: 10px;
}

.NHTopbar {
  position: relative;
  height: 182px;
}
.NHInsetRight {
  display: inline-block;
  background-color: white;
  width: 360px;
  height: 237px;
  padding: 5px;
  margin-right: 20px;
}
.NHInsetLeft {
  display: inline-block;
  width: 100px;
  color: white;
  margin: 10px;
  font-size: 10px;
}
.NHSpacer {
  height: 20px;
}
.NHFooter {
  height: 61px;
  background-color: white;
  color: green;
  font-size: 37px;
  font-weight: 900;
}
.NHH1 {
  position: absolute;
  font-weight: 900;
  color: white;
  font-size: 70px;
  right: 20px;
  top: 95px;
  transform: scale(1, 1.2);
}
.NHH1Tilt {
  font-weight: 900;
  color: white;
  transform: rotate(-20deg) scale(1, 1.25);
  font-size: 60px;
  text-align: left;
  margin: 0;
  margin-left: -15px;
  line-height: 0.9;
  padding-top: 15px;
  position: absolute;
}
.NHH2 {
  color: green;
  font-size: 15px;
  font-weight: 900;
  margin-left: 22px;
}
.NHbody {
  margin: 22px 0px 0px 5px;
  font-weight: bold;
}
@media print {
  .NHOutset,
  .NHInsetRight {
    border: 2px solid black;
  }
  .NHH1,
  .NHH1Tilt,
  .NHFooter {
    color: black;
  }
}
</style>
