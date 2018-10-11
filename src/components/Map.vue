<template>
  <div id="map"></div>
</template>

<script>
import Map from "ol/Map";
import View from "ol/View";

import TileLayer from "ol/layer/Tile";
import LayerVector from "ol/layer/Vector";
import SourceVector from "ol/source/Vector";
import GeoJSON from "ol/format/GeoJSON";
import Feature from "ol/Feature";

import Image from "ol/layer/Image";
import ImageWMS from "ol/source/ImageWMS";
import TileImage from "ol/source/TileImage";
import OSM from "ol/source/OSM.js";

export default {
  name: "Map",
  props: {
    msg: String
  },
  mounted() {
    new Map({
      layers: [
        new TileLayer({
          title: "Google Yol",
          // image: "/assets/img/streets.jpg",
          source: new TileImage({
            url: "http://mt1.google.com/vt/lyrs=m@113&hl=tr&&x={x}&y={y}&z={z}"
          }),
          visible: true
        })
      ],
      target: "map",
      view: new View({
        center: [4000000, 4000000],
        zoom: 4
      })
    });
  }
};
</script>

<style scoped>
</style>
