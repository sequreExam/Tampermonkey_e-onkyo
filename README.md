# Tampermonkey_e-onkyo
曲名が切れて意味わかんないので縦のリストにしたみたいです(記憶なし)

    // ==UserScript==
    // @name        e-onkyo
    // @version     1.0
    // @description :Home Goto HelloWork; :HelloWork Goto Home;
    // @author      sequre
    // @match       http://www.e-onkyo.com/search/*
    // @grant       none
    // ==/UserScript==
    "use strict";

    // Your code here...
    const lists = document.querySelectorAll(".searchResultAlbumListEntry");
    const texts = document.querySelectorAll(".searchResultAlbumListEntry p");
    const images = document.querySelectorAll(".searchResultAlbumListEntry img");
    let i, m;

    for(i = 0, m = lists.length; i < m; i++)
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
