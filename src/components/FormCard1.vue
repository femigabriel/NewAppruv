<template>
  <div class="login-card">
    <header class="login-header">
      <h1 id="page-title">Create Account</h1>
    </header>
    <div class="form-row">
      <div class="form-container">
        <div class="form-group">
          <div class="form-label">
            <label for="business-name" class="control-label">
              Registered Business Name
            </label>
          </div>
          <div class="form-label">
            <input
              id="business-name"
              type="text"
              class="form-control"
              name="user.attributes.businessName"
              errormessage="Please enter business name"
              required=""
            />
          </div>
        </div>
      </div>

      <div class="form-container">
        <div class="form-group">
          <div class="form-label">
            <label for="business-address" class="control-label"
              >Business Address</label
            >
          </div>
          <div class="form-input">
            <input
              type="text"
              id="business-address"
              class="form-control"
              name="user.attributes.businessAddress"
              errormessage="Please enter business address"
              required=""
            />
          </div>
        </div>
      </div>
    </div>
    <div class="form-group">
      <div class="form-label">
        <label for="business-description" class="control-label">
          What is your Business about?
        </label>
      </div>
      <div class="form-input">
        <textarea
          id="business-description"
          type="text"
          class="form-control"
          rows="4"
          name="user.attributes.businessDescription"
          errormessage="Please enter business description"
          required=""
        ></textarea>
      </div>
    </div>

    <div class="form-group">
      <div class="form-label">
        <label class="control-label"> What's your role at this company? </label>
      </div>
      <div class="form-input" style="margin-top: 5px">
        <div class="custom-control custom-radio">
          <input
            id="rd-1"
            type="radio"
            name="user.attributes.companyRole"
            class="custom-control-input role-radio"
            value="Company administrator / Senior manager"
          />
          <label class="custom-control-label" for="rd-1"
            >Company administrator / Senior manager</label
          >
        </div>
        <div class="custom-control custom-radio">
          <input
            id="rd-2"
            type="radio"
            name="user.attributes.companyRole"
            class="custom-control-input role-radio"
            value="Employee / Contractor"
          />
          <label class="custom-control-label" for="rd-2"
            >Employee / Contractor</label
          >
        </div>
        <div class="custom-control custom-radio">
          <input
            id="rd-3"
            type="radio"
            name="user.attributes.companyRole"
            class="custom-control-input role-radio"
            value="Director / Owner"
          />
          <label class="custom-control-label" for="rd-3"
            >Director / Owner</label
          >
        </div>
        <div class="custom-control custom-radio">
          <input
            id="rd-4"
            type="radio"
            name="user.attributes.companyRole"
            class="custom-control-input role-radio"
            value="Software Developer / Engineer"
          />
          <label class="custom-control-label" for="rd-4"
            >Software Developer / Engineer</label
          >
        </div>
      </div>
      <div class="d-input">
        <input
          id="companyRole"
          type="text"
          class="form-control hidden"
          errormessage="Please select a company role"
          required=""
        />
      </div>
    </div>

    <div class="form-group">
      <div class="form-label">
        <label class="control-label">
          What products are you interested in?
        </label>
      </div>
      <div class="form-input" style="margin-top: 5px">
        <div class="custom-control custom-checkbox custom-control-inline">
          <input
            id="ck-1"
            type="checkbox"
            class="custom-control-input products-input"
            value="Appruve Identity"
          />
          <label class="custom-control-label" for="ck-1"
            >Appruve Identity</label
          >
        </div>
        <div class="custom-control custom-checkbox custom-control-inline">
          <input
            id="ck-2"
            type="checkbox"
            class="custom-control-input products-input"
            value="Appruve Agency"
          />
          <label class="custom-control-label" for="ck-2">Appruve Agency</label>
        </div>
        <div class="custom-control custom-checkbox custom-control-inline">
          <input
            id="ck-3"
            type="checkbox"
            class="custom-control-input products-input"
            value="Appruve Business"
          />
          <label class="custom-control-label" for="ck-3"
            >Appruve Business</label
          >
        </div>
        <div class="custom-control custom-checkbox custom-control-inline">
          <input
            id="ck-4"
            type="checkbox"
            class="custom-control-input products-input"
            value="Appruve Financial"
          />
          <label class="custom-control-label" for="ck-4"
            >Appruve Financial</label
          >
        </div>
      </div>
      <div class="d-input">
        <input
          id="products"
          type="text"
          name="user.attributes.products"
          class="form-control hidden"
          errormessage="Please select a product"
          required=""
        />
      </div>
    </div>

    <div class="form-group">
      <div class="form-input" style="margin-top: 30px">
        <div class="custom-control custom-checkbox custom-control-inline">
          <input
            id="privacy"
            type="checkbox"
            checked="checked"
            class="custom-control-input"
            errormessage="Please agree to our privacy policy"
            required=""
          />
          <label class="custom-control-label" for="privacy">
            I agree to Appruve's
            <a href="https://appruve.co/privacy/">Privacy Policy</a>
          </label>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    previous() {
      this.$emit("previous");
    },
  },
};
</script>

<style>
.form-row {
 display: flex;
 flex-wrap: wrap;
    margin-right: -5px;
    margin-left: -5px;
}
.form-horizontal .form-group {
    margin-right: -20px;
    margin-left: -20px;
}

 
</style>
