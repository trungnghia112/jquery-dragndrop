jQuery - drag 'n' drop - 1.4
============================

Le plugin a besoin de ces deux fichiers (en plus de _jquery.js_):
* [jquery-dragndrop.js](https://github.com/Mr21/jquery-dragndrop/blob/master/js/jquery-dragndrop.js)
* [jquery-dragndrop.css](https://github.com/Mr21/jquery-dragndrop/blob/master/css/jquery-dragndrop.css)

Demo
----

[mr21.fr/jquery-dragndrop/](http://mr21.fr/jquery-dragndrop/)

Exemple
-------

__HTML__

    <div id="dragndrop">
        <div class="jqdnd-drop">
            <b class="jqdnd-drag" style="background:#ddf"></b>
            <b class="jqdnd-drag" style="background:#aaf"></b>
        </div>
        <div class="jqdnd-drop">
            <b class="jqdnd-drag" style="background:#ddf"></b>
            <b class="jqdnd-drag" style="background:#aaf"></b>
        </div>
    </div>
    
__JS__

    $('#dragndrop').dragndrop({
        ondrag: function(drops, drags) {
            console.log('>>> ondrag');
            console.log(drops);
            console.log(drags);
        },
        ondrop: function(drops, drags) {
            console.log('<<< ondrop');
            console.log(drops);
            console.log(drags);
        }
    });

Historique des versions
-----------------------

* __1.4__ : Patch du bug des parents lors du `ondrop` quand les élèments sont lachés nulle-part.
* __1.3__ : `.off()` n'est plus utilisé lors du `DOMNodeInserted` sur les `jqdnd-drag`.
* __1.2__ : Patch d'un bug en rapport avec les `jqdnd-drop` et le mouseover recodé.
* __1.1__ : Patch d'un bug lié au `DOMNodeInserted`.
* __1.0__ : Première version fonctionnelle!
