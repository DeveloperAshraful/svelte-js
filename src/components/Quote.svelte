<script>
    import {Form, FormGroup, FormText, Input, Label} from 'sveltestrap';
    let radioGroup;

    let hasError = false;
    let isSuccessVisible = false;
    let submitted = false;

    const errMessage = "All the fields are mandatory";

    function handleSubmit() {
        isSuccessVisible = true;
        setTimeout(function(){
            isSuccessVisible = false;
        }, 4000);
        console.log('submit button');
    }
    function submitBtn() {
        submitted = true;
    }


</script>
<div class="quote-area">
  <h3>Get a free Quote</h3>

  {#if hasError === true}
    <p class="error-alert">{errMessage}</p>
  {:else}
    {#if isSuccessVisible}
      <p class="error-alert">Data updated successfully</p>
    {/if}
  {/if}

  <form on:submit|preventDefault={handleSubmit}>
    <div class="row">
      <div class="col-md-6">
        <FormGroup>
          <Label for="fname">First Name</Label>
          <Input type="text" name="fname" id="fname" placeholder="Enter First Name"/>
        </FormGroup>
      </div>
      <div class="col-md-6">
        <FormGroup>
          <Label for="lname">Last Name</Label>
          <Input type="text" name="lname" id="lname" placeholder="Enter Last Name"/>
        </FormGroup>
      </div>
      <div class="col-md-6">
        <FormGroup>
          <Label for="email">Email</Label>
          <Input type="email" name="email" id="email" placeholder="Enter Email"/>
        </FormGroup>
      </div>
      <div class="col-md-6">
        <FormGroup>
          <Label for="phone">Phone number</Label>
          <Input type="text" name="phone" id="phone" placeholder="Enter phone number"/>
        </FormGroup>
      </div>
      <div class="col-md-12">
        <FormGroup>
          <Label for="message">Message</Label>
          <Input type="textarea" name="message" id="Type Message"/>
        </FormGroup>
      </div>
      <div class="col-md-6">
        <FormGroup>
            <Input type="submit" on:click={submitBtn} name="submit" value="Send"/>
        </FormGroup>
      </div>
    </div>
  </form>


</div>
<style>
  .quote-area {
    position: relative;
    background: #ffffff;
    padding: 30px;
    border-radius: 5px;
  }
  .quote-area h3 {
    font-size: 22px;
    color: #323232;
    font-weight: bold;
    text-transform: uppercase;
    border-bottom: 3px solid #ec1f27;
    padding-bottom: 10px;
    margin-bottom: 15px;
    display: inline-block;
  }

  /*============ Start Responsive ==============*/

  @media (max-width: 767px) {
  }

  @media (max-width: 575px) {
    .quote-area {
      padding: 20px 15px;
    }
  }

  @media (max-width: 479px) {
    .quote-area {
      padding: 20px 10px;
    }
  }


</style>