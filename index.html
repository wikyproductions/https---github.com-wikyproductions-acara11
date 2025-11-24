<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- leaflet css link  -->
    <link rel="stylesheet"
        href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />

    <title>Web-GIS with Geoserver and Leaflet</title>

    <style>
        body {
            margin: 0;
            padding: 0;
        }

        #map {
            width: 100%;
            height: 100vh;
        }

        .legend {
            padding: 6px 8px;
            font: 14px/16px Arial, Helvetica, sans-serif;
            background: white;
            background: rgba(255,255,255,0.8);
            box-shadow: 0 0 15px rgba(0,0,0,0.2);
            border-radius: 5px;
            line-height: 18px;
            color: #555;
        }

        .legend i {
            width: 18px;
            height: 18px;
            float: left;
            margin-right: 8px;
            opacity: 0.7;
        }
    </style>
</head>

<body>
    <div id="map"></div>

    <!-- leaflet js link  -->
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>

    <script>
        // ===============================
        // MAP DASAR
        // ===============================
        var map = L.map("map").setView([-7.732521, 110.402376], 11);

        var osm = L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
            maxZoom: 19,
            attribution: "© OpenStreetMap contributors",
        }).addTo(map);

        // ===============================
        // LAYER WMS DARI GEOSERVER
        // ===============================

        // 1. Admin Kecamatan
        var kecamatan = L.tileLayer.wms(
            "http://localhost:8080/geoserver/pgw/wms", {
                layers: "pgw:admin_sleman",
                format: "image/png",
                transparent: true
            }
        ).addTo(map);

        var jalan = L.tileLayer.wms(
            "http://localhost:8080/geoserver/pgw/wms", {
                layers: "pgw:jalan_sleman",
                format: "image/png",
                transparent: true
            }
        ).addTo(map);

        var rs = L.tileLayer.wms(
            "http://localhost:8080/geoserver/pgw/wms", {
                layers: "pgw:rs_sleman",
                format: "image/png",
                transparent: true
            }
        ).addTo(map);

        var overlayLayers = {
            "Administrasi Kecamatan": kecamatan,
            "Jalan Kabupaten Sleman": jalan,
            "RS Kecamatan": rs
        };

        var pengangguran = L.tileLayer.wms("https://geoportal.slemankab.go.id/geoserver/wms", {
            layers: "geonode:pengangguran_sleman_2024",
            format: "image/png",
            transparent: true,
        }).addTo(map);

        overlayLayers["Tingkat Pengangguran"] = pengangguran;

        L.control.layers(null, overlayLayers).addTo(map);

        // LEGENDA
        function getColor(d) {
            return d > 2.5 ? '#800026' :
                   d > 2.0 ? '#BD0026' :
                   d > 1.5 ? '#E31A1C' :
                   d > 1.0 ? '#FC4E2A' :
                   d > 0.5 ? '#FD8D3C' :
                             '#FEB24C';
        }

        var legend = L.control({position: 'bottomright'});

        legend.onAdd = function (map) {

            var div = L.DomUtil.create('div', 'info legend'),
                grades = [0, 0.5, 1.0, 1.5, 2.0, 2.5],
                labels = ['<strong>Tingkat Pengangguran (%)</strong><br>'];

            for (var i = 0; i < grades.length; i++) {
                var from = grades[i];
                var to = grades[i + 1];

                labels.push(
                    '<i style="background:' + getColor(from + 0.1) + '"></i> ' +
                    from + (to ? '&ndash;' + to : '+'));
            }

            div.innerHTML = labels.join('<br>');
            return div;
        };
        legend.addTo(map);
    </script>
     
</body>

</html>