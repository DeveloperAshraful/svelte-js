<script>
    import {Form, FormGroup, FormText, Input, Label} from 'sveltestrap';
    let radioGroup;
</script>
<div class="wrapper-area contact-us-area">
  <div class="container">
    <div class="quote-area">
    <h3>Get a free Quote</h3>
    <Form>
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
            <Input type="submit" name="submit" value="Send"/>
          </FormGroup>
        </div>
      </div>
    </Form>
  </div>
  </div>
</div>
<style></style>