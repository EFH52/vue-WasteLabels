<template>
  <div class="HWOutset">
    <div class="HWLabel">
      <div class="HWInset">
        <h1 class="HWH1">HAZARDOUS WASTE</h1>
        <h2 class="HWH2">FEDERAL LAWS PROHIBIT IMPROPER DISPOSAL</h2>
        <h3
          class="HWH3"
        >IF FOUND, CONTACT THE NEAREST POLICE OR PUBLIC SAFETY AUTHORISTY OR THE U.S. ENVIRONMENTAL PROTECTION AGENCY</h3>
        <h2 class="HWH2 HWGen">GENERATOR INFORMATION:</h2>
        <div class="row no-gutters">
          <h3 class="HWH3 HWBody col-2">NAME</h3>
          <span class="text-info col-10">{{facility}}</span>
        </div>
        <div class="row no-gutters">
          <h3 class="HWH3 HWBody">ADDRESS</h3>
        </div>
        <div class="row no-gutters">
          <h3 class="col-7 HWH3 HWBody">CITY</h3>
          <h3 class="col-2 HWH3 HWBody">STATE</h3>
          <h3 class="col-3 HWH3 HWBody">ZIP</h3>
        </div>
        <div class="row no-gutters">
          <div class="col-7">
            <div class="row no-gutters">
              <h3 class="col-3 HWH3 HWBody">
                EPA
                <br>ID NO.
              </h3>
              <span class="col text-info align-self-end">{{epaID}}</span>
            </div>
          </div>
          <div class="col-5">
            <div class="row no-gutters">
              <h3 class="col-5 HWH3 HWBody">
                EPA
                <br>WASTE NO.
              </h3>
              <span class="col text-info align-self-end">{{wasteNumber}}</span>
            </div>
          </div>
        </div>
        <div class="row no-gutters">
          <div class="col-7">
            <div class="row no-gutters">
              <h3 class="col-5 HWH3 HWBody">
                ACCUMULATION
                <br>START DATE
              </h3>
              <span class="col-7 text-info align-self-end">{{asd}}</span>
            </div>
          </div>
          <div class="col-5">
            <div class="row no-gutters">
              <h3 class="col-7 HWH3 HWBody">
                MANIFEST
                <br>DOCUMENT NO.
              </h3>
              <span class="col-5 text-info align-self-end">{{manifest}}</span>
            </div>
          </div>
        </div>
        <div
          class="row no-gutters justify-content-center align-items-center no-gutters"
          style="margin-top: -10px;"
        >
          <div class="col-1" style="font-size: 75px;">[</div>
          <div
            class="col m-0 p-0 text-info text-center align-self-end"
            style="font-size: 25px; line-height: 1;"
          >
            <p>{{psn}}</p>
          </div>
          <div class="col-1 text-right" style="font-size: 75px;">]</div>
        </div>
        <h3
          class="HWH3"
          style="width: 100%; font-size: 12px; margin-top: -5px;"
        >D.O.T. PROPER SHIPPING NAME AND UN OR NA NO. WITH PREFIX</h3>
        <h1 class="HWH1" style="font-size: 35px; margin: 1px;">HANDLE WITH CARE!</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HWLabel",
  data: function() {
    return {};
  },
  props: {
    facility: String,
    epaID: String,
    wasteNumber: Array,
    asd: String,
    manifest: String,
    psn: String
  }
};
</script>

<style scoped>
.HWLabel {
  width: 500px;
  height: 500px;
  padding: 10px;
  background: repeating-linear-gradient(
    45deg,
    yellow,
    yellow 10px,
    firebrick 10px,
    firebrick 20px
  );
}
.HWInset {
  width: 480px;
  height: 480px;
  background-color: yellow;
  padding: 15px;
}
.HWOutset {
  width: 520px;
  height: 520px;
  background-color: yellow;
  padding: 10px;
}
.HWH1 {
  font-weight: 900;
  text-align: center;
  color: firebrick;
  font-size: 43px;
  margin-top: -10px;
}
.HWH2 {
  text-align: center;
  color: black;
  font-weight: 900;
  font-size: 15px;
}
.HWH3 {
  margin: auto;
  width: 285px;
  text-align: center;
  font-weight: bold;
  color: black;
  font-size: 13px;
  line-height: 1 rem;
}
.HWGen {
  text-align: left;
  margin: 10px 0px;
}
.HWBody {
  width: 100%;
  font-weight: 400;
  text-align: left;
  margin: 3px 0px;
}
.text-info {
  font-size: 13px;
  padding-bottom: 1px;
}
@media print {
  .HWOutset {
    border: 2px solid black;
  }
}
</style>
