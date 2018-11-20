<template>
  <header class="hd-Header">
    <div class="hd-Header_Inner">
      <div class="hd-Header_Body">
        <a class="hd-Header_LogoContainer" href="/">
          <Logo/>
        </a>
        <div class="hd-Header_Navigation">
          <nav class="nav-Navigation">
            <ul class="nav-Navigation_Items">
              <li class="nav-Navigation_Item">
                <a href="/about" class="nav-Navigation_Link">About us</a>
              </li>
              <li class="nav-Navigation_Item">
                <a href="/products" class="nav-Navigation_Link">Our products</a>
              </li>
              <li class="nav-Navigation_Item">
                <a href="/blog" class="nav-Navigation_Link">Blog</a>
              </li>
              <li class="nav-Navigation_Item">
                <a href="/contact" class="nav-Navigation_Link">Contact us</a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  import Logo from '~/assets/svgs/logo.svg'

  export default {
    name: 'index',
    components: {
      Logo,
    }
  }
</script>
