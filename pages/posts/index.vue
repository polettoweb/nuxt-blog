<template>
    <div class="posts-page">
        <PostList :posts="loadedPosts"/>
    </div>
</template>
<script>
import PostList from '@/components/Posts/PostList'
export default {
    components: {
        PostList
    },
    asyncData(context, callback) {
        setTimeout(() => {
        callback(null, {
            loadedPosts: [
            {id: '1', title: 'First Post', previewText: 'This is my first post', thumbnail: 'https://techcrunch.com/wp-content/uploads/2015/04/codecode.jpg'},
            {id: '2', title: 'Second Post', previewText: 'This is my second post', thumbnail: 'https://techcrunch.com/wp-content/uploads/2015/04/codecode.jpg'}
            ]
        })    
        }, 1500)
    },
}
</script>

<style scoped>
.posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
