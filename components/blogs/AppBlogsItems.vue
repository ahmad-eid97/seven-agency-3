<template>
  <div class="blog-area pt-100 pb-70">
    <div class="container">
      <div class="section-title text-center">
        <span class="sp-color2">Latest Blog</span>
        <h2>Let’s Check Some Latest Blog</h2>
        <div class="heading-spacer">
          <i class="fa-solid fa-angle-down"></i>
        </div>
      </div>
      <div class="row pt-45" v-if="blogs.blogs.length >= 1">
        <div
          v-for="blog in blogs.blogs"
          :key="blog.id"
          class="col-lg-4 col-md-6"
          @click="$router.push(localePath(`/blog/${blog.id}`))"
        >
          <div class="blog-card">
            <div class="blog-img">
              <router-link to="blog">
                <img :src="blog.image" alt="Blog Images" />
              </router-link>
              <div class="blog-tag">
                <h3>{{ $date(new Date(blog.publish_date), "dd") }}</h3>
                <span>{{ $date(new Date(blog.publish_date), "MMM") }}</span>
              </div>
            </div>
            <h3 class="title">
              <router-link to="blog">{{ blog.title }}</router-link>
            </h3>
            <div class="content">
              <ul>
                <li>
                  <a href="#"><i class="fa-regular fa-user"></i> By Admin</a>
                </li>
                <li>
                  <a href="index.html"
                    ><i class="fa-solid fa-tag"></i> Business</a
                  >
                </li>
              </ul>
              <p>{{ blog.description }}</p>
            </div>
          </div>
        </div>
        <div class="col-lg-12 col-md-12 text-center">
          <div class="pagination-area">
            <a href="#" class="page-numbers">
              <i class="fa-solid fa-arrow-left"></i>
            </a>
            <span class="page-numbers current" aria-current="page">1</span>
            <a href="#" class="page-numbers">2</a>
            <a href="#" class="page-numbers">3</a>
            <a href="#" class="page-numbers">
              <i class="fa-solid fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppBlogsItems",
  props: ["blogs"],
};
</script>

<style>
.blog-area .section-title span {
  margin-bottom: 8px;
  font-weight: 600;
  display: block;
  color: #f3615a;
}
.blog-area .section-title h2 {
  font-weight: 400;
  line-height: 41.6px;
  letter-spacing: 1px;
  text-transform: capitalize;
  margin-bottom: 20px;
}

.blog-card {
  background-color: #fff;
  -webkit-box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
  margin-bottom: 30px;
  border-radius: 0;
  -webkit-transition: 0.9s;
  transition: 0.9s;
  border: 3px solid #f3615a;
  transform: translateY(0px);
  height: 100%;
}
.blog-card:hover {
  transform: translateY(-15px);
  box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
  -webkit-box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
  -moz-box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
}
.blog-card .blog-img {
  position: relative;
  margin: 0 0 -30px;
  z-index: 0;
}
.blog-card:hover .blog-img {
  margin: 0 0 0;
}
.blog-card .blog-img img {
  border-radius: 0;
  height: 250px;
  width: 100%;
}
.blog-card .blog-img .blog-tag {
  position: absolute;
  top: -10px;
  right: 30px;
  text-align: center;
  border: 3px solid #f3615a;
  background-color: #fff;
  padding: 15px 12px;
  border-radius: 0;
  text-align: center;
}
.blog-card:hover .blog-img .blog-tag {
  position: absolute;
  top: -20px;
  right: 30px;
  text-align: center;
  background-color: #f3615a;
  padding: 15px 12px;
  border-radius: 0px;
  text-align: center;
}
.blog-card .blog-img .blog-tag h3 {
  font-size: 27px;
  color: #f3615a;
  line-height: 1;
  margin-bottom: 0;
  font-weight: 500;
}
.blog-card:hover .blog-img .blog-tag h3 {
  font-size: 27px;
  color: #fff;
  line-height: 1;
  margin-bottom: 0;
  font-weight: 500;
}
.blog-card .blog-img .blog-tag span {
  color: #f3615a;
  line-height: 1;
  font-weight: 500;
}
.blog-card:hover .blog-img .blog-tag span {
  color: #fff;
  line-height: 1;
  font-weight: 500;
}
.blog-card .content ul li a {
  color: #f3615a;
}
.blog-card .content ul li a i {
  font-size: 20px;
  color: #f3615a;
  margin-right: 5px;
  position: relative;
  top: 3px;
}
.blog-card .content {
  padding: 25px 30px;
}
.blog-card .content ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
}
.blog-card .content ul li {
  display: inline-block;
  font-size: 15px;
}
.blog-card h3.title {
  font-size: 22px;
  padding: 10px 30px;
  background: #f3615a;
  text-align: center;
  position: relative;
  z-index: 1;
}
.blog-card h3.title a {
  color: #fff;
}
.blog-card .content p {
  margin-bottom: 8px;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
