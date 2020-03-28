<template>
    <div class="col-3 my-2">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
                <br>
            </div>
        </div>
    </div>
</template>
<script>
export default {
   
}
</script>
<style>
.panel-body{
    font-family:Arial, Helvetica, sans-serif;
    font-size: 24px;
    color: #6e6e6e;
    background-color: antiquewhite;
}
.quote{
    cursor: pointer;
}
.quote:hover{
    background-color:rgb(60, 139, 241);
    color:#fff;
}

</style>