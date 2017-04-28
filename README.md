# Tampermonkey_e-onkyo
    // ==UserScript==
    // @name           e-onkyo
    // @version        1.0
    // @description :Home Goto HelloWork; :HelloWork Goto Home;
    // @author         sequre
    // @match         http://www.e-onkyo.com/search/*
    // @grant          none
    // ==/UserScript==
    /* jshint -W097 */
    "use strict";

    // Your code here...
    var lists = document.querySelectorAll(".searchResultAlbumListEntry");
    var texts = document.querySelectorAll(".searchResultAlbumListEntry p");
    var images = document.querySelectorAll(".searchResultAlbumListEntry img");
    for(var i = 0, m = lists.length; i < m; i++)
    {
        lists[i].setAttribute("style", "float: initial; height: 64px;");
    }
    for(i = 0, m = texts.length; i < m; i++)
    {
        texts[i].setAttribute("style", "overflow: initial; font-size: 14px;");
    }
    for(i = 0, m = images.length; i < m; i++)
    {
        images[i].width = 64;
        images[i].height = 64;
        images[i].setAttribute("align", "left");
    }
