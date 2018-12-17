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

        if (!this.section.data.background)
            this.section.data.background = wwLib.wwObject.getDefault({ type: 'ww-color' });

        if (!this.section.data.logoBig)
            this.section.data.logoBig = wwLib.wwObject.getDefault({ type: 'ww-image' });

        if (!this.section.data.title)
            this.section.data.title = wwLib.wwObject.getDefault({ type: 'ww-text', data: { color: 'black' } });

        if (!this.section.data.subtitle)
            this.section.data.subtitle = wwLib.wwObject.getDefault({ type: 'ww-text', data: { color: 'black' } });

        if (!this.section.data.subtitle2)
            this.section.data.subtitle2 = wwLib.wwObject.getDefault({ type: 'ww-text', data: { color: 'black' } });

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
    overflow: hidden;
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
