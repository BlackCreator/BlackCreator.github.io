---
layout: post
title: About
permalink: /about/
img: about.png
---

Greetings. My real name is Stanislav. I work in Applied Mathematics and Computer Science. My research fields include numerical analysis and scientific computing. I use various tools, methods, programming languages (mainly, C/C++) in my projects. If you have any questions or offers/deals, please feel free to send me a message to exsidia@gmail.com. Also, here’s my [Curriculum Vitae]({{site.baseurl}}/docs/cv-us.pdf){:target="_blank"}. Here below are some of my photos.

<div align="center"><ul id="instafeed"></ul></div>
<script>
var token = '6256378210.a6f3670.172ce1dede224ad7b26c9b837fd1d519',
    num_photos = 5,
    container = document.getElementById( 'instafeed' ),
    scrElement = document.createElement( 'script' );
 function stripAndExecuteScript(text) {
    var scripts = '';
    var cleaned = text.replace(/<script[^>]*>([\s\S]*?)<\/script>/gi, function(){
        scripts += arguments[1] + '\n';
        return '';
    });

    if (window.execScript){
        window.execScript(scripts);
    } else {
        var head = document.getElementsByTagName('head')[0];
        var scriptElement = document.createElement('script');
        scriptElement.setAttribute('type', 'text/javascript');
        scriptElement.innerText = scripts;
        head.appendChild(scriptElement);
        head.removeChild(scriptElement);
    }
    return cleaned;
};


var scriptString = '<scrip' + 't + async="" defer="" src="//platform.instagram.com/en_US/embeds.js"></scr' + 'ipt>';

window.result = function( data ) 
{
for(x in data.data)
{
container.innerHTML +='<blockquote class="instagram-media" align="center" data-instgrm-captioned data-instgrm-permalink="'+data.data[x].link+'" data-instgrm-version="8" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"><div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:1.0% 0; text-align:center; width:100%;"> <a target="_blank" href="'+data.data[x].link+'"><img src="' + data.data[x].images.standard_resolution.url + '"></a></div> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A post shared by <a href="https://www.instagram.com/k3rnel_/" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px;" target="_blank"> Rango</a> (@k3rnel_)</p></div></blockquote>';
}
}




 
scrElement.setAttribute( 'src', 'https://api.instagram.com/v1/users/self/media/recent?access_token=' + token + '&count=' + num_photos + '&callback=result' );
document.body.appendChild( scrElement );

</script>




