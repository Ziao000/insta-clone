<template>
    <div class="card">
        <div class="card-img">
            <h1>{{ post.name }}</h1>
            <img :src="post.imgUrl" alt="">
        </div>
        <div class="card-content">
            <h2>{{ post.title }}</h2>
            <p>{{ post.content }}</p>
        </div>
       
            <button v-on:click="() => this.$emit('like', post)" class="btn">
                <span>{{ post.like }} {{ post.like > 1 ? 'Likes' : 'Like' }}</span>
            </button>
            <p>Commentaires {{ post.commentCount }}</p>
            <div class="comment">
                <div class="comment-content">
                    <h3>{{post.commentName}}</h3>
                    <p>{{ post.comment }}</p>
                    <input type="text" placeholder="Ajouter un commentaires">
                </div>
            </div>
     
    </div>
</template>

<script>
export default{
    name: 'CardComponent',
    props:['post']
}
</script>

<style scoped>
.card {
    align-items: center;
   
    width: 500px;
    height: auto;
    align-items: center;
    border: rgb(73, 73, 73) 2px solid;
    margin: 20px;
    padding: 10px;
}

.card-img{
    width: 100%;
    height: 400px;
}

.card-content{
    padding-top: 100px;
    text-align: center;
    
}

/* .comment-content{

} */
.card-img img{
    width: 100%;
    height: 100%;
}

.btn{
    background-color: #d4008a;
    border: none;
    color: white;
    padding: 20px;
    margin: 20px;
    cursor: pointer;
    transition: .2s;
}

.btn:hover{
    border-radius: 6px;
    background-color: #fff;
    border: #d4008a 2px solid;
    color: #d4008a;
    transition: .2s;
}

</style>