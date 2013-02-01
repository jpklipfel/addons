ADDON originally created by @hsquividant.

PHP query on french soil databases.
Return edges and detail of soil cartographic unit selected by user.
Default options for this addon are specified in the manifest.json file:

    "default_options": {
        "group": "Pedologie",                                             // future option including addon in a group   
        "url": "http://websoltest.agrocampus-ouest.fr/webservice/getUCS", // Regional websol server
        "format": "geojson",                                              // spatial format. Do not change.
        "sld": false,                                                     // return no sld. Do not change
        "layers": "25035,25022,25029,25056"                               // departemental layers list. 
    }

If you want to query another soil database, you have to change "url" and "layers" options. In this case, be sure to include such options in your ADDON config object:
For example, to query Bourgogne soil database, here are the right options. I test it & it runs. 

    "options": {
        "group": "Pedologie",
        "url": "http://websol.educagri.fr/webservice/getUCS",
        "format": "geojson",
        "sld": false,
        "layers": "25021,25058,25071,25089"
    }

