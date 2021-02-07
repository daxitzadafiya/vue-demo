<template>
  <div>
    <b-container fluid>
      <table>
        <tr>
          <td>
            <label for="CustName" class="font-weight-bold"
              >CUSTOMER NAMES :</label
            >
          </td>
          <td class="mb-5">
            <b-form-input
              id="CustName"
              placeholder="enter customer name"
            ></b-form-input>
          </td>
        </tr>
        <tr>
          <td>
            <label for="CustName" class="font-weight-bold"
              >PO / JOB NAME :</label
            >
          </td>
          <td>
            <b-form-input
              id="CustName"
              placeholder="enter po / job name"
            ></b-form-input>
          </td>
        </tr>
        <tr>
          <td>
            <label for="CustName" class="font-weight-bold">UNIT #</label>
          </td>
          <td>
            <b-form-input id="CustName" placeholder="enter unit"></b-form-input>
          </td>
        </tr>
      </table>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ""
    };
  }
};
</script>
