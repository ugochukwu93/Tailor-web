<template>
  
      <div class="footer">
        <div>
            <p class="">
                © Ugochukwu. {{new Date().getFullYear()}}
            </p>
        </div>
        <div>
            <img 
            src="../assets/img/facebook2.png"
            />
        </div>
        <div>
            <img 
            src="../assets/img/instagram2.png"
            />
        </div>
        <div>
            <img 
            src="../assets/img/twitter2.png"
            />
        </div>
        <div>
            <img 
            src="../assets/img/pinterest2.png"
            />
        </div>
      </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.footer {
    display: flex;
    background: #4C4556;
    padding: 25px;
    width: 100%;
    @media(max-width: 600px) {
        width: 100%;
        padding: 10px;
        height: 50px;
    }

    div {
        margin-right: 20px;

        img {
            cursor: pointer;
        }
    }

    div:first-child {
        margin-right: auto;
        color: #fff
    }

}
</style>