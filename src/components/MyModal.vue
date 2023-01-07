<template>
    <div class="myModal_wrapper" v-bind:class="{ 'myModal_closed': closed, 'myModal_open': open,  }">
        <div class="myModal">
            <a v-on:click.prevent="$emit('openM')" href=""><img src="../assets/Vector.png" alt=""></a>
            <div class="myModal_green">
                <div class="myModal_green2"></div>
            </div>
            <div class="myModal_line"></div>
            <div class="myModal_sk1"></div>
            <div class="myModal_sk2"></div>
            <div class="myModal_sk3"></div>
            <div class="myModal_sk4"></div>
            <div class="myModal_sk5"></div>
            <div class="myModal_sk6"></div>
            <div class="myModal_line"></div>
            <button class="myModal_btnDel">Удалить предмет </button>
        </div>
    </div>



</template>


<script>


export default {
    components: {
    },
    name: 'MyModal',
    props: {
        open: {
            type: null,
            default() {
                return null
            }
        }
    },
    data() {
        return {
            closed: true,
        }
    },
    methods: {
       

        
    },
    computed: {
       
    }
}
</script>

<style>
.myModal {
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    bottom: 150px;
    right: 113px;
    box-sizing: border-box;
    width: 250px;
    height: 500px;
    background: rgba(38, 38, 38, 0.5);
    border-left: 1px solid #4D4D4D;
    backdrop-filter: blur(8px);
    z-index: 100;
    transform: rotate(270deg);
    border-radius: 0 8px 8px 0;
    transition: transform 0.15s ease 0s, opacity 0.15s ease 0s;
    z-index: 50;
}



.myModal_closed {
    transition: ease-in 0.5s;
    transform: translateY(-250px);
    opacity: 0;
    z-index: 50;
}

.myModal_open {
    transition: ease-in 0.5s;
    transform: translateY(0px);
    opacity: 1;
    z-index: 50;
}





.myModal a {
    margin-left: 200px;
    margin-top: 18px;
}

.myModal_green {
    position: relative;
    width: 115.56px;
    height: 115.56px;
    background: #7FAA65;
}

.myModal_green2 {
    position: absolute;
    width: 115.56px;
    height: 115.56px;
    left: 14.4px;
    top: -14.4px;
    background: rgba(184, 217, 152, 0.35);
    backdrop-filter: blur(6px);
}

.Mymodal_line {
    width: 220px;
    height: 1px;
    background: #4D4D4D;
}

.myModal_sk1 {
    width: 211px;
    height: 30px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
    border-radius: 8px;
}

.myModal_sk2,
.myModal_sk3,
.myModal_sk4 {
    width: 211px;
    height: 10px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
    border-radius: 4px;
}

.myModal_sk5 {
    width: 180px;
    height: 10px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
    border-radius: 4px;
}

.myModal_sk6 {
    width: 80px;
    height: 10px;
    background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
    border-radius: 4px;
}

.myModal_btnDel {
    width: 220px;
    height: 39px;
    background: #FA7272;
    border-radius: 8px;
    color: white;
    border: none;
    outline: none;
    cursor: pointer;
    margin-bottom: 18px;
}
</style>