<script lang="ts">
    import {Router, Route, Link} from 'svelte-navigator'
    import Home from "../pages/Home.svelte";
    import About from "../pages/About.svelte";
    import Contactus from "../pages/Contactus.svelte";

    import {
        Collapse,
        Navbar,
        NavbarToggler,
        NavbarBrand,
        Nav,
        NavItem,
        NavLink,
        Dropdown,
        DropdownToggle,
        DropdownMenu,
        DropdownItem
    } from 'sveltestrap';

    let isOpen = false;

    function handleUpdate(event) {
        isOpen = event.detail.isOpen;
    }

    let logo = 'assets/images/logo.png';
</script>
<header class="header-area">
  <div class="container">
    <div class="logo">
      <a href="/"><img src={logo} alt="logo"></a>
    </div>
    <Router>
      <nav>
        <Link to="/">Home</Link>
        <Link to="about-us">About us</Link>
        <Link to="contact-us">Contact us</Link>
      </nav>
      <main>
        <Route path="/">
          <Home/>
        </Route>
        <Route path="about-us">
          <About/>
        </Route>
        <Route path="contact-us">
          <Contactus/>
        </Route>
      </main>

      <Navbar color="light" light expand="md">
        <NavbarBrand href="/">sveltestrap</NavbarBrand>
        <NavbarToggler on:click={() => (isOpen = !isOpen)}/>
        <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
          <Nav class="ms-auto" navbar>
            <NavItem>
              <NavLink href="/">Home</NavLink>
            </NavItem>
            <NavItem>
              <NavLink href="/about-us">About Us</NavLink>
            </NavItem>
            <NavItem>
              <NavLink href="/contact-us">Contact Us</NavLink>
            </NavItem>
          </Nav>
        </Collapse>
      </Navbar>

    </Router>

  </div>
</header>
<style>
  .header-area {
    position: relative;
    background: #ffffff;
    border-bottom: 5px solid #EC1F27;
  }

  .logo {
    padding: 15px 0;
    text-align: center;
  }

  .logo img {
    width: auto;
    max-width: 100%;
    height: auto;
    max-height: 64px;
  }
</style>