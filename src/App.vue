<template>
    <v-app id="inspire">
        <v-app-bar app elevation="0">
            <v-subheader><h1 class="green--text">Portfolio<span class="pink--text">.in</span></h1></v-subheader>
            <v-tabs center-active right background-color="transparent" active-class="active-tab">
                <v-tab href="#home">Home</v-tab>
                <v-tab>About</v-tab>
                <v-tab>Portfolio</v-tab>
                <v-tab>Blog</v-tab>
                <v-tab>Contact</v-tab>
            </v-tabs>
            <v-btn large color="green" class="white--text ml-10">Fire me an Email</v-btn>
        </v-app-bar>
        <v-main style="background-color: #F5F5F5">
            <section class="intro-section" id="home">
                <v-row class="align-center px-10" style="height: 690px">
                    <v-col lg="6" cols="6" class="pa-6 font-weight-bold py-16">
                        <h2 class="display-3">Visual <span class="green--text">Design</span> & <span class="pink--text">Art</span>
                            Director</h2>
                        <v-subheader>Hi, I am Jack, focusing on creating emotional experiences.</v-subheader>
                        <br>
                        <br>
                        <v-btn large elevation="5" color="green" class="white--text mt-10 px-10 py-5">Hire Me</v-btn>
                        <v-btn large elevation="5" color="pink" class="white--text mt-10 ml-10 px-10 py-5">Contact
                        </v-btn>
                        <v-row class="mt-16">
                            <v-chip class="px-4 ma-3" color="primary">
                                <v-icon left size="20">mdi-facebook</v-icon>
                                Facebook
                            </v-chip>
                            <v-chip class="px-4 ma-3 white--text" color="#01ff56">
                                <v-icon left size="20">mdi-whatsapp</v-icon>
                                Linkedin
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="info">
                                <v-icon left size="20">mdi-linkedin</v-icon>
                                Linkedin
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="dark">
                                <v-icon left size="20">mdi-github</v-icon>
                                Linkedin
                            </v-chip>
                        </v-row>
                    </v-col>
                    <v-col lg="6" cols="6">
                        <v-img src="https://preview.colorlib.com/theme/jackco/assets/img/hero/xhero_right.png.pagespeed.ic.U76_mb-Zcf.webp"></v-img>
                    </v-col>
                </v-row>
            </section>
            <section class="about-me" id="about">
                <v-img class="pa-10" height="400" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-row justify="center" class="align-center">
                        <v-col lg="6" cols="6">
                            <v-card class="text-center pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <v-card-subtitle class="green--text">ABOUT MYSELF</v-card-subtitle>
                                <h2 class="display-1 font-weight-regular">
                                    I’m a Creative director based on New York, who loves clean, simple & unique design.
                                    I also enjoy crafting..
                                </h2>
                                <v-btn large elevation="5" color="pink" class="white--text mt-10 px-10 py-5">Download
                                    Resume
                                    <v-icon>mdi-download</v-icon>
                                </v-btn>
                            </v-card>
                        </v-col>
                        <v-col lg="6" cols="6">
                            <v-card class="pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <div class="py-1" v-for="(item,index) in items" :key="index">
                                    <label>{{ item.title }}</label>
                                    <v-progress-linear
                                            :color="item.color"
                                            height="10"
                                            :value="item.value"
                                    ></v-progress-linear>
                                </div>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-img>
            </section>
            <section class="educaion py-6">
                <v-container>
                    <h4 class="display-2 text-center">Education</h4>
                    <v-row class="py-8">
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>User Experience Designer</h2>
                                        <span>March 2020 - Present</span>
                                    </div>
                                    <a class="green--text">at Dalian University <v-icon color="green">mdi-link</v-icon></a>
                                </div>
                                <v-card-text>
                                    Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna
                                    ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat
                                    justo sed libero varius vulputate.
                                </v-card-text>
                            </v-card>
                        </v-col>
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>UI Designer</h2>
                                        <span>March 2020 - Present</span>
                                    </div>
                                    <a class="green--text">at School of California<v-icon color="green">mdi-link</v-icon></a>
                                </div>
                                <v-card-text>
                                    Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna
                                    ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat
                                    justo sed libero varius vulputate.
                                </v-card-text>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-container>
            </section>
            <section class="experiance py-6">
                <v-img class="pa-10" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-container>
                        <h4 class="display-2 text-center">Experience</h4>
                        <v-timeline>
                            <v-timeline-item v-for="(exper,index) in experience" :key="index"
                                             :color="index % 2 === 0 ?'pink':'green'">
                                <v-card class="rounded-xl">
                                    <v-card-title :color="index % 2 === 0 ?'pink':'green'">
                                        {{exper.title}}
                                    </v-card-title>
                                    <v-card-text>
                                        <b>{{exper.date}}</b><br>
                                        <b>@{{exper.institute}}</b><br>
                                        {{exper.decription}}
                                    </v-card-text>
                                </v-card>
                            </v-timeline-item>
                        </v-timeline>
                    </v-container>
                </v-img>

            </section>
            <section class="portfolio">
                <h4 class="display-2 text-center">Portfolio</h4>
                <v-slide-group
                        class="pa-4"
                        active-class="success"
                        show-arrows
                >
                    <v-slide-item v-for="(slider,index) in sliders" :key="index">
                        <v-card height="250" width="250" class="mx-2">
                            <img height="100%" width="100%" :src="slider" alt="">
                        </v-card>
                    </v-slide-item>
                </v-slide-group>
            </section>
            <section class="contact-us pt-10">
                <v-img class="pt-10" gradient="to bottom, rgb(166 199 156), rgb(227 227 227 / 86%)" src="https://img.freepik.com/free-photo/contact-us_36325-2135.jpg?size=626&ext=jpg">
                    <v-container>
                        <h4 class="display-1 text-center mb-5">
                            I’m a designer, based in San Francisco. Currently a freelancer. You can see my hobbies on @Jack-Co and some photos on me too.
                        </h4>
                        <v-divider />
                        <br>
                        <v-row>
                            <v-col cols="12" lg="6">
                                <v-card-title>DROP A LINE</v-card-title>
                                <v-form>
                                    <v-text-field label="Your Name" />
                                    <v-text-field label="Email" />
                                    <v-text-field label="Subject" />
                                    <v-textarea label="Message" />
                                    <v-btn large color="green" class="white--text">Send Message</v-btn>
                                </v-form>
                            </v-col>
                            <v-col cols="12" lg="3" offset="2">
                                <v-card-title>CONTACT ME</v-card-title>
                                <v-card-text>
                                    4657 Franklin Avenue, ARCH CAPE <br>
                                    +361-883-3218 <br>
                                    hello@jac-co.com <br>
                                </v-card-text>
                                <v-card-actions>
                                    <v-btn large elevation="5" color="pink" class="white--text mt-10 px-10 py-5">Download
                                        Resume
                                        <v-icon>mdi-download</v-icon>
                                    </v-btn>
                                </v-card-actions>
                            </v-col>
                        </v-row>
                    </v-container>
                    <v-footer class="mt-4">
                        <v-col
                                class="text-center"
                                cols="12"
                        >
                            <strong>Copyright ©{{ new Date().getFullYear() }} All rights reserved | This template is made with  by
                                <a href="" class="green--text">Web Burden</a>
                            </strong>
                        </v-col>
                    </v-footer>
                </v-img>
            </section>
        </v-main>
    </v-app>
