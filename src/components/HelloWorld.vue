<template>
  <div id="dummy"></div>
</template>

<script>
window.THREE = require('three');

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    const scene = new window.THREE.Scene();
    const camera = new window.THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

    const renderer = new window.THREE.WebGLRenderer();
    renderer.setSize( window.innerWidth, window.innerHeight );
    document.body.appendChild( renderer.domElement );

    const geometry = new window.THREE.BoxGeometry();
    const material = new window.THREE.MeshBasicMaterial( { color: 0x00ff00 } );
    const cube = new window.THREE.Mesh( geometry, material );
    scene.add( cube );
    camera.position.z = 5;
    renderer.render( scene, camer

  }
}
</script>
