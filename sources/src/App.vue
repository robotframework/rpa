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
              header: "",
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
        },
        {
          title: "Examples",
          text_block: true,
          tab_box: false,
          feature_box: false,
          data: {
            text: {
              header: "Examples",
              text:
                "<p>Robot Framework RPA has just been developed (for RPA?) so there are no real life cases just yet. However, soon there will be and then this page will be updated.</p>\
                <p>Robot Framework RPA can be used wherever RPA is used. RPA aims to replace manual, repetitive and boring human tasks. A good example of RPA in use is a process that has repeatable and predictable interactions with IT applications. For example, RPA is widely used in Finance and Insurance industries where there’s still a lot of repetitive processes like handling loan or insurance applications.</p>"
            }
          }
        },
        {
          title: "Getting started",
          text_block: true,
          tab_box: false,
          feature_box: false,
          data: {
            text: {
              header: "Getting started",
              text: ""
            }
          }
        },
        {
          title: "FAQ",
          text_block: true,
          tab_box: false,
          feature_box: false,
          data: {
            text: {
              header: "FAQ",
              text:
                '<div class="faq"><p><b>Q</b>: What is the price for Robot Framework RPA Tool?</p>\
                <p>Robot Framework RPA tool is an open source tool and it is free to use without license costs.</p>\
                <p><b>Q</b>: license?</p> \
                <p>Apache License 2.0</p>\
                <p><b>Q</b>: What do I need to get started?</p>\
                <p></p>\
                <p><b>Q</b>: What does it take for one to learn to develop robots with Robot Framework?</p>\
                <p>A good start is if you’ve used Robot Framework before. If you haven’t, no problem. Basic Python skills are enough? There are also foundation courses available for those who are beginning their journey with Robot Framework.</p>\
                <p><b>Q</b>: How does it differentiate with Robot Framework for test automation?</p>\
                <p>Robot Framework is the core and you can do test automation and/or RPA with it. The main difference between these two is that in test automation you automate test cases and in RPA you automate processes. \
                <p><b>Q</b>: Does this RPA tool scale up and down?</p>\
                <p>Yes and yes. In Robot Framework RPA you can add any number of robots whilst in other tools you pay for adding additional robots. </p>\
                <p><b>Q</b>: How are security issues handled?</p>\
                <p></p>\
                <p><b>Q</b>: Where is Robot Framework RPA used?</p>\
                <p>Anywhere where processes can be automated. </p>\
                <p><b>Q</b>: Is there future development provided for this tool?</p>\
                <p>Yes, Robot Framework Foundation is enabling future development for this tool.</p></div>'
            }
          }
        },
        {
          title: "Libraries",
          text_block: true,
          tab_box: true,
          feature_box: false,
          data: {
            text: {
              header: "Libraries",
              text: "",
              notext:
                '<p> Test libraries provide the actual testing capabilities to Robot Framework by providing keywords. There are several standard libraries that are bundled in with the framework, and galore of separately developed external libraries that can be installed based on your needs. Creating your own test libraries <a href="http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#creating-test-libraries" target="_blank">is a breeze</a>. </p> <p> <a href="https://github.com/robotframework/robotframework.github.com" target="_blank">Let us know</a> if there are useful libraries missing from the list. </p>'
            },
            tabs: [
              {
                title: "Standard",
                items: [
                  {
                    title: "Builtin",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Provides a set of often needed generic keywords. Always automatically available without imports."
                  },
                  {
                    title: "Dialogs",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Provides means for pausing the test execution and getting input from users."
                  },
                  {
                    title: "Collections",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Provides a set of keywords for handling Python lists and dictionaries."
                  },
                  {
                    title: "OperatingSystem",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Enables various operating system related tasks to be performed in the system where Robot Framework is running."
                  },
                  {
                    title: "Remote",
                    href: "https://github.com/robotframework/RemoteInterface",
                    text:
                      "Special library acting as a proxy between Robot Framework and test libraries elsewhere. Actual test libraries can be running on different machines and be implemented using any programming language supporting XML-RPC protocol."
                  },
                  {
                    title: "Screenshot",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Provides keywords to capture screenshots of the desktop."
                  },
                  {
                    title: "String",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Library for generating, modifying and verifying strings."
                  },
                  {
                    title: "Telnet",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Makes it possible to connect to Telnet servers and execute commands on the opened connections."
                  },
                  {
                    title: "XML",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Library for generating, modifying and verifying XML files."
                  },
                  {
                    title: "Process",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Library for running processes in the system. New in Robot Framework 2.8."
                  },
                  {
                    title: "DateTime",
                    href:
                      "http://robotframework.org/robotframework/#standard-libraries",
                    text:
                      "Library for date and time conversions. New in Robot Framework 2.8.5."
                  }
                ]
              },
              {
                title: "External",
                items: [
                  {
                    title: "Android library",
                    href:
                      "https://github.com/lovelysystems/robotframework-androidlibrary#readme",
                    text:
                      "Library for all your Android automation needs. It uses Calabash Android internally."
                  },
                  {
                    title: "AnywhereLibrary",
                    href:
                      "https://github.com/luisxiaomai/robotframework-anywherelibrary",
                    text:
                      "Library for testing Single-Page Apps (SPA). Uses Selenium Webdriver and Appium internally."
                  },
                  {
                    title: "AppiumLibrary",
                    href:
                      "https://github.com/jollychang/robotframework-appiumlibrary",
                    text:
                      "Library for Android- and iOS-testing. It uses Appium internally."
                  },
                  {
                    title: "Archive library",
                    href:
                      "https://github.com/bulkan/robotframework-archivelibrary",
                    text: "Library for handling zip- and tar-archives."
                  },
                  {
                    title: "AutoItLibrary",
                    href:
                      "https://github.com/bulkan/robotframework-archivelibrary",
                    text:
                      "Windows GUI testing library that uses AutoIt freeware tool as a driver."
                  },
                  {
                    title: "CncLibrary",
                    href:
                      "https://github.com/eficode/robotframework-cnclibrary",
                    text: "Library for driving a CNC milling machine."
                  },
                  {
                    title: "Database Library (Java)",
                    href: "https://github.com/Hi-Fi/robotframework-dblibrary",
                    text:
                      'Java-based library for database testing. Usable with Jython. Available also at <a href="http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22robotframework-dblibrary%22" target="_blank">Maven central</a>.'
                  },
                  {
                    title: "Database Library (Python)",
                    href:
                      "http://franz-see.github.com/Robotframework-Database-Library/",
                    text:
                      "Python based library for database testing. Works with any Python interpreter, including Jython."
                  },
                  {
                    title: "Diff Library",
                    href:
                      "https://github.com/bulkan/robotframework-difflibrary",
                    text: "Library to diff two files together."
                  },
                  {
                    title: "Django Library",
                    href:
                      "https://pypi.python.org/pypi/robotframework-djangolibrary",
                    text:
                      'Library for <a href="https://www.djangoproject.com/" target="_blank">Django</a>, a Python web framework.'
                  },
                  {
                    title: "Eclipse Library",
                    href:
                      "https://github.com/lcarbonn/robotframework-eclipselibrary/",
                    text:
                      "Library for testing Eclipse RCP applications using SWT widgets."
                  },
                  {
                    title: "robotframework-faker",
                    href: "https://pypi.python.org/pypi/robotframework-faker/",
                    text:
                      'Library for <a href="https://github.com/joke2k/faker" target="_blank">Faker</a>, a fake test data generator.'
                  },
                  {
                    title: "FTP library",
                    href:
                      "https://github.com/kowalpy/Robot-Framework-FTP-Library",
                    text:
                      "Library for testing and using FTP server with Robot Framework."
                  },
                  {
                    title: "HTTP library (livetest)",
                    href:
                      "https://github.com/peritus/robotframework-httplibrary/#readme",
                    text:
                      "Library for HTTP level testing using livetest tool internally."
                  },
                  {
                    title: "HTTP library (Requests)",
                    href:
                      "https://github.com/bulkan/robotframework-requests/#readme",
                    text:
                      "Library for HTTP level testing using Request internally."
                  },
                  {
                    title: "HttpRequestLibrary (Java)",
                    href:
                      "https://github.com/Hi-Fi/robotframework-httprequestlibrary#readme",
                    text:
                      'Library for HTTP level testing using Apache HTTP client. Available also at <a href="http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22robotframework-httprequestlibrary%22" target="_blank">Maven central</a>.'
                  },
                  {
                    title: "iOS library",
                    href:
                      "https://github.com/lovelysystems/robotframework-ioslibrary#readme",
                    text:
                      "Library for all your iOS automation needs. It uses Calabash iOS Server internally."
                  },
                  {
                    title: "ImageHorizonLibrary",
                    href:
                      "https://github.com/eficode/robotframework-imagehorizonlibrary#readme",
                    text:
                      "Cross-platform, pure Python library for GUI automation based on image recognition."
                  },
                  {
                    title: "JavaFXLibrary",
                    href: "https://github.com/eficode/JavaFXLibrary#readme",
                    text:
                      'Library for testing JavaFX applications, based on <a href="https://github.com/TestFX/TestFX" target="_blank">TestFX</a>. Has also remote interface support.'
                  },
                  {
                    title: "MongoDB library",
                    href:
                      "https://github.com/iPlantCollaborativeOpenSource/Robotframework-MongoDB-Library#readme",
                    text: "Library for interacting with MongoDB using pymongo."
                  },
                  {
                    title: "MQTT library",
                    href:
                      "https://github.com/randomsync/robotframework-mqttlibrary#readme",
                    text: "Library for testing MQTT brokers and applications."
                  },
                  {
                    title: "NcclientLibrary",
                    href: "https://github.com/vkosuri/robotframework-ncclient",
                    text: "https://github.com/ncclient/ncclient"
                  },
                  {
                    title: "Rammbock",
                    href: "https://github.com/robotframework/Rammbock#readme",
                    text:
                      "Generic network protocol test library that offers easy way to specify network packets and inspect the results of sent and received packets."
                  },
                  {
                    title: "RemoteSwingLibrary",
                    href:
                      "https://github.com/robotframework/remoteswinglibrary",
                    text:
                      "Library for testing and connecting to a java process and using SwingLibrary, especially Java Web Start applications."
                  },
                  {
                    title: "RESTinstance",
                    href: "https://github.com/asyrjasalo/RESTinstance/",
                    text: "Robot Framework test library for HTTP JSON APIs."
                  },
                  {
                    title: "SeleniumLibrary",
                    href: "http://github.com/robotframework/SeleniumLibrary/",
                    text:
                      "Web testing library that uses popular Selenium tool internally."
                  },
                  {
                    title: "Selenium2Library",
                    href: "https://github.com/robotframework/Selenium2Library",
                    text:
                      "Web testing library that uses Selenium 2. Library is deprecated; users should upgrade to SeleniumLibrary described above."
                  },
                  {
                    title: "Selenium2Library for Java",
                    href:
                      "https://github.com/MarkusBernhardt/robotframework-selenium2library-java#readme",
                    text: "Java port of the Selenium2Library."
                  },
                  {
                    title: "ExtendedSelenium2Library",
                    href:
                      "https://github.com/rickypc/robotframework-extendedselenium2library",
                    text:
                      "Web testing library that uses Selenium2Library internally, providing AngularJS support on top of it."
                  },
                  {
                    title: "SikuliLibrary",
                    href:
                      "https://github.com/rainmanwy/robotframework-SikuliLibrary#readme",
                    text:
                      'Sikuli Robot Framework Library provide keywords to test UI through <a href="http://sikulix.com/" target="_blank">Sikulix</a>. This library supports Python 2.x and 3.x.'
                  },
                  {
                    title: "SSHLibrary",
                    href: "https://github.com/robotframework/SSHLibrary",
                    text:
                      "Enables executing commands on remote machines over an SSH connection. Also supports transfering files using SFTP."
                  },
                  {
                    title: "SudsLibrary",
                    href:
                      "https://github.com/ombre42/robotframework-sudslibrary#readme",
                    text:
                      "A library for functional testing of SOAP-based web services based on Suds, a dynamic SOAP 1.1 client."
                  },
                  {
                    title: "SwingLibrary",
                    href: "https://github.com/robotframework/SwingLibrary/wiki",
                    text:
                      "Library for testing Java applications with Swing GUI."
                  },
                  {
                    title: "TestFX Library",
                    href:
                      "https://github.com/Altran-PT-GDC/Robot-Framework-Test-FX-Library",
                    text:
                      'Library to enable to test Java FX applications using the <a href="https://github.com/TestFX/TestFX" target="_blank">TestFX framework</a>.'
                  },
                  {
                    title: "TFTPLibrary",
                    href:
                      "https://github.com/kowalpy/Robot-Framework-TFTP-Library",
                    text:
                      'Library for interacting over <a href="https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol" target="_blank">Trivial File Transfer Portocol</a>.'
                  },
                  {
                    title: "watir-robot",
                    href: "https://github.com/semperos/watir-robot/#readme",
                    text: "Web testing library that uses Watir tool."
                  }
                ]
              },
              {
                title: "Other",
                items: [
                  {
                    title: "Creating test libraries",
                    href:
                      "http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#creating-test-libraries",
                    text:
                      "Creating test libraries section in Robot Framework User Guide."
                  },
                  {
                    title: "plone.app.robotframework",
                    href:
                      "https://pypi.python.org/pypi/plone.app.robotframework",
                    text:
                      "Provides resources and tools for writing functional Selenium tests for Plone CMS and its add-ons."
                  },
                  {
                    title: "JavalibCore",
                    href: "https://github.com/robotframework/JavalibCore/wiki",
                    text:
                      "Base for implementing larger Java based test libraries for Robot Framework."
                  },
                  {
                    title: "Remote",
                    href: "https://github.com/robotframework/RemoteInterface",
                    text:
                      "Built-in special library acting as a proxy between Robot Framework and test libraries elsewhere. Actual test libraries can be running on different machines and be implemented using any programming language supporting XML-RPC protocol."
                  },
                  {
                    title: "RemoteApplications",
                    href:
                      "https://github.com/robotframework/RemoteApplications",
                    text:
                      "Special test library for launching Java applications on a separate JVM and taking other libraries into use on them."
                  }
                ]
              }
            ]
          }
        },
        {
          title: "Tools",
          text_block: true,
          tab_box: true,
          feature_box: false,
          data: {
            text: {
              header: "Tools",
              text: "",
              notext:
                '<p> Supporting tools ease everything surrounding tests: editing, running, building and so on. Most of these tools are developed as separate projects, but some are built into the framework itself. </p> <p> <a href="https://github.com/robotframework/robotframework.github.com" target="_blank">Let us know</a> if there are useful tools missing from the list. </p>'
            },
            tabs: [
              {
                title: "BUILT-IN",
                items: [
                  {
                    title: "Rebot",
                    href:
                      "http://robotframework.org/robotframework/#built-in-tools",
                    text:
                      "Tool for generating logs and reports based on XML outputs and for combining multiple outputs together."
                  },
                  {
                    title: "Libdoc",
                    href:
                      "http://robotframework.org/robotframework/#built-in-tools",
                    text:
                      "Tool for generating keyword documentation for test libraries and resource files."
                  },
                  {
                    title: "Testdoc",
                    href:
                      "http://robotframework.org/robotframework/#built-in-tools",
                    text:
                      "Generates high level HTML documentation based on Robot Framework test cases."
                  },
                  {
                    title: "Tidy",
                    href:
                      "http://robotframework.org/robotframework/#built-in-tools",
                    text:
                      "Tool for cleaning up and changing format of Robot Framework test data files."
                  }
                ]
              },
              {
                title: "EDITORS",
                items: [
                  {
                    title: "RIDE",
                    text: "Standalone Robot Framework test data editor.",
                    href: "https://github.com/robotframework/RIDE/wiki"
                  },
                  {
                    title: "Atom plugin",
                    text: "Robot Framework plugin for Atom.",
                    href: "https://atom.io/packages/language-robot-framework"
                  },
                  {
                    title: "Brackets plugin",
                    text: "Robot Framework plugin for Brackets.",
                    href:
                      "https://github.com/boakley/brackets-robotframework/wiki"
                  },
                  {
                    title: "Eclipse plugin",
                    text: "Robot Framework plugin for Eclipse IDE.",
                    href:
                      "https://github.com/NitorCreations/RobotFramework-EclipseIDE/wiki"
                  },
                  {
                    title: "Emacs major mode",
                    text: "Emacs major mode for editing tests.",
                    href: "https://github.com/sakari/robot-mode"
                  },
                  {
                    title: "Gedit",
                    text: "Syntax highlighting for Gedit.",
                    href: "https://github.com/vkosuri/gedit-robot"
                  },
                  {
                    title: "Robot Plugin for IntelliJ IDEA",
                    text: "For IntelliJ IDEA-based editors by JIVE Software.",
                    href: "http://plugins.jetbrains.com/plugin/7430"
                  },
                  {
                    title: "Robot Support for IntelliJ IDEA",
                    text:
                      "For IntelliJ IDEA-based editors by Valerio Angelini.",
                    href: "http://plugins.jetbrains.com/plugin/7415"
                  },
                  {
                    title: "TextMate bundle",
                    text: "Bundle for TextMate adding syntax highlighting.",
                    href: "https://bitbucket.org/jussimalinen/robot.tmbundle/"
                  },
                  {
                    title: "Sublime assistant",
                    text:
                      "A plugin for Sublime Text 2 &amp; 3 by Andriy Hrytskiv.",
                    href:
                      "https://github.com/andriyko/sublime-robot-framework-assistant"
                  },
                  {
                    title: "Sublime plugin",
                    text: "A plugin for Sublime Text 2 by Mike Gershunovsky.",
                    href: "https://github.com/shellderp/sublime-robot-plugin"
                  },
                  {
                    title: "Vim plugin",
                    text: "Vim plugin for development with Robot Framework.",
                    href: "https://github.com/mfukar/robotframework-vim"
                  },
                  {
                    title: "Notepad++",
                    text: "Syntax highlighting for Notepad++.",
                    href: "https://github.com/vkosuri/lang-robot"
                  },
                  {
                    title: "RED",
                    text: "Eclipse based editor with a debugger by Nokia.",
                    href: "https://github.com/nokia/RED"
                  }
                ]
              },
              {
                title: "BUILD TOOLS",
                items: [
                  {
                    title: "Jenkins plugin",
                    href:
                      "https://wiki.jenkins-ci.org/display/JENKINS/Robot+Framework+Plugin",
                    text:
                      "Plugin to collect and publish Robot Framework test results in Jenkins."
                  },
                  {
                    title: "Maven plugin",
                    href: "http://robotframework.github.com/MavenPlugin/",
                    text: "Maven plugin for using Robot Framework."
                  },
                  {
                    title: "Ant task",
                    href: "http://code.google.com/p/robotframework-ant/",
                    text: "Ant task for running Robot Framework tests."
                  }
                ]
              },
              {
                title: "OTHER",
                items: [
                  {
                    title: "Fixml",
                    href: "https://bitbucket.org/robotframework/fixml",
                    text:
                      "Tool for fixing Robot Framework output files that are broken."
                  },
                  {
                    title: "Pabot",
                    href: "https://github.com/mkorpela/pabot",
                    text: "A parallel executor for Robot Framework test cases."
                  },
                  {
                    title: "Mabot",
                    href: "http://github.com/robotframework/mabot/",
                    text:
                      "Tool for reporting manual tests in format compatible with Robot Framework outputs."
                  },
                  {
                    title: "RFDoc",
                    href: "http://github.com/robotframework/rfdoc",
                    text:
                      "Web based system for storing and searching Robot Framework test library and resource file documentations."
                  },
                  {
                    title: "Robot Framework Hub",
                    href: "https://github.com/boakley/robotframework-hub/wiki",
                    text:
                      "Lightweight web server that provides access to the Robot Framework test assets via browser."
                  },
                  {
                    title: "Robot Tools",
                    href: "https://bitbucket.org/robotframework/robottools",
                    text:
                      "Collection of supporting tools that can be used with Robot Framework."
                  },
                  {
                    title: "SAGE Framework",
                    href: "https://www.nrl.navy.mil/itd/imda/products/sage",
                    text:
                      "Multi-agent based extension to Robot Framework. Agent based systems make it possible to test distributed systems such as Service Oriented Architecture systems. SAGE Provides a library of Robot Framework keywords for creating and managing SAGE agent networks as well as collecting and reporting results from remote agents."
                  },
                  {
                    title: "Robot Corder",
                    href: "https://github.com/sohwendy/Robotcorder",
                    text:
                      "Robot Corder generates Robot Framework test script by recording user interactions and scanning the html page in your Chrome browser. It aims to be equivalent of Selenium IDE for RobotFramework browser test automation."
                  },
                  {
                    title: "Robot Framework Lexer",
                    href: "https://bitbucket.org/robotframework/pygmentslexer",
                    text:
                      "Robot Framework syntax highlighting with Pygments. Link is to the lexer project itself, but the lexer is part of Pygments from version 1.6 onwards."
                  },
                  {
                    title: "DbBot",
                    href: "https://github.com/robotframework/DbBot",
                    text:
                      "Tool for serializing Robot Framework test results, i.e. output.xml files, into a SQLite database. It serves a good starting point to create your own reporting and analyzing tools."
                  },
                  {
                    title: "StatusChecker",
                    href: "https://github.com/robotframework/statuschecker/",
                    text:
                      "A tool for validation that executed Robot Framework test cases have expected statuses and log messages. Mainly targeted for test library developers."
                  }
                ]
              }
            ]
          }
        }
      ]
    };
  }
};
</script>
