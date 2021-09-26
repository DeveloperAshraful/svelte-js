<script lang="ts">
    import { Button, Col, Row } from 'sveltestrap';

    const colors = [
        'primary',
        'secondary',
        'success',
        'danger',
        'warning',
        'info',
        'light',
        'dark'
    ];

    let count = 0;

    let user = { loggedIn: false };

    function toggle() {
        user.loggedIn = !user.loggedIn;
    }

    function incrementCount() {
        count += 1;
    }
    $: doubled = count * 2;


</script>
<div class="nested-area">
  <h3>Nested paragraph</h3>
  <button on:click={incrementCount}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
  </button>

  <p>{count} doubled is {doubled}</p>

  {#if user.loggedIn}
    <button on:click={toggle}>
      Log out
    </button>
  {/if}

  {#if !user.loggedIn}
    <button on:click={toggle}>
      Log in
    </button>
  {/if}
  <br>
  <Row>
    <Col>
      <Button color="primary" outline>Hello World!</Button>
    </Col>
  </Row>


    <div class="mt-5">
      {#each colors as color}
        <Button class="me-2 ms-2" outline {color}>{color}</Button>
      {/each}
    </div>


</div>
