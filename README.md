<html>
<head>
	<title>belajar wegis</title>
<!-- LEAFLET CSS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<style>
    #map{
        width: 100%;
        height: 100vh;
    }
    </style>
<head> 
<body>
     <div id="map"></div>
     <body>
<html>
    <!-- LEAFLET JAVASCRIPT -->
    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js" integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>
    <script>
    <!-- LOKASI KAJIAN -->
    var map = L.map('map').setView([-5.367016, 105.317890], 15);
    <!-- BASEMAP OPENSTREETMAP -->
    var osm = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
     });
     osm.addTo(map);
     <!-- BASEMAP ESRI -->
var Esri_WorldImagery = L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}', {
    attribution: 'Tiles &copy; Esri &mdash; Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community'
    });
Esri_WorldImagery.addTo(map);
<!-- BUNDARAN YANG SERING SAYA LANGGAR ATURAN SAAT BERLALU LINTAS DI ITERA -->
var bundaran = L.circle([ -5.363156, 105.312634], {
    color: 'red',
    fillColor: '#f03',
    fillOpacity: 0.5,
    radius: 20
}).addTo(map);
<!-- BUNDARAN INI JUGA SERING SAYA LANGGAR SETELAH SELESAI KULIAH DI GKU 2 -->
var bundaran = L.circle([-5.360813, 105.314847], {
    color: 'green',
    fillColor: '#00ff00',
    fillOpacity: 0.5,
    radius: 35
}).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG E -->
var polygon = L.polygon([
    [-5.359799, 105.315831],
    [-5.359957, 105.315831],
    [-5.359957, 105.315571],
    [-5.360474, 105.315571],
    [-5.360474, 105.315401],
    [-5.359635, 105.315401],
    [-5.359635, 105.315571],
    [-5.359799, 105.315571]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG E -->
var polygon = L.polygon([
    [-5.361290, 105.314062],
    [-5.361446, 105.314058],
    [-5.361446, 105.313971],
    [-5.361504, 105.313974],
    [-5.361506, 105.314043],
    [-5.361714, 105.314041],
    [-5.361710, 105.313879],
    [-5.361509, 105.313880],
    [-5.361513, 105.313929],
    [-5.361442, 105.313925],
    [-5.361450, 105.313325],
    [-5.361295, 105.313323],
    [-5.361296, 105.313619],
    [-5.361172, 105.313620],
    [-5.361172, 105.313785],
    [-5.361283, 105.313782]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG LABTEK 5 OZT -->
var polygon = L.polygon([
    [-5.361970, 105.311004],
    [-5.362141, 105.310998],
    [-5.362158, 105.309950],
    [-5.361994, 105.309953]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG LABTEK 2 -->
var polygon = L.polygon([
    [-5.361425, 105.310973],
    [-5.361602, 105.310973],
    [-5.361606, 105.310019],
    [-5.361426, 105.310019]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG KULIAH UMUM 1 -->
var polygon = L.polygon([
    [-5.360814, 105.311005],
    [-5.361026, 105.311007],
    [-5.361018, 105.309989],
    [-5.360805, 105.309991]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG LABTEK 1 -->
var polygon = L.polygon([
    [-5.360211, 105.309995],
    [-5.360415, 105.309998],
    [-5.360425, 105.310506],
    [-5.360207, 105.310510]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG C-->
var polygon = L.polygon([
    [-5.358333, 105.313335],
    [-5.358468, 105.313335],
    [-5.358466, 105.314001],
    [-5.358313, 105.314149]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG D-->
var polygon = L.polygon([
    [-5.358540, 105.313457],
    [-5.359049, 105.313453],
    [-5.358907, 105.313597],
    [-5.358542, 105.313597]
]).addTo(map);
<!-- POLIGON BANGUNAN  GEDUNG LABORATORIUM TEKNIK 3-->
var polygon = L.polygon([
    [-5.360180, 105.309461],
    [-5.360417, 105.309462],
    [-5.360417, 105.308819],
    [-5.360178, 105.308814]
]).addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GK2 -->
    var GKU2 = L.marker([-5.360245, 105.314034]);
    var namagk2 = GKU2.bindPopup("Gedung Kuliah Umum 2").openPopup()
    namagk2.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GK1 -->
    var GKU1 = L.marker([-5.360887, 105.310620]);
    var namagku1 = GKU1.bindPopup("Gedung Kuliah Umum 1").openPopup()
    namagku1.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG F -->
    var GDF = L.marker([-5.361369, 105.313710]);
    var namagdf = GDF.bindPopup("Gedung Kuliah Umum 1").openPopup()
    namagdf.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG LABTEK 5 OZT -->
    var LAB5 = L.marker([-5.362034, 105.310442]);
    var namalab5 = LAB5.bindPopup("Gedung Laboratorium Teknik 5 & OZT").openPopup()
    namalab5.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG LABTEK 2 -->
    var LAB2 = L.marker([-5.361492, 105.310442]);
    var namalab2 = LAB2.bindPopup("Gedung Kuliah Umum 2").openPopup()
    namalab2.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG LABTEK 1 -->
    var LAB1 = L.marker([-5.360346, 105.310226]);
    var namalab1 = LAB1.bindPopup("Gedung Laboratorium Teknik 1").openPopup()
    namalab1.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG C -->
    var GDC = L.marker([-5.358380, 105.313586]);
    var namagedc = GDC.bindPopup("Gedung C").openPopup()
    namagedc.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG D -->
    var GDD = L.marker([-5.358757, 105.313521]);
    var namagedd = GDD.bindPopup("Gedung D").openPopup()
    namagedd.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG LABTEK 3 -->
    var LAB3 = L.marker([-5.360290, 105.309154]);
    var namalab3 = LAB3.bindPopup("Gedung Laboratorium Teknik 3").openPopup()
    namalab3.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG E -->
    var GDE = L.marker([-5.360054, 105.315533]);
    var namagede = GDE.bindPopup("Gedung E").openPopup()
    namagede.addTo(map);
    var baseMaps = {
	"OSM":osm,
	"ESRI":Esri_WorldImagery,
};
var overlayMaps = {
	"GKU 1": GKU1,
    "GKU 2" : GKU2,
    "Gedung D": GDD,
    "Gedung C": GDC,
    "Gedung E": GDE,
    "Gedung F": GDF,
    "Labtek 1": LAB1,
    "Labtek 2": LAB2,
    "Labtek 3": LAB3,   
    "Labtek 5": LAB5,
};

map.removeLayer(LAB5)
map.removeLayer(GKU1)
map.removeLayer(GKU2)
map.removeLayer(GDE)
map.removeLayer(LAB3)
map.removeLayer(GDC)
map.removeLayer(GDF)
map.removeLayer(LAB2)
map.removeLayer(LAB1)

L.control.layers(baseMaps,overlayMaps, {collapsed : false}).addTo(map);
</script>
 </script>
