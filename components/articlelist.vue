<template>
  <div class="article_list">
    <div class="header">
      <svg-icon iconClass="article" />
      <span class="text">文章列表</span>
    </div>
    <div class="list">
      <div class="article_content"
           v-for="(index) in 5"
           :key="index">
        <div class="image">
          <img src="@/assets/avtor.jpg"
               alt="">
        </div>
        <div class="article_text">
          <div class="title">node是个好东西</div>
          <div class="content">好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习
            好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习
            好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习好好学习
            好好学习好好学习好好学习
          </div>
          <div class="info">作者信息</div>
          <div class="label-y">标签1，标签2</div>
        </div>
      </div>
    </div>
    <nav aria-label="Page navigation"
         class="navigation">
      <ul class="pagination">
        <li>
          <a href="#"
             aria-label="Previous">
            <span aria-hidden="true">&laquo;</span>
          </a>
        </li>
        <li><a href="#">1</a></li>
        <li><a href="#">2</a></li>
        <li><a href="#">3</a></li>
        <li><a href="#">4</a></li>
        <li><a href="#">5</a></li>
        <li>
          <a href="#"
             aria-label="Next">
            <span aria-hidden="true">&raquo;</span>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.article_list {
  border: 1px solid #66a8f9;
  border-radius: 5px;
}
.header {
  height: 40px;
  border-bottom: 1px solid #66a8f9;
  line-height: 40px;
  padding-left: 20px;
  .text {
    font-size: 20px;
  }
}
.article_content {
  display: flex;
  border-bottom: 1px solid #66a8f9;
}
.image {
  width: 250px;
  padding: 5px;
  img {
    display: block;
    width: 100%;
  }
}
.article_text {
  display: flex;
  width: 250px;
  flex-grow: 1;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10px;
  box-sizing: border-box;
  .title,
  .content,
  .info {
    margin-bottom: 10px;
  }
  .content {
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3; //行数
    -webkit-box-orient: vertical;
  }
}
.navigation {
  display: flex;
  justify-content: center;
}
</style>