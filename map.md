---
title: Field Sites
---

Below are my primary research locations.

<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
/>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<div id="map" style="height: 500px; border-radius: 12px;"></div>

<script>
  var map = L.map('map').setView([0, -120], 2);

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; OpenStreetMap contributors'
  }).addTo(map);

  // Hawai‘i
  L.marker([21.30169, -157.81544]).addTo(map)
    .bindPopup("Hawai‘i – Long-term invasion biology & eDNA work");

  // Galápagos
  L.marker([-0.7432, -90.3047]).addTo(map)
    .bindPopup("Galápagos Islands – NSF IRES field program");

  // Scripps / California
  L.marker([32.867, -117.257]).addTo(map)
    .bindPopup("Scripps Institution of Oceanography – foundational work");

  // Marshall Islands
  L.marker([7.16435, 171.03892]).addTo(map)
    .bindPopup("Marshall Islands – eDNA sampling (Majuro)");
</script>
