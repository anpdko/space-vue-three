<template>
   <div class="back">
      <img src="@/assets/destination/background-destination-desktop.jpg" alt="">
   </div>
   <canvas ref="webGl" class="webGl" />
</template>

<script>
import {
   Scene,
   SphereGeometry,
   MeshStandardMaterial,
   Mesh,
   HemisphereLight,
   PerspectiveCamera,
   WebGLRenderer,
   TextureLoader,
} from "three";

import { OrbitControls } from "three/addons/controls/OrbitControls.js";
import { watch, onMounted, ref, computed } from "vue";
import { useWindowSize } from "@vueuse/core";

export default {
   props: {
    material: {
      type: String,
      required: true,
    },
  },
   setup(props) {
      const webGl = ref();
      const { width } = useWindowSize();
      let camera, renderer, scene, mesh, controls, light;
      
      const aspectRatio = computed(() => {
         return width.value / width.value;
      });

      const responseWidth = (width) => {
         if (width <= 1080) {
            return width / 2
         }
         return 540
      }

      const setCanvas = () => {
         // Create Scene
         scene = new Scene();
         // scene.background = new TextureLoader().load("/images/background-destination-desktop.jpg");

         // Create Object
         const geometry = new SphereGeometry(5, 50, 50);
         const material = new MeshStandardMaterial({
            map: new TextureLoader().load("/images/" + props.material),
         });
         mesh = new Mesh(geometry, material);
         scene.add(mesh);

         // Lights
         light = new HemisphereLight(0xffffff, 0x080820, 1);
         light.position.set(-50, 50, -25);
         scene.add(light);


         // Camera
         camera = new PerspectiveCamera(20, aspectRatio.value, 0.1, 100);
         camera.position.z = 30;
         scene.add(camera);
         camera.add(light);
         // camera.add(light2);

         // Renderer
         const canvas = webGl.value;
         renderer = new WebGLRenderer({ canvas, antialias: true, alpha: true });
         let size = responseWidth(width.value)
         renderer.setSize(size, size);
         renderer.render(scene, camera);

         // Controls
         controls = new OrbitControls(camera, canvas);
         controls.enableZoom = false;
         controls.enableDamping = true;
      };

      const updateCamera = () => {
         camera.aspect = aspectRatio.value;
         camera.updateProjectionMatrix();
      };

      const updateRenderer = () => {
         let size = responseWidth(width.value)
         renderer.setSize(size, size);
         renderer.render(scene, camera);
      };

      watch(width, (val) => {
         if (val) {
            updateCamera();
            updateRenderer();
         }
      });

      const animate = () => {
         mesh.rotation.y += 0.004;
         controls.update();
         renderer.render(scene, camera);
         requestAnimationFrame(animate);
      };

      onMounted(() => {
         setCanvas();
         animate();
      });

      return { webGl };
   },
};
</script>

<style scoped>
.webGl {
   background-color: transparent;
}
</style>