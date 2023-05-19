<link rel="stylesheet" href="../assets/styles/main.sass">
<template>
    <div class="header">
        <div class="container">
            <div class="header__logo">
                <a href="#"><img src="../../public/img/dc-logo.png" alt="logo img"/></a>
            </div>
            <nav class="navbar">
                <ul class="nav-list">
                    <li class="nav-item"><a href="#">CHARACTERS</a></li>
                    <li class="nav-item active"><a href="#">COMICS</a></li>
                    <li class="nav-item"><a href="#">MOVIES</a></li>
                    <li class="nav-item"><a href="#">TV</a></li>
                    <li class="nav-item"><a href="#">GAMES</a></li>
                    <li class="nav-item"><a href="#">COLLECTIBLES</a></li>
                    <li class="nav-item"><a href="#">VIDEOS</a></li>
                    <li class="nav-item"><a href="#">FANS</a></li>
                    <li class="nav-item"><a href="#">NEWS</a></li>
                    <li class="nav-item"><a href="#">SHOP</a></li>
                </ul>
            </nav>
        </div>

    </div>
</template>

<script>
export default {
    name: "AppHeader"
}
</script>

<style lang="sass" scoped>
@import "src/assets/styles/partials/variables"

.container
  max-width: 1400px
  margin: 0 auto
  padding-inline: 10px
  display: flex
  justify-content: space-between

  .navbar
    .nav-list
      font-size: 15px
      list-style: none
      display: flex
      height: 100%
      padding: 0
      margin: 0

      .nav-item
        height: 100%

        a
          text-decoration: none
          height: 100%
          padding: 10px
          display: flex
          place-items: center
          font-weight: bold

        a:active
          color: $color-blue

        &:hover
          border-bottom: 5px solid $color-blue

      .nav-item.active
        border-bottom: 5px solid $color-blue

        a
          color: $color-blue

.header
  padding: 15px

</style>