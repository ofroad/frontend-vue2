<template>
  <div class="ui card">
  <div class="content">
    <div class="right floated meta" data-garbage="true">{{ item.time | timeAgo }} 之前</div>
    
    <img class="ui avatar image" src="../assets/elliot.jpg"> 
    <router-link :to="'/user/' + item.by">{{ item.by }}</router-link> 
  </div>
  <div class="image">
    <img src="../assets/dog-1.jpg" alt="">
  </div>
  <div class="content">
     <p class="header">{{ item.title }}</p>
    <span class="right floated">
      
      <i class="heart outline like icon"></i>
       {{ item.score }} 喜欢
    </span>
    <i class="comment icon" data-garbage="true"></i>
    <router-link :to="'/item/' + item.id">{{ item.descendants }} 条评论</router-link>
  </div>
  <div class="extra content">
    <div class="ui large transparent left icon input">
      <i class="heart outline icon"></i>
      <input type="text" placeholder="Add Comment...">
    </div>
  </div>
</div>

  

</template>

<script>
export default {
  name: 'news-item',
  props: ['item']
}
</script>

