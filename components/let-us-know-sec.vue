<template>
    <div class="flex-sec"><a>
        <div class="let-us-know-sec">
            Discuss how we can enable the<span>DIGITAL TRANSFORMATION!</span>     
        </div>
        </a>
    </div>
</template>

<script>
export default {
    mounted () {
    this.$nextTick(() => {
                        
                          
    })
  }
}
</script>>



<style scoped>
    .flex-sec{
        height: 30vh;
        width: 100%;
        padding: 1vw 5vw;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        background: white;
        transition: 0.5s;
        text-decoration: none;
    }
    .let-us-know-sec{
        text-align: center;
        font-size: 2rem;
        font-weight: 700;
        color: var(--main-black);
        
    }
    a {
        text-decoration: none;
    }
    .flex-sec:hover{
        background: var(--lightBlue);
        cursor: pointer;
    }
    .let-us-know-sec span{
        margin-left: 10px;
        color: var(--linkBlue);
    }
</style>
