```javascript
const mtlLoader = new MTLLoader();
  mtlLoader.load(
    "https://raw.githubusercontent.com/fredysomy/3dmodels/main/torusball/torusball.mtl",
    (mtl1) => {
      mtl1.preload();
      const objLoader = new OBJLoader();
      objLoader.setMaterials(mtl1);
      objLoader.load(
        "https://raw.githubusercontent.com/fredysomy/3dmodels/main/torusball/torusball.obj",
        (root) => {
          scene.add(root);
          root.position.set(0, -4, 0);
        }
      );
    }
  );


```
