
### 1. 실습화면
![image](https://github.com/qkrgudals1030/quizai/assets/50895124/53e2ae37-db91-4ab1-a484-d64d237a9665)

### 1. p5.js의 특징
1. 웹 친화성: p5.js는 자바스크립트 기반으로, HTML, CSS와 쉽게 통합되어 웹 페이지에서 직접 실행할 수 있습니다.
2. 간단한 문법: 복잡한 그래픽스 프로그래밍을 간단한 코드로 표현할 수 있습니다.
3. 인터랙티브 기능: 사용자의 입력(마우스, 키보드 등)에 반응하는 인터랙티브 프로그램을 쉽게 작성할 수 있습니다.
4. 다양한 내장 함수: 드로잉, 애니메이션, 3D 그래픽, 데이터 시각화 등을 위한 풍부한 함수들을 제공합니다.
5. 크로스 플랫폼: 다양한 브라우저와 플랫폼에서 일관되게 작동합니다.

### 인터랙티브 아트의 개념

인터랙티브 아트는 사용자의 입력이나 상호작용에 반응하는 예술 형식입니다. 이는 디지털 기술을 활용하여 관객이 작품에 직접 참여하고, 작품의 일부가 되도록 합니다. p5.js를 이용하면 이런 인터랙티브 아트를 손쉽게 구현할 수 있습니다. 예를 들어, 마우스 움직임에 따라 화면의 그래픽이 변하거나, 키보드 입력에 따라 색상이 바뀌는 등의 인터랙티브 요소를 추가할 수 있습니다.

### 예제 코드 작성 및 설명
```
function setup() {
  createCanvas(windowWidth, windowHeight);
  background(255);
}

function draw() {
  fill(0,255,0);
  ellipse(mouseX, mouseY, 50, 50);
}
```

#### 코드설명
이 코드는 사용자가 마우스를 움직일 때마다 그 위치에 원이 그려지도록 합니다. 매 프레임마다 새로운 원이 그려지기 때문에, 마우스를 움직이면 마치 그려진 궤적을 따라 원들이 찍히는 효과가 나타나게됩니다. 해당 코드는 초록색원이 출력되도록 설정하였습니다.

### 2. ml5.js의 기능과 장점

ml5.js는 머신러닝을 쉽게 사용할 수 있도록 도와주는 자바스크립트 라이브러리입니다. 주로 웹 개발자나 초보자를 위해 설계되었으며, TensorFlow.js 위에 구축되었습니다. 
1. 간단한 API: 복잡한 머신러닝 모델을 간단한 함수 호출로 사용할 수 있습니다.
2. 웹 친화성: 웹 브라우저에서 바로 실행 가능하며, HTML, CSS와 쉽게 통합할 수 있습니다.
3. 다양한 모델 지원: 이미지 분류, 객체 인식, 포즈 추정, 텍스트 생성 등 다양한 머신러닝 모델을 제공합니다.
4. 프리 트레이닝 모델 사용 가능: 사전 학습된 모델을 바로 사용할 수 있어 빠른 프로토타이핑이 가능합니다.
5. 오픈소스: 누구나 사용할 수 있고, 커뮤니티의 기여로 지속적으로 발전하고 있습니다.


### 이미지 분류 모델 구현 과정
1. 데이터 준비: 분류하고자 하는 이미지 데이터셋을 준비합니다.
2. 모델 로드: ML5.js에서 제공하는 사전 학습된 모델(예: MobileNet)을 로드합니다.
3. 모델 예측: 입력 이미지를 모델에 전달하여 예측 결과를 얻습니다.
4. 결과 처리: 예측 결과에서 가장 높은 확률의 클래스를 선택하여 이미지 분류 결과를 출력합니다.

### 이미지 분류 모델의 원리

이미지 분류 모델은 합성곱 신경망(Convolutional Neural Network, CNN) 알고리즘을 사용합니다. CNN은 이미지의 특징을 자동으로 추출하고, 이를 바탕으로 이미지를 분류하는 방식입니다.
CNN 모델은 합성곱 층, 풀링 층, 완전 연결 층으로 구성되어 있습니다. 합성곱 층은 이미지의 지역적 특징을 추출하고, 풀링 층은 특징 맵의 크기를 줄여 연산량을 감소시킵니다. 완전 연결 층에서는 추출된 특징을 바탕으로 이미지를 분류합니다.


### 3. 실습화면

![project3](https://github.com/qkrgudals1030/quizai/assets/50895124/dc6766e3-92af-4c5b-a40a-e2b1df376d72)


### 3. three.js의 주요 구성 요소 설명
three.js는 웹에서 3D 그래픽스를 구현하기 위한 자바스크립트 라이브러리입니다. 주요 구성 요소는 다음과 같습니다:

1. Scene (장면): 3D 객체들이 배치되는 공간입니다. 모든 객체는 장면(Scene)에 추가되어야 렌더링할 수 있습니다.
2. Camera (카메라): 장면을 바라보는 시점입니다. 일반적으로 원근 카메라(PerspectiveCamera)나 정사영 카메라(OrthographicCamera)를 사용합니다.
3. Renderer (렌더러): 장면과 카메라를 기반으로 화면에 3D 그래픽스를 그리는 역할을 합니다. 웹GLRenderer가 가장 많이 사용됩니다.
4. Mesh (메시): 기하학적 형상(Geometry)과 표면 특성(Material)을 결합한 객체로, 3D 장면을 구성하는 기본 단위입니다.
5. Light (조명): 장면에 빛을 추가하여 객체를 더 현실적으로 보이게 합니다. AmbientLight, PointLight, DirectionalLight 등이 있습니다.
6. Geometry (기하학): 3D 객체의 형태를 정의합니다. BoxGeometry, SphereGeometry 등이 있습니다.
7. Material (재질): 객체의 표면 특성을 정의합니다. MeshBasicMaterial, MeshStandardMaterial 등이 있습니다.


### 3D 장면 구성 과정

three.js를 사용하여 3D 장면을 구성하는 과정은 다음과 같습니다:

1. 장면 생성: new THREE.Scene()을 사용하여 장면을 생성합니다.
2. 카메라 생성: new THREE.PerspectiveCamera()를 사용하여 카메라를 생성하고 위치를 설정합니다.
3. 렌더러 생성: new THREE.WebGLRenderer()를 사용하여 렌더러를 생성하고, 크기를 설정한 후 HTML 문서에 추가합니다.
4. 메시 생성: 기하학과 재질을 결합하여 메시를 생성하고, 장면에 추가합니다.
5. 조명 추가: 다양한 조명을 생성하고 장면에 추가합니다.
6. 애니메이션 루프 설정: requestAnimationFrame()을 사용하여 애니메이션 루프를 설정하고, 렌더링을 반복합니다.

### 예제 코드 작성 및 설명

```
import * as THREE from '../build/three.module.js';

class App {
    constructor() {
        const divContainer = document.querySelector("#webgl-container");
        this._divContainer = divContainer;

        const renderer = new THREE.WebGL1Renderer({antialias: true});
        renderer.setPixelRatio(window.devicePixelRatio);
        divContainer.appendChild(renderer.domElement);
        this._renderer = renderer;

        const scene = new THREE.Scene();
        this._scene = scene;

        this._setupCamera();
        this._setupLight();
        this._setupModel();

        window.onresize = this.resize.bind(this);
        this.resize();

        requestAnimationFrame(this.render.bind(this));

        // 색상 변경 타이머 설정
        this.colorChangeInterval = 3; // 3초마다 색상 변경
        this.lastColorChangeTime = 0;
    }

    _setupCamera() {
        const width = this._divContainer.clientWidth;
        const height = this._divContainer.clientHeight;
        const camera = new THREE.PerspectiveCamera(
            75,
            width / height,
            0.1,
            100
        );
        camera.position.z = 2;
        this._camera = camera;
    }

    _setupLight() {
        const color = 0xffffff;
        const intensity = 1;
        const light = new THREE.DirectionalLight(color, intensity);
        light.position.set(-1, 2, 4);
        this._scene.add(light);
    }

    _setupModel() {
        const geometry = new THREE.BoxGeometry(1, 1, 1);
        const material = new THREE.MeshPhongMaterial({color: 0x44a88});

        const cube = new THREE.Mesh(geometry, material);
        this._scene.add(cube);
        this._cube = cube;
    }

    resize() {
        const width = this._divContainer.clientWidth;
        const height = this._divContainer.clientHeight;

        this._camera.aspect = width / height;
        this._camera.updateProjectionMatrix();

        this._renderer.setSize(width, height);
    }

    render(time) {
        this._renderer.render(this._scene, this._camera);
        this.update(time);
        requestAnimationFrame(this.render.bind(this));
    }

    update(time) {
        time *= 0.001;
        this._cube.rotation.x = time;
        this._cube.rotation.y = time;

        // 3초마다 색상 변경
        if (time - this.lastColorChangeTime > this.colorChangeInterval) {
            const randomColor = Math.random() * 0xffffff;
            this._cube.material.color.set(randomColor);
            this.lastColorChangeTime = time;
        }
    }
}

window.onload = function() {
    new App()
}
```
#### 코드설명

위 코드는 회전하는 큐브로 일정시간이 지나면 색상이 랜덤하게 변하도록 코드를 작성해보았습니다.
Three.js의 기본 기능을 사용하여 3D 큐브를 렌더링하고 애니메이션화합니다. 특히 색상 변경 기능을 추가하여 더욱 인터랙티브한 요소를 포함하고 있습니다.

### 4. 실습화면

![image](https://github.com/qkrgudals1030/quizai/assets/50895124/6ba8a048-7bf6-4945-999d-3b6ed8f07ff8)

![image](https://github.com/qkrgudals1030/quizai/assets/50895124/20f742f3-de33-49cc-a818-9f54edcc3098)


### 4. R3F의 특징 및 이점

React Three Fiber(R3F)는 React를 사용하여 Three.js로 3D 그래픽스를 쉽게 구현할 수 있도록 돕는 라이브러리입니다. 주요 특징과 이점은 다음과 같습니다:

1. React와의 완벽한 통합: R3F는 React 컴포넌트로 Three.js 장면을 구성할 수 있게 해줍니다. React의 상태 관리, 라이프사이클 메서드 등을 3D 그래픽스와 통합할 수 있습니다.
2. 컴포넌트 기반 개발: R3F는 3D 그래픽스를 React 컴포넌트로 분리하여 재사용성과 유지보수성을 높입니다.
3. Declarative API: 선언형 API를 사용하여 코드를 직관적이고 쉽게 작성할 수 있습니다. JSX 문법을 활용하여 Three.js 객체를 정의합니다.
4. React 생태계와 호환: React의 훅, 컨텍스트, 라우터 등과 자연스럽게 통합할 수 있어 더 복잡한 애플리케이션을 쉽게 개발할 수 있습니다.
5. Three.js 기능의 손쉬운 사용: Three.js의 강력한 기능을 그대로 사용하면서도 React의 편리한 개발 방식을 활용할 수 있습니다.


### R3F를 사용한 3D 장면 생성 과정

1. React 프로젝트 설정: Create React App이나 Vite를 사용하여 React 프로젝트를 설정합니다.
2. React Three Fiber 설치: npm install @react-three/fiber three 명령어로 R3F와 Three.js를 설치합니다.
3. Canvas 컴포넌트 사용: R3F의 Canvas 컴포넌트를 사용하여 3D 장면을 렌더링할 공간을 만듭니다.
4. 3D 객체 추가: R3F의 컴포넌트를 사용하여 3D 객체를 추가하고, React 훅을 사용하여 애니메이션을 설정합니다.


### 예제 코드 작성 및 설명

#### MyElement3D.jsx
```
import { OrbitControls } from "@react-three/drei";
import { useControls } from "leva";
import { useEffect, useRef } from "react";
import * as THREE from "three";

function MyElement3D() {
  const refMesh = useRef();
  const refWireMesh = useRef();

  const { shape, xSize, ySize, zSize, xSegments, ySegments, zSegments } = useControls({
    shape: { value: "Box", options: ["Box", "Sphere", "Cylinder", "Torus", "Cone", "Dodecahedron"] },
    xSize: { value: 1, min: 0.1, max: 5, step: 0.01 },
    ySize: { value: 1, min: 0.1, max: 5, step: 0.01 },
    zSize: { value: 1, min: 0.1, max: 5, step: 0.01 },
    xSegments: { value: 1, min: 1, max: 10, step: 1 },
    ySegments: { value: 1, min: 1, max: 10, step: 1 },
    zSegments: { value: 1, min: 1, max: 10, step: 1 },
  });

  useEffect(() => {
    refWireMesh.current.geometry = refMesh.current.geometry;
  }, [xSize, ySize, zSize, xSegments, ySegments, zSegments]);

  // 바닥 생성
  const floorGeometry = new THREE.PlaneGeometry(20, 20);
  const floorMaterial = new THREE.MeshStandardMaterial({ color: 0x808080, side: THREE.DoubleSide });
  const floor = new THREE.Mesh(floorGeometry, floorMaterial);
  floor.receiveShadow = true;

  // 선택된 모양에 따라 해당하는 Three.js의 기하학을 생성
  let geometry;
  switch (shape) {
    case "Sphere":
      geometry = new THREE.SphereGeometry(xSize, ySegments, zSegments);
      break;
    case "Cylinder":
      geometry = new THREE.CylinderGeometry(xSize, ySize, zSize, xSegments, ySegments);
      break;
    case "Torus":
      geometry = new THREE.TorusGeometry(xSize, ySize, xSegments, ySegments);
      break;
    case "Cone":
      geometry = new THREE.ConeGeometry(xSize, ySize, zSize, xSegments, ySegments);
      break;
    case "Dodecahedron":
      geometry = new THREE.DodecahedronGeometry(xSize, zSegments);
      break;
    default:
      geometry = new THREE.BoxGeometry(xSize, ySize, zSize, xSegments, ySegments, zSegments);
      break;
  }

  return (
    <>
      <OrbitControls />

      <ambientLight intensity={0.5} />

      <directionalLight position={[5, 10, 7]} intensity={1} castShadow={true} shadow-mapSize-width={1024} shadow-mapSize-height={1024} />

      <mesh ref={refMesh} receiveShadow={true} castShadow={true}>
        <primitive object={geometry} />
        <meshPhysicalMaterial color="#1abc9c" roughness={0.5} metalness={0.5} />
      </mesh>

      <mesh ref={refWireMesh} receiveShadow={true} castShadow={true}>
        <meshPhysicalMaterial emissive="yellow" wireframe={true} />
      </mesh>

      <mesh rotation={[-Math.PI / 2, 0, 0]} position={[0, -2, 0]} receiveShadow>
        <planeGeometry args={[20, 20]} />
        <shadowMaterial opacity={0.5} />
      </mesh>
    </>
  );
}

export default MyElement3D;
```

#### app.jsx

```
import './App.css'
import { Canvas } from '@react-three/fiber'
import MyElement3D from './MyElement3D'

function App() {
  return (
    <>
    <Canvas>
      <MyElement3D />

    </Canvas>
    </>
  )
}

export default App
```

#### 코드설명
Sphere, Cylinder, Torus, Cone, Dodecahedron 해당 모형들을 선택하고 useControls를 사용하여 사용자가 3D 객체의 형태와 크기를 조정할 수 있는 UI를 제공합니다.
3F를 사용하여 다양한 형태의 3D 객체를 렌더링하고, 사용자가 인터페이스를 통해 실시간으로 객체의 속성을 변경할 수 있도록 합니다. Three.js의 강력한 3D 그래픽스 기능을 React와 결합하여 더욱 직관적인 개발 환경을 제공합니다.

### 소감

퀴즈시험을 통해 배웠던 내용을 한번더 학습해보는 느낌으로 깃허브에 정리를 해보면서 조금더 쉽게 위 내용들에 대해 공부해 볼 수 있었고 또한 모르는 내용에 대해서는 깃허브나 주변친구들의 도움을 받아 쉽게 해결해 볼 수 있었습니다. 또한 위 내용들만 정리를 하는 것이 아닌 이때까지 배웠던 내용들을 잘 정리하여 저만의 것으로 만들어 혼자힘으로 프로그래밍을 할 수 있도록 열심히 공부해 볼 것입니다. 수업시간에 배운내용들은 카페에 있는 내용을 잘 참고하여 공부하겠습니다. ai그래픽스 화이팅!! 감사합니다.







