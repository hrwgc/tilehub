## tilehub - mbtiles hosted and served via GitHub

[![](https://img.skitch.com/20120713-deww5ab2fcwqm37y7sqpayt9si.png)](http://hrwgc.github.com/tilehub/)

This project was inspired by Bobby Sudekum's [TileMill without the Box](http://www.visuallybs.com/no-box/).

Making a few simple modifications to his code, I was able to create [tilehub](http://hrwgc.github.com/tilehub/), which serves map tiles rendered in [TileMill] via GitHub pages. Everything is contained in the repo itself.

### Steps

1. Check out Bobby Sudekum's [article](http://www.visuallybs.com/no-box/), which has good step-by-step instructions. Then render a map in TileMill and export the mbtiles.

2. Install [MBUtil][MBUtil].

3. Use MBUtil to decompose the mbtiles file

    mb-util yourmap.mbtiles yourdirectory

4. Modify the metadata.json file


<pre>
grid({
    "attribution": "", 
    "description": "", 
    "center": "-73.964,40.772,13", 
    "bounds": "-74.2538,40.5159,-73.5535,40.984", 
    "minzoom": "10", 
    "version": "1.0.0", 
    "maxzoom": "15", 
    "name": "contours",
    "scheme": "xyz",
    "tiles": ["\/tilehub\/mbtiles\/2010contours\/1.0.0\/contours\/{z}\/{x}\/{y}.png"],
    "grids": ["\/tilehub\/mbtiles\/2010contours\/1.0.0\/contours\/{z}\/{x}\/{y}.grid.json"]
})
</pre>
5. Link to leaflet, wax, and jquery.
