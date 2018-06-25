<template>
    <div class="item">
        <div class="siteTitle">{{siteTitle}}</div>
        <div class="siteImage" :style="{backgroundImage: 'url(' + siteImage + ')'}"></div>
        <div class="siteProgress">{{Progress}}</div>
        <div class="siteDescrition">{{siteDescrition}}</div>
        <div class="siteOptions">
            <div class="editSite">Modify</div>
            <div class="hideSite">Hide</div>
            <div class="goToTheSite">Open in new tab</div>
        </div>
        
    </div>
</template>

<script>
    
    export default{
        props: ['siteTitle', 'siteDescrition', 'Progress', 'siteImage', 'id']
    }
</script>

<style scoped>
.item{
  background-color: white;

        box-sizing: border-box;
        width: 280px;
        border: 1px solid #ccc;
        box-shadow: 0 2px 2px #aaa;
        margin: 2px;
}
div{
    background-color: #ccc;
    padding: 3px;
}
.siteTitle, .siteDescrition, .siteProgress, .siteImage, .siteOptions{
    margin-bottom: 1px;
    line-height: 2;
}
.editSite, .hideSite, .goToTheSite{
    border: 1px dotted rgba(29, 29, 83, 0.493);
}
.siteDescrition{
    height: 100px;
}
.siteImage{
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 200px;
}
.siteOptions{
    width: 100%;
  display: flex;
  flex: align-self;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
