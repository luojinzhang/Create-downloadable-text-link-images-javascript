# Create-downloadable-text-link-images-javascript
Create downloadable text using blob for images on javascript

    var images = document.getElementsByTagName('img'); 
    var aa='';
    for(var i = 0; i < images.length; i++) {
        if (images[i].src.indexOf("tv") > -1 || images[i].src.indexOf("tivi") > -1 || images[i].src.indexOf("ti-vi") > -1)
         aa += images[i].src + "\n";
        }
        (function () {
        var textFile = null,
        makeTextFile = function (text) {
        var data = new Blob([text], {type: 'text/plain'});
        if (textFile !== null) {
          window.URL.revokeObjectURL(textFile);
        }
        textFile = window.URL.createObjectURL(data);
        return textFile;
        };
        location = makeTextFile(aa);
    })();
