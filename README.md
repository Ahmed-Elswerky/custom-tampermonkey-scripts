# custom-script-for-dark-theme

# Description:

### this is a custom script repository, it's used with tampermonkey, and for the sole purpose of reducing the strain on the eye by making more websites in dark theme and bold fonts

# link to install TamperMonkey from

https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en

# Code to add

```// ==UserScript==
// @name         New Userscript
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://www.messenger.com/*
// @match        https://firebase.google.com/*
// @match        https://soundcloud.com/*
// @match        https://docs.flutter.dev/*
// @match        https://stackoverflow.com/*
// @match        https://pub.dev/*
// @match        https://dmitripavlutin.com/*
// @match        https://move.egybest.co/*
// @match        https://developer.android.com/*
// @match        https://drive.google.com/*
// @match        https://dillinger.io/*
// @match        localhost:3001/*
// @match        antqueuelive.web.app/*
// @match        https://translate.google.com/*
// @match        https://console.firebase.google.com/*
// @match        https://www.npmjs.com/*
// @match        https://console.cloud.google.com/*
// @match        https://cloud.google.com/*
// @match        https://play.google.com/*
// @match        https://realmefirmware.com/*
// @match        https://ant.design/*
// @match        https://react-bootstrap.github.io/*
// @match        https://www.itwonders-web.com/*
// @match        https://www.linkedin.com/*
// @match        https://www.diffchecker.com/*
// @icon         https://www.google.com/s2/favicons?domain=messenger.com
// @grant        none
// ==/UserScript==

(function() {
    setTimeout(function (){
        var style = document.createElement('style')
        let css=`*{font-weight:bold !important;}\
             html{filter:invert(1) hue-rotate(180deg) !important}\
             body{background:whitesmoke}\
             img,.bixrwtb6 ,svg,.image,.video-wrapper{filter:invert(1) hue-rotate(180deg) !important}`;
        style.type = 'text/css';
        if (style.styleSheet){
            // This is required for IE8 and below.
            style.styleSheet.cssText = css;
        } else {
            style.appendChild(document.createTextNode(css));
        }
        document.head.appendChild(style);
    },1)

    // Your code here...
})();