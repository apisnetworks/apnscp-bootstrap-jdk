apnscp JavaScript Kit

apnscp Bootstrap JDK is a kit to build apnscp's JavaScript libraries. The JDK relies on Bootstrap 4, which is mated to this repository (and panel). As of now, the current version is 4.0.0-alpha.6.

Node LTS (6.10) is recommended.

Getting Started

    git clone https://github.com/apisnetworks/apnscp-bootstrap-jdk.git
    cd apnscp-bootstrap-jdk
    npm install

Specifying Output

Use the environment variable THEME to force an output file (default: apnscp.css), APNSCP_PATH is the assumed location of apnscp, if making changes to a live panel; and THEME_PATH is the location for CSS themes in apnscp, usually public/css/themes/.

    env THEME=mytheme grunt dist

Compiled CSS will be spit out to dist/css/mytheme.css.



Building On-the-fly

JDK makes use of grunt-contrib-watch to rebuild whenever a watched file is changed. Simply run grunt watch from the command-line.



Enabling in apnscp

apnscp must be configured with [style] => override_js set to true on config.ini. Once enabled, apnscp will use /public/js/apnscp-custom.js instead of /public/js/apnscp.js. This will also futureproof apnscp updates that will overwrite apnscp.js.
