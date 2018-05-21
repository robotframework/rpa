<template>
    <div class="row no-gutters">
     <div class="col-md-2">
         <navigation-vertical :pages="pages"/>
     </div>

    <div class="col-md-10" id="scroller"
    ref="content" style="position:relative;height:100vh;overflow-y:scroll;overflow-x:hidden;-webkit-overflow-scrolling: touch;">
        <app-header/>
        <page-block v-for="(page, index) in pages"
          v-bind:page="page"
          v-bind:index="index"
          v-bind:key="index"
          class="pl-md-5 px-lg-2 p-sm-3 py-5 p-xs-1"/>
        <app-footer class="mt-0 py-5"/>
      </div>
    </div>
</template>
<script>
import PageBlock from "@/Components/PageBlock.vue";

export default {
  components: {
    PageBlock
  },
  data() {
    return {
      pages: [
        {
          title: "Introduction",
          text_block: true,
          tab_box: false,
          feature_box: false,
          data: {
            text: {
              header: "Introduction",
              text:
                "<p>Robot Framework is an open source robotic process automation (RPA) a solution that is used to automate business processes. It is open and extensible which means that it can be integrated with virtually any other tool to create powerful and flexible RPA solutions.<p>Robot’s core framework is a generic automation platform that is hugely popular in test automation and has an active community of thousands of developers with many industry leading companies using it in their software development. This means that Robot Framework is actively supported and continuously improving.</p><p>The extensibility of Robot Framework is enabled by its modular architecture that builds on top of extension libraries. The Robot Framework community develops and maintains these libraries that provide functionality such as optical image recognition, database access, HTTP APIs, iOS and Android application support, and remote execution. It is also trivially easy to create new libraries out of Python or Java code which enables any user to integrate new functionality into Robot Framework.</p><p>Being open source also means that Robot Framework is free to use without licensing costs and you can run any number of Robot Framework RPA processes in parallel. Orchestration functionality in enterprise scale projects are available through Jenkins plugins.</p>"
            }
          }
        },
        {
          title: "Why choose Robot Framework?",
          text_block: true,
          tab_box: false,
          feature_box: false,
          hide_from_nav: true,
          data: {
            text: {
              header: "Why choose Robot Framework?",
              text:
                "<p>Building RPA solutions is a means to an end. The RPA technology that powers these solutions is an enabling technology that does not provide any value by itself so why should it be expensive and closed?</p>\
                <p>When you choose Robot Framework for your RPA implementation, you are choosing the freedom to extend it in any way you whish and the possibility to run it anywhere and how often you like. Robot Framework is not supported by just one single company but a network of thousands of experts around the world, which means that the future value of your RPA investment will be secured.</p>"
            }
          }
        },
        {
          title: "Comparison",
          text_block: true,
          table_box: true,
          data: {
            text: {
              header: "Comparison between closed and open solutions",
              text: ""
            },

            table: {
              fields: {
                title: {
                  label: " "
                },
                open_solution: {
                  label: "Open solution"
                },
                closed_solution: {
                  label: "Closed solution"
                }
              },
              rows: [
                {
                  title: "Licence costs",
                  open_solution: "None",
                  closed_solution:
                    "Yes, depending on orchestration and number of parallel processes"
                },
                {
                  title: "Scalability",
                  open_solution: "Yes with open source tools",
                  closed_solution: "Yes with additional cost"
                },
                {
                  title: "Features",
                  open_solution: "Limitless extensibility",
                  closed_solution: "Vendor supported feature set"
                },
                {
                  title: "Security",
                  open_solution: "Open for audit",
                  closed_solution: "Closed, based on trust"
                },
                {
                  title: "Support for using machine learning models",
                  open_solution: "Yes, state of the art tools available",
                  closed_solution: "Vendor supported feature set"
                },
                {
                  title: "Resources for developers",
                  open_solution:
                    "Active global community of thousands of developers and contributors, free online resources and documentation",
                  closed_solution: "Vendor specific programs"
                }
              ]
            }
          }
        }
      ]
    };
  }
};
</script>
