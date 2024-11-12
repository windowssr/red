<template>
    <div class="Home">
        <div class="text-container">
            <p class="text">中外宏桥是一个连接国内外有人的夸文化桥梁</p>
            <p class="intro-text">
                中国的旅游资源丰富多样，从古老的历史遗址到现代的都市风光，
                从自然景观到人文景观，都深受游客喜爱。无论是长城、故宫，还是桂林山水、黄山风光，都是世界闻名的旅游胜地。
                此外，中国还拥有许多现代化的旅游城市和休闲度假区，提供了丰富的文化和娱乐体验。
            </p>
        </div>
    </div>
    
    
</template>

<script lang='ts' setup name='App'>
    import { RouterLink, RouterView } from 'vue-router';
</script>


<style scoped>
    .Home {
        position: absolute;
        top: 105px;
        left: 50%;
        transform: translateX(-50%);
        width: 100%;
        height: 100%;
        max-width: 1520px;
        height: 95%;
        background-color: rgba(233, 16, 16, 0.8); /* 背景框的背景色，带透明度 */
        border-radius: 0px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        background-size: contain;
        background-repeat: no-repeat;
        /* overflow: hidden; */
    }

    /* 背景图片 */
    .Home::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url('@/assets/home_background.png'); /* 设置背景图片 */
        background-size: contain; /* 图片按比例缩放，使其适应容器大小 */
        background-repeat: no-repeat; /* 不重复图片 */
        overflow: auto; /* 允许内容滚动 */
        /* background-position: center;  */
        z-index: -1; /* 确保背景图层在内容层下 */
    }
    /* 文字容器 */
    .text-container {
        position: absolute;
        top: 580px; /* 控制文字离底部的距离 */
        left: 40%;
        transform: translateX(-50%); /* 使文字居中 */
        z-index: 1; /* 文字层级高于背景 */
        color: rgb(24, 22, 22); /* 文字颜色 */
        font-size: 50px; /* 字体大小 */
        text-align: left; /* 文字居中对齐 */
        padding: 10px;
    }
    /* 文字样式 */
    .text {
        margin: 0; /* 去除默认的外边距 */
        font-size: 40px; /* 可以根据需要调整字体大小 */
        color: rgba(20, 17, 17, 0.9); /* 设置透明的白色文字 */
        font-family: 'Arial', sans-serif; /* 修改字体 */
        font-weight: bold;
        /* background: linear-gradient(45deg, #ff6b6b, #f4a261, #2a9d8f); */
        /* color: transparent; */
        text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), 0px 0px 25px rgba(255, 255, 255, 0.6);
    }
    /* 新增的介绍文本样式 */
    .intro-text {
        font-size: 24px; /* 调整字体大小 */
        color: rgba(255, 255, 255, 0.8); /* 设置文字颜色 */
        margin-top: 20px; /* 给新段落增加间距 */
        line-height: 1.6; /* 增加行间距 */
        text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3); /* 文字阴影 */
    }

    .main-introduce {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(255, 0, 0, 0.5); /* 红色背景，半透明 */
        transform: translateY(30%); /* 将背景向上移动，使其下边缘超过图片 */
        z-index: 0; /* 确保背景在图片上方 */
    }


    .top-nav {
    display: flex;
    justify-content: center;
    background-color: #f8f8f8;
    padding: 10px 0;
    border-bottom: 1px solid #ddd;
    }

    .nav-item {
    margin: 0 15px;
    text-decoration: none;
    color: #e0e405;
    font-size: 16px;
    transition: color 0.3s ease;
    }

    .nav-item:hover {
    color: #64967E;
    }
</style>