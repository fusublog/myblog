<template>
  <div class="wrapper">
    <div class="container">
      <div class="row">
        <div class="visible-sm visible-xs col-xs-2 col-sm-3"
             id="smallmenu">
          <div class="hamburger"
               @click="changemen">
            <svg-icon iconClass="menu" />
          </div>
          <ul class="dropdown-menu"
              :style="show? 'display:block': ''">
            <li>
              <svg-icon iconClass="home" /><a href="#">首页</a></li>
            <li>
              <svg-icon iconClass="studly" /><a href="#">学习</a></li>
            <li>
              <svg-icon iconClass="live" /><a href="#">生活</a></li>
            <li>
              <svg-icon iconClass="login" /><a href="#">登录/注册</a></li>
          </ul>
        </div>
        <div class="col-sm-6 col-xs-8 col-md-3 col-lg-4"
             id="blog_logo">
          <img src="@/assets/logo.png"
               alt="">
        </div>
        <div class="visible-sm visible-xs col-xs-2 col-sm-3 serch"
             id="small_search">
          <div class="search">
            <svg-icon iconClass="search" />
          </div>
        </div>
        <div class="col-md-9 col-lg-8 hidden-sm hidden-xs"
             id="options_bar">
          <div class="menu">
            <div class="home">
              <svg-icon iconClass="home" />
              <span class="text">首页</span>
            </div>
            <div class="studly">
              <svg-icon iconClass="studly" />
              <span class="text">学习</span></div>
            <div class="live">
              <svg-icon iconClass="live" />
              <span class="text">生活</span></div>
          </div>
          <form class="navbar-form navbar-left"
                role="search">
            <div class="form-group">
              <input type="text"
                     class="form-control"
                     placeholder="Search">
            </div>
            <button type="submit"
                    class="btn btn-default">Submit</button>
          </form>
          <div class="login_res">
            <div class="res">
              <span class="text">注册</span></div>
            <div class="login">
              <span class="text">登录</span></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      show: false
    }
  },
  methods: {
    changemen () {
      this.show = !this.show
    }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  background-color: #00c58e;
}
.container {
  height: 60px;
}
.row {
  height: 100%;
}
#blog_logo {
  min-width: 60px;
  text-align: center;
  img {
    display: block;
    width: 60px;
    height: 60px;
  }
}
#options_bar {
  display: flex;
  justify-content: space-between;
  height: 100%;
  .menu {
    flex-grow: 3;
    div {
      display: inline-block;
      box-sizing: border-box;
      font-size: 18px;
      padding: 15px 10px;
      line-height: 30px;
      cursor: pointer;
    }
  }
  .navbar-form {
    flex-grow: 2;
    margin: 0;
    display: flex;
    align-items: center;
    .form-group {
      margin-right: 5px;
    }
  }
  .login_res {
    flex-grow: 1;
    text-align: center;
    div {
      display: inline-block;
      box-sizing: border-box;
      font-size: 18px;
      padding: 15px 10px;
      line-height: 30px;
      cursor: pointer;
    }
  }
}
#smallmenu,
#small_search {
  height: 100%;
  .hamburger,
  .search {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
}
.dropdown-menu {
  margin: 0;
  li {
    display: flex;
    height: 50px;
    align-items: center;
    font-size: 18px;
    padding: 10px 0px 10px 10px;
    box-sizing: border-box;
    a {
      width: 100%;
      height: 100%;
      box-sizing: border-box;
    }
  }
}
@media only screen and (min-width: 692px), (max-width: 892px) {
  #options_bar {
    .menu {
      div {
        font-size: 16px;
      }
    }
    .login_res {
      div {
        font-size: 16px;
      }
    }
  }
  #blog_logo {
    min-width: 60px;
    display: flex;
    justify-content: center;
  }
}
@media only screen and (max-width: 691px) {
  .wrapper {
    background-color: #00c58e;
  }
  .container {
    height: 40px;
  }
  .row {
    height: 100%;
  }
  #blog_logo {
    min-width: 40px;
    display: flex;
    justify-content: center;
    img {
      display: block;
      width: 40px;
      height: 40px;
    }
  }
}
</style>