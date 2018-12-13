<template>
    <div class="landing_A">
        <!-- wwManager:start -->
        <wwSectionEditMenu v-bind:sectionCtrl="sectionCtrl"></wwSectionEditMenu>
        <!-- wwManager:end -->

        <wwObject class="background" v-bind:ww-object="section.data.background" ww-category="background"></wwObject>
        
        <div class="container-fluid">

            <div class="row">
                <div class="logo-big-container">
                    <wwObject v-bind:ww-object="section.data.logoBig"></wwObject>
                </div>

                <h1 class="title block">
                    <wwObject v-bind:ww-object="section.data.title"></wwObject>
                </h1>

                <h2 class="subtitle block">
                    <wwObject v-bind:ww-object="section.data.subtitle"></wwObject>
                </h2>

                <h3 class="subtitle block">
                    <wwObject v-bind:ww-object="section.data.subtitle2"></wwObject>
                </h3>

                <div class="button-container block">
                    <wwObject v-bind:ww-object="section.data.button"></wwObject>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: "landing_A",
    props: {
        sectionCtrl: Object
    },
    data() {
        return {}
    },
    computed: {
        section() {
            return this.sectionCtrl.get();
        }
    },
    created() {
        this.section.data = this.section.data || {}
        // this.section.data = {"isNew":false,"title":{"data":{"popup":null},"font":"","link":"","size":"text-big","text":{"fr_FR":"Welcome To Your Fabulous Website"},"type":"text","zoom":-1,"align":"","class":["ww-animspeed-normal","ww-anim-fade-top-bounce"],"image":"/img/no_image_selected.png","ratio":-1,"colors":{"color":null,"borderColor":"","backgroundColor":""},"hidden":false,"position":{"x":0,"y":0},"uniqueId":0.06710339192416104},"button":{"data":{"popup":null},"font":"","link":"section://1035","size":"","text":{"fr_FR":"Start Now !"},"type":"text","zoom":-1,"align":"","class":["ww-class-btn-bg-none","ww-class-btn-padding-small","ww-class-btn-border-small","ww-class-btn-format-round-small","ww-anim-fade","ww-class-font-size-small"],"image":"/img/no_image_selected.png","ratio":-1,"colors":{"color":"#FFFFFF","borderColor":"#FFFFFF","backgroundColor":"#FFFFFF"},"hidden":false,"position":{"x":0,"y":0},"uniqueId":0.7809282019898562},"logoBig":{"data":{"popup":null},"font":"","link":null,"size":"","text":{"fr_FR":""},"type":"text","zoom":0.436374624713393,"align":"","class":["ww-anim-fade","ww-animspeed-slow"],"image":"https://wewebprod.s3-eu-west-1.amazonaws.com/designs/46/sections/1VnU4mJYqI0QOzZqLNBJbJs2UY3L0VRJ.png","ratio":-1,"colors":{"color":"","borderColor":"","backgroundColor":""},"hidden":false,"position":{"x":-1.9373391779708982e-14,"y":0.5655042575474689},"uniqueId":0.8381540437461199},"subtitle":{"data":{"popup":null},"font":"sans-serif","link":"","size":"text-small","text":{"fr_FR":"This section is called a \"landing page\". It is the first page seen by your visitors.<br>A large picture, impactful text, your logo at the top (optional) and a call to action button at the bottom (recommended!).<br><br>Hit the pen to start editing.<br>"},"type":"text","zoom":-1,"align":"center","class":["ww-anim-fade","ww-animspeed-normal"],"image":"/img/no_image_selected.png","ratio":-1,"colors":{"color":"","borderColor":"","backgroundColor":""},"hidden":false,"position":{"x":0,"y":0},"uniqueId":0.7936393689745822},"subtitle2":{"data":{"popup":null},"font":"","link":"","size":"","text":{"fr_FR":""},"type":"text","zoom":-1,"align":"","class":[],"image":"/img/no_image_selected.png","ratio":-1,"colors":{"color":"","borderColor":"","backgroundColor":""},"hidden":false,"position":{"x":0,"y":0},"uniqueId":0.4431173787051501},"background":{"data":{"popup":null},"font":"","link":null,"size":"","text":{"fr_FR":""},"type":"text","zoom":-1,"align":"","class":["ww-class-img-filter-uni-big"],"image":"https://wewebprod.s3-eu-west-1.amazonaws.com/designs/46/sections/3eHa5RHVGPCNovdVTJuDlmz6tVwsXGTU.jpg","ratio":-1,"colors":{"color":"","borderColor":"","backgroundColor":""},"hidden":false,"position":{"x":0,"y":0},"uniqueId":0.34482088449480486},"titleStyle":{"size":"text-xbig"},"sectionTitle":"landing","subtitleStyle":{"size":"text-small"}};

        if (!this.section.data.background)
            this.section.data.background = wwLib.wwObject.getDefault({ type: 'ww-color' });

        if (!this.section.data.logoBig)
            this.section.data.logoBig = wwLib.wwObject.getDefault({ type: 'ww-image' });

        if (!this.section.data.title)
            this.section.data.title = wwLib.wwObject.getDefault({ type: 'ww-text' });

        if (!this.section.data.subtitle)
            this.section.data.subtitle = wwLib.wwObject.getDefault({ type: 'ww-text' });

        if (!this.section.data.subtitle2)
            this.section.data.subtitle2 = wwLib.wwObject.getDefault({ type: 'ww-text' });

        if (!this.section.data.button)
            this.section.data.button = wwLib.wwObject.getDefault({ type: 'ww-button' });

        this.sectionCtrl.update(this.section);
    },
    methods: {}
};
</script>

