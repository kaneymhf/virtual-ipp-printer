<template>
  <div class="home">
    <div class="device">
      <div style="float: left; width: 30%">
        <h3>Device</h3>

        <img class="logo" v-if="this.mfp == true" alt="Vue logo" src="../assets/mfp.png">
        <img class="logo" v-if="this.mfp == false" alt="Vue logo" src="../assets/no_mfp.png">

      </div>
      <div style="float: right; width: 65%" >
        <h3>INFO</h3>

        <table id="info" style="width: 80%">
          <tbody>
            <tr>
              <td style="width: 30%">Name</td>
              <td>Virtual IPP Printer</td>
            </tr>
            <tr>
              <td>Status</td>
              <td>Ready</td>
            </tr>
          </tbody>
        </table>

        <h3>Paper</h3>

        <table id="info" style="width: 80%">
          <tbody>
            <tr>
              <td style="width: 30%">Size</td>
              <td colspan="2">A1</td>
            </tr>
            <tr>
              <td>Capacity</td>
              <td colspan="2">{{ this.paper_value }} / 500 </td>
            </tr>
            <tr>
              <td>Level</td>
              <td style="width: 20%">
                {{ paper_level }}%
              </td>
              <td>
                <div class="progress">
                  <div class="progress-bar main"
                  :style="paper_style"
                  >
                  </div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>

        <h3>Toner</h3>

        <table id="info" style="width: 80%">
          <tbody>
            <tr>
              <td style="width: 30%">Black</td>
              <td style="width: 20%">
                {{ toner_level }}%
              </td>
              <td>
                <div class="progress">
                  <div class="progress-bar black"
                  :style="toner_style"
                  >
                  </div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    mfp: Boolean,
    color: Boolean,
    toner_value: Number,
    paper_value: Number,
  },
  computed: {
    paper_level() {
      return ((this.paper_value / 500) * 100).toFixed(2);
    },
    paper_style() {
      return `width: ${this.paper_level}%`;
    },
    toner_level() {
      return ((this.toner_value / 100) * 100).toFixed(2);
    },
    toner_style() {
      return `width: ${this.toner_level}%`;
    },
  },
};
</script>
