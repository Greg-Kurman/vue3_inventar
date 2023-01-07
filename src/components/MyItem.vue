<template>
    <div class="myItem">
        <div class="myItem_img">
            <img src="`../assets/${{color}}.png`" alt="">
            <div  v-bind:class="color"> </div>
            {{ color }}
        </div>
        <div class="myItem_count">
            {{ count }}
        </div>
    </div>

</template>


<script>
export default {
    name: 'MyItem',
    props: {
        color: {
            type: String,
        }
    },
    emits: {
    },
    data() {
        return {
            count: 5
        }
    }

}
</script>

<style>
.myItem {
    margin-left: 10.5px;
    position: relative;
    width: 95px;
    height: 105.9px;
    cursor: pointer;
}

.myItem_img {
    position: absolute;
    top: 25%;
    left: 25%;
}

.myItem_img img {
    width: 48px;
    height: 48px;
}

.img2 {
    width: 48px;
    height: 48px;
    position: absolute;
    top: -10%;
    left: -10%;
    background: rgba(217, 187, 152, 0.35);
    backdrop-filter: blur(6px);
}

.myItem_count {
    color: white;
    position: absolute;
    top: 0px;
    right: 0px;
    width: 15px;
    height: 16px;
    background: #262626;
    border: 1px solid #4D4D4D;
    border-radius: 6px 0px 0px 0px;
    transform: rotate(270deg);
}

.red {
    width: 48px;
    height: 48px;
    position: absolute;
    top: -10%;
    left: -10%;
    background: rgba(217, 187, 152, 0.35);
    backdrop-filter: blur(6px);
}

.green {
    width: 48px;
    height: 48px;
    position: absolute;
    top: -10%;
    left: -10%;
    background: rgba(184, 217, 152, 0.35);
    backdrop-filter: blur(6px);
}

.purple {
    width: 48px;
    height: 48px;
    position: absolute;
    top: -10%;
    left: -10%;
    background: rgba(116, 129, 237, 0.35);
    backdrop-filter: blur(6px);
}
</style>