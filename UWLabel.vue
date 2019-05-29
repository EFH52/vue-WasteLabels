<template>
  <div class="UWOutset">
    <div class="UWLabel">
      <div class="UWTopbar">
        <h1 class="UWH1 UWH1Tilt">UNIVERSAL</h1>
        <h1 class="UWH1">WASTE</h1>
      </div>
      <div class="UWInset">
        <div class="row justify-content-center">
          <h2 class="UWH2">GENERATOR INFORMATION (Optional)</h2>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-3 UWH2 UWbody">SHIPPER</h2>
          <span class="col-8 text-info align-self-end">{{facility}}</span>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-2 UWH2 UWbody">ADDRESS</h2>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-4 UWH2 UWbody">CITY, STATE, ZIP</h2>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-3 UWH2 UWbody">CONTENTS</h2>
          <span class="col-8 text-info align-self-end">{{contents}}</span>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-2 UWH2 UWbody"></h2>
        </div>
        <div class="row m-0 no-gutters">
          <h2 class="col-6 UWH2 UWbody">ACCUMULATION START DATE</h2>
          <span class="col-5 text-info align-self-end">{{asd}}</span>
        </div>
      </div>
      <div class="UWSpacer"></div>
      <div class="UWFooter d-flex justify-content-center align-items-center">
        <div
          style="margin-top: -18px;  margin-left: -1.2px; transform: scale(1.088,1);"
        >UNIVERSAL WASTE</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UWLabel",
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
.UWLabel {
  width: 500px;
  height: 500px;

  background-color: rebeccapurple;
}
.UWOutset {
  background-color: white;
  width: 520px;
  height: 520px;
  padding: 10px;
}

.UWTopbar {
  height: 182px;
}
.UWInset {
  background-color: white;
  width: 480px;
  height: 257px;
  padding: 5px;
  margin-left: 10px;
  margin-right: 10px;
}
.UWSpacer {
  height: 10px;
}
.UWFooter {
  height: 51px;
  background-color: white;
  color: rebeccapurple;
  font-size: 50px;
  font-weight: 900;
  text-align: justify;
}
.UWH1 {
  font-weight: 900;
  text-align: right;
  color: white;
  font-size: 84px;
  margin: 0;
  margin-top: 35px;
  margin-right: 10px;
  transform: scale(1, 1.3);
}
.UWH1Tilt {
  transform: rotate(-30deg) scale(1, 1.25);
  font-size: 51px;
  text-align: left;
  margin: 0;
  margin-left: -25px;
  margin-top: 7px;
  line-height: 0.5;
  padding-top: 15px;
}
.UWH2 {
  color: rebeccapurple;
  font-size: 15px;
  font-weight: bolder;
}
.UWbody {
  margin: 22px 0px 0px 10px;
  font-weight: 900;
}
@media print {
  .UWOutset,
  .UWInset {
    border: 2px solid black;
  }
  .UWH1,
  .UWH1Tilt,
  .UWFooter {
    color: black;
  }
}
</style>