<style scoped>
.landing_A {
    position: relative;
    flex-basis: 100%;
    /* overflow: hidden; */
}

.landing_A.container-fluid {
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
}

.landing_A .background {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
}

.landing_A .logo-big-container {
    margin-top: 50px;
}

.landing_A .title {
    margin-top: 5%;
}

.landing_A .subtitle {
    margin-top: 2%;
    margin-bottom: 2%;
}

.landing_A .navigation {
    display: table;
    table-layout: fixed;
    margin-top: 30px;
}

.landing_A .navigation a {
    display: table-cell;
    width: 2%;
    text-align: center;
    color: white;
    text-decoration: none;
    text-transform: capitalize;
    border-bottom: 2px solid transparent;
    -webkit-transition: all 0.2s ease;
    -moz-transition: all 0.2s ease;
    -ms-transition: all 0.2s ease;
    -o-transition: all 0.2s ease;
    transition: all 0.2s ease;
}

.landing_A .navigation a:hover {
    border-bottom: 2px solid white;
}

.landing .block {
    position: relative;
    width: 100%;
    min-height: 1px;
    padding-right: 15px;
    padding-left: 15px;
    -ms-flex: 0 0 100%;
    flex: 0 0 100%;
    max-width: 100%;
}

.landing_A .title {
    width: 80%;
    margin-left: 10%;
    margin-right: 10%;
    color: white;
    text-align: center;
}

.landing_A .subtitle {
    width: 80%;
    margin-left: 10%;
    margin-right: 10%;
    margin-top: 10px;
    margin-bottom: 10px;
    color: white;
    text-align: center;
}

.landing_A .button-container {
    display: flex;
    justify-content: center;
    width: 100%;
}

@media (max-width: 768px) {
    .landing_A .navigation {
        display: none;
    }
    .landing_A>.edit-image-button {
        right: 60px !important;
    }
    .landing_A .title {
        margin-top: 15%;
    }
}

.landing_A .section-edit {
    top: 5px !important;
}

.landing_A .picture-button {
    margin-right: 40px;
}

.landing_A .row {
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    margin-right: -15px;
    margin-left: -15px;
}

@media (min-width: 480px) {
    .landing_A .logo-big-container {
        -ms-flex: 0 0 83.333333%;
        flex: 0 0 83.333333%;
        max-width: 83.333333%;
        margin-left: 8.333333%;
    }
}

@media (min-width: 768px) {
    .landing_A .logo-big-container {
        -ms-flex: 0 0 66.666666%;
        flex: 0 0 66.666666%;
        max-width: 66.666666%;
        margin-left: 16.666666%;
    }
}

@media (min-width: 960px) {
    .landing_A .logo-big-container {
        -ms-flex: 0 0 50%;
        flex: 0 0 50%;
        max-width: 50%;
        margin-left: 25%;
    }
}

</style>