</template>

<script>
    export default {
        name: 'App',

        data: () => ({
            drawer: null,
            items: [
                {title: 'HTML', value: 100, color: 'light-blue'},
                {title: 'CSS', value: 100, color: 'deep-orange'},
                {title: 'Javascript', value: 70, color: 'light-green'},
                {title: 'Vuejs', value: 80, color: 'blue'},
                {title: 'Vuetify', value: 90, color: 'black'},
                {title: 'PHP', value: 100, color: 'red'},
            ],
            experience: [
                {
                    title: 'User Experience Designer',
                    date: 'March 2020 - Present',
                    institute: 'Web Burden',
                    decription: 'Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.'
                },
                {
                    title: 'UI Designer',
                    date: 'March 2020 - Present',
                    institute: 'Web Burden',
                    decription: 'Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.'
                },
                {
                    title: 'Illustration Artiest',
                    date: 'March 2020 - Present',
                    institute: 'Web Burden',
                    decription: 'Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.'
                },
                {
                    title: 'Graphic Designer',
                    date: 'March 2020 - Present',
                    institute: 'Web Burden',
                    decription: 'Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.'
                },
            ],
            sliders:[
                'https://cdn.searchenginejournal.com/wp-content/uploads/2020/01/which-web-design-platform-is-right-for-you-5e4d59fb941b9-1520x800.png',
                'https://cdn.searchenginejournal.com/wp-content/uploads/2019/12/5-ways-seo-web-design-go-together-5e2945dd5df37.png',
                'https://data.whicdn.com/images/350420216/original.jpg?t=1605047796',
                'https://1zylgb20pxi7mw2sdr8i4a14-wpengine.netdna-ssl.com/wp-content/uploads/2020/01/projectleft.jpg',
                'https://cdn.dribbble.com/users/702789/screenshots/14012516/media/561a8b7e8cbe51c72c18f4ef0dc72676.png?compress=1&resize=400x300',
                'https://cdn.dribbble.com/users/2399102/screenshots/15522177/media/346d890482d929610d316938e7d48629.png?compress=1&resize=400x300',
            ]
        }),
    }
</script>
<style>
    .v-tab.active-tab {
        color: #e91e63;
    }

    .v-tab.active-tab::before {
        background-color: #4caf50;
    }
</style>