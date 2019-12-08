<template>

      <div class="card text-center">
        <div class="card-header text-left">
          <div>{{info.autor}} </div>
          {{info.title}}
        </div>
        <div class="card-body">
          <img  class="card-img-top" :src="info.url" alt="slika">
        </div>
        <div class="card-footer text-left">
           {{info.time}}
        </div>
      </div>







</template>

<script>
export default {
props: ["info"]
}
</script>