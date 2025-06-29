<div align="center">

# � THE BACKROOMS 🌟
### *Đồ án môn học CS105 - Đồ hoạ máy tính*

<img src="https://img.shields.io/badge/Three.js-v0.149.0-black?style=for-the-badge&logo=three.js&logoColor=white"/>
<img src="https://img.shields.io/badge/WebGL-2.0-red?style=for-the-badge&logo=webgl&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-ES6+-yellow?style=for-the-badge&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/GLSL-Shaders-purple?style=for-the-badge&logo=opengl&logoColor=white"/>

*Trải nghiệm kinh dị 3D immersive được xây dựng từ đầu với công nghệ WebGL hiện đại*

---

</div>

## 👥 Đội ngũ phát triển

| Thành viên | MSSV | Vai trò & Đóng góp |
|------------|------|-------------------|
| **🏆 Nguyễn Khang Hy** | 23520662 | **Trưởng nhóm & Lập trình viên chính**<br/>• Phát triển Engine cốt lõi<br/>• Xây dựng hoàn chỉnh hệ thống Shader<br/>• Hệ thống Animation & Physics nâng cao<br/>• Tối ưu hiệu năng & Thiết kế kiến trúc<br/>• Tài liệu kỹ thuật & Thuyết trình |
| **Phùng Văn Đạt** | 22520234 | **Lập trình Gameplay**<br/>• Triển khai logic trò chơi<br/>• Phát triển hệ thống AI<br/>• Kiểm thử & Sửa lỗi |
| **Lê Văn Giáp** | 22520363 | **Lập trình Đồ họa**<br/>• Tích hợp mô hình 3D<br/>• Hệ thống phát hiện va chạm<br/>• Hỗ trợ hiệu ứng thị giác |
| **Trần Giang Sư** | 22522166 | **Lập trình Audio & Giao diện**<br/>• Tích hợp hệ thống âm thanh<br/>• Phát triển giao diện người dùng<br/>• Hỗ trợ hiệu ứng post-processing |

**Giảng viên hướng dẫn:** ThS. Cấp Phạm Đình Thắng  
**Lớp:** CS105.P22  
**Học kỳ:** II - Năm học 2024-2025

---

## 🎯 Tổng quan dự án

**The Backrooms** là một trải nghiệm kinh dị 3D được phát triển hoàn toàn bằng **Three.js** và **WebGL**, tái hiện không gian đáng sợ và bí ẩn của "Backrooms" - một hiện tượng internet nổi tiếng. Dự án thể hiện sự ứng dụng sâu sắc các kỹ thuật đồ hoạ máy tính hiện đại.

### ✨ Điểm nổi bật
- 🎨 **6 Shader tùy chỉnh** được viết hoàn toàn từ đầu với GLSL
- 🏃‍♂️ **Hệ thống Animation nâng cao** với 7 trạng thái chuyển động phức tạp
- 🔊 **Hệ thống âm thanh không gian 3D** với 11 hiệu ứng âm thanh đắm chìm
- 🎮 **Điều khiển FPS tùy chỉnh** với phát hiện va chạm chính xác pixel-perfect
- 🌟 **Pipeline xử lý đa lượt** với 6 hiệu ứng post-processing
- 📱 **Tối ưu hiệu năng** cho cả máy tính để bàn và thiết bị di động
- 🧠 **Hệ thống AI tìm đường** cho hành vi của SCP-096 entity

---

## 🚀 Công nghệ & Kiến trúc

### 🎨 **Engine Đồ họa Cốt lõi**
```javascript
Three.js v0.149.0     // Engine render 3D WebGL
GLTFLoader           // Tải mô hình 3D (định dạng .glb)
PointerLockControls  // Hệ thống camera góc nhìn thứ nhất
AnimationMixer       // Animation phức tạp cho nhân vật
```

### 🎭 **Hệ thống Shader Tùy chỉnh**
Được phát triển với **GLSL (OpenGL Shading Language)**:

| Shader | Chức năng | Tham số chính |
|--------|-----------|---------------|
| **RGBShiftShader** | Chromatic aberration effect | `amount`, `angle` |
| **FilmShader** | Retro film grain & scanlines | `nIntensity`, `sCount` |
| **StaticShader** | TV static noise effect | `amount`, `size` |
| **BadTVShader** | TV distortion simulation | `distortion`, `speed` |
| **VignetteShader** | Edge darkening effect | `offset`, `darkness` |
| **UnrealBloomPass** | HDR bloom lighting | `threshold`, `strength` |

### 🎵 **Hệ thống Âm thanh Nâng cao**
```javascript
Spatial Audio        // Hiệu ứng âm thanh vị trí 3D
Dynamic Mixing       // Điều khiển âm lượng nhạc nền & SFX
Ambient Soundscape   // Xoay vòng 3 track nhạc nền
Interactive SFX      // 11 hiệu ứng âm thanh gameplay
```

### 🏗️ **Kiến trúc hệ thống**
```
src/
├── 🎮 objects/
│   ├── Player.js         # Character animation system (7 states)
│   ├── Door.js           # Interactive door mechanics
│   ├── EndingDoor.js     # Victory condition handler
│   ├── Glowstick.js      # Collectible item system
│   └── scp-096.js        # AI enemy with pathfinding
├── 🔊 audio.js           # Spatial audio manager
shader/
├── 🎨 Custom GLSL Shaders (6 effects)
├── 📦 UnrealBloomPass.js # HDR bloom implementation
utils/
├── 🗺️ FixedMapLayout.js  # Level design data
├── 🔧 optimize_map_by_0.js # Performance utilities
```

---

## 🎮 Gameplay & Features

### 🕹️ **Điều khiển**
| Phím | Hành động | Mô tả |
|------|-----------|-------|
| `W A S D` | Di chuyển | Chuyển động nhân vật |
| `Chuột` | Nhìn | Xoay camera |
| `Shift` | Chạy | Tăng tốc độ di chuyển |
| `C` | Cúi | Di chuyển lén lút |
| `F` | Đèn pin | Bật/tắt ánh sáng |
| `E` | Tương tác | Mở cửa |
| `X` | Quan sát | Chế độ camera tự do |
| `M` | Bản đồ | Bật/tắt minimap |

### 🎯 **Mục tiêu Game**
1. **Khám phá** mê cung vô hạn của những căn phòng màu vàng
2. **Thu thập** 4 glowstick rải rác trong bản đồ  
3. **Tìm kiếm** cửa thoát (cần có đủ glowstick)
4. **Sinh tồn** trước SCP-096 entity đang rình rập
5. **Thoát ra** để giành chiến thắng

### 🔮 **Tính năng Nâng cao**
- **Hệ thống ánh sáng động**: Bóng đổ và chiếu sáng thời gian thực
- **Phát hiện va chạm**: Va chạm chính xác với tường và vật thể
- **Máy trạng thái Animation**: Chuyển đổi mượt mà giữa các trạng thái
- **Giám sát hiệu năng**: FPS và tối ưu hóa thời gian thực
- **Âm thanh không gian hóa**: Hiệu ứng âm thanh vị trí 3D
- **Hot-reload Shader**: Điều chỉnh hiệu ứng thị giác thời gian thực

---

## 🛠️ **Triển khai Kỹ thuật**

### 📊 **Tối ưu Hiệu năng**
```javascript
// Điều chỉnh chất lượng động
renderer.setPixelRatio(window.devicePixelRatio * 0.5);

// Hệ thống giới hạn FPS
const maxFPS = 100;
let lastTime = performance.now();

// Bật/tắt shader cho thiết bị yếu
const shadersToggled = true;
```

### 🎨 **Pipeline Shader**
```glsl
// Ví dụ: RGB Shift Fragment Shader
uniform sampler2D tDiffuse;
uniform float amount;
uniform float angle;

void main() {
    vec2 offset = amount * vec2(cos(angle), sin(angle));
    vec4 cr = texture2D(tDiffuse, vUv + offset);
    vec4 cga = texture2D(tDiffuse, vUv);
    vec4 cb = texture2D(tDiffuse, vUv - offset);
    gl_FragColor = vec4(cr.r, cga.g, cb.b, cga.a);
}
```

### 🎭 **Hệ thống Animation**
```javascript
// Quản lý trạng thái nhân vật
const ANIMATION_STATES = {
  IDLE: 'idle',
  WALKING: 'walking', 
  RUNNING: 'running',
  JUMPING: 'jumping',
  CROUCHING: 'crouching',
  CROUCH_WALKING: 'crouch_walking',
  WALKING_BACKWARD: 'walking_backward'
};
```

---

## 🚀 **Cài đặt & Thiết lập**

### 📋 **Yêu cầu**
- Trình duyệt hiện đại hỗ trợ **WebGL 2.0**
- Tương thích **ES6 Modules**
- Kết nối internet ổn định (phụ thuộc CDN)

### ⚡ **Khởi động Nhanh**

1. **Clone repository**
```bash
git clone [repository-url]
cd Computer_Graphics
```

2. **Khởi động server local**

**Tùy chọn A: Python**
```bash
python -m http.server 8000
```

**Tùy chọn B: Node.js**
```bash
npm install -g http-server
http-server -p 8000
```

**Tùy chọn C: PHP**
```bash
php -S localhost:8000
```

3. **Chạy game**
```
http://localhost:8000
```

### 🎛️ **Chế độ Phát triển**
Bật giao diện debug để điều chỉnh tham số thời gian thực:
- Cài đặt đồ họa (pixel ratio, ánh sáng)
- Tham số shader (cường độ, méo hình)
- Cài đặt gameplay (tốc độ di chuyển, va chạm)
- Giám sát hiệu năng (FPS, sử dụng bộ nhớ)

---

## 📁 **Project Structure**

```
Backrooms-Game/
├── 📄 index.html              # Main HTML entry point
├── 🎮 main.js                 # Core game engine & logic
├── 🎨 style.css               # UI styling & animations
├── 📝 README.md               # Project documentation
├── 🔧 PointerLockControls.js  # Custom FPS camera controller
│
├── 📂 src/
│   ├── 🔊 audio.js            # Spatial audio management
│   └── 📂 objects/
│       ├── Player.js          # Character system & animations
│       ├── Door.js            # Interactive door mechanics
│       ├── EndingDoor.js      # Victory condition handler
│       ├── Glowstick.js       # Collectible item system
│       └── scp-096.js         # AI enemy with pathfinding
│
├── 📂 shader/                 # Custom GLSL shader collection
│   ├── RGBShiftShader.js      # Chromatic aberration
│   ├── FilmShader.js          # Retro film grain
│   ├── StaticShader.js        # TV static noise
│   ├── BadTVShader.js         # CRT distortion
│   ├── VignetteShader.js      # Edge darkening
│   ├── UnrealBloomPass.js     # HDR bloom effect
│   └── 📂 glsl/               # Raw GLSL shader files
│
├── 📂 assets/                 # 3D models & audio assets
│   ├── 🎵 sounds/             # Audio files (11 tracks)
│   └── 🎯 *.glb               # 3D models (Player, Doors, etc.)
│
├── 📂 public/                 # Static assets & textures
│   ├── 🖼️ *.jpg, *.png        # Wall, floor, ceiling textures
│   ├── 📱 icon/               # Favicon & app icons
│   └── 🎭 models/             # Additional 3D assets
│
├── 📂 utils/                  # Utility functions & helpers
│   ├── FixedMapLayout.js      # Level design data
│   ├── optimize_map_by_0.js   # Performance optimization
│   └── script_gen_map.js      # Procedural map generation
│
└── 📂 docs/                   # Project documentation
    └── system-architecture-diagram.svg
```

---

## 🎓 **Thành tựu & Triển khai Kỹ thuật**

#### 🎨 **Lập trình Shader Nâng cao**
- **6 GLSL Shader tùy chỉnh** viết từ đầu với các kỹ thuật:
  - Tối ưu fragment shader cho hiệu năng
  - Kỹ thuật rendering đa lượt
  - Triển khai HDR tone mapping
  - Hiệu ứng méo hình thời gian thực

#### 🎮 **Kiến trúc Engine Game**
- **Bộ điều khiển FPS tùy chỉnh** với nội suy camera mượt mà
- **Hệ thống Animation dựa trên trạng thái** với chuyển đổi liền mạch
- **Engine phát hiện va chạm** sử dụng AABB và Ray casting
- **Hệ thống Profile hiệu năng** với giám sát thời gian thực

#### 🔧 **Đổi mới Kỹ thuật**
- **Điều chỉnh chất lượng động**: Tự động điều chỉnh chất lượng theo khả năng thiết bị
- **Quản lý bộ nhớ**: Tối ưu tải asset và streaming texture
- **Triển khai âm thanh không gian**: Audio vị trí 3D với độ suy giảm khoảng cách
- **Hệ thống hành vi AI**: State machine cho tìm đường của enemy

### 📚 **Các khái niệm Đồ họa Máy tính được Áp dụng**
- **Phép biến đổi 3D**: Ma trận Model, View, Projection
- **Mô hình ánh sáng**: Phong shading, shadow mapping
- **Texture Mapping**: UV mapping, normal mapping
- **Rasterization**: Fragment shader, depth testing
- **Post-processing**: Pipeline rendering đa lượt

### 🧮 **Nền tảng Toán học**
- **Đại số tuyến tính**: Phép toán vector, biến đổi ma trận
- **Lượng giác**: Xoay camera, nội suy animation
- **Phát hiện va chạm**: AABB, giao điểm ray-plane
- **Nội suy**: Chuyển đổi animation mượt mà

### 💻 **Kỹ thuật Lập trình**
- **Thiết kế hướng đối tượng**: Kiến trúc modular
- **Lập trình hướng sự kiện**: Xử lý input người dùng
- **Lập trình bất đồng bộ**: Tải asset, quản lý audio
- **Tối ưu hiệu năng**: LOD, culling, batching

---

## 🎨 **Trình diễn Thị giác**

### 🌟 **Bộ sưu tập Hiệu ứng Shader**

| Hiệu ứng | Preview | Mô tả |
|----------|---------|-------|
| **Chromatic Aberration** | `Tách kênh màu RGB` | Tạo hiệu ứng méo thấu kính |
| **Film Grain** | `Scanline + nhiễu retro` | Thẩm mỹ phim cổ điển |
| **TV Static** | `Nhiễu số` | Mô phỏng nhiễu điện tử |
| **CRT Distortion** | `Cong màn hình` | Mô phỏng TV cũ |
| **Vignette** | `Tối góc` | Hiệu ứng tập trung điện ảnh |
| **HDR Bloom** | `Tỏa sáng` | Render ánh sáng chói thực tế |

### 🎭 **Animation Nhân vật**
- **Idle**: Thở, chuyển động tinh tế
- **Walking**: Chu kỳ bước đi tự nhiên
- **Running**: Di chuyển nhịp độ nhanh
- **Crouching**: Tư thế ẩn nấp
- **Backward Walking**: Chuyển động lùi
- **Crouch Walking**: Di chuyển im lặng
- **Jumping**: Hành động nhảy dọc

---

## 🏆 **Ghi nhận & Cảm ơn**

### 🎨 **Tài nguyên 3D**
- **Mô hình Player**: [ETB Animated](https://sketchfab.com/3d-models/etb-animated-use-animation-dropdown-to-see-all-6795caee22124716bab954326306d3e3) từ Sketchfab
- **Mô hình Cửa**: [Lowpoly Animated Doors](https://sketchfab.com/3d-models/lowpoly-animated-doors-blender-file-58a65be7345348ada5f7f02374fdbefb) từ Sketchfab
- **Cửa Garage**: [Garage Door 01](https://sketchfab.com/3d-models/garage-door-01-fb7a0e3b6cf348f48831a80e49054609) từ Sketchfab
- **Glowstick**: [Glowstick Model](https://sketchfab.com/3d-models/glowstick-cbc7f31c658247219c32b083183513e5) từ Sketchfab
- **SCP-096**: [SCP-096 Model](https://sketchfab.com/3d-models/scp-096-7074212c3ba54d0d959c48c55b8fefce) từ Sketchfab

### 🔧 **Thư viện Mã nguồn Mở**
- **[Three.js](https://threejs.org/)**: Thư viện đồ họa 3D
- **[lil-gui](https://lil-gui.georgealways.com/)**: GUI nhẹ
- **[stats.js](https://github.com/mrdoob/stats.js/)**: Giám sát hiệu năng

### 🎵 **Tài nguyên Âm thanh**
- Nhạc nền và hiệu ứng âm thanh từ nhiều tác giả
- Triển khai âm thanh không gian sử dụng Web Audio API

---

## 📊 **Benchmark Hiệu năng**

### 🎯 **Thông số Mục tiêu**
- **FPS**: 60+ trên trình duyệt hiện đại
- **Sử dụng bộ nhớ**: < 200MB RAM
- **Thời gian tải**: < 5 giây
- **Hỗ trợ trình duyệt**: Chrome 90+, Firefox 88+, Safari 14+

### ⚡ **Kỹ thuật Tối ưu**
- Điều chỉnh pixel ratio động
- Giảm độ phức tạp shader
- Geometry instancing cho các đối tượng lặp lại
- Nén texture và mipmapping
- Frustum culling cho các đối tượng ngoài màn hình

---

## 🔮 **Cải tiến Tương lai**

### 🎮 **Tính năng Gameplay**
- [ ] Hỗ trợ multiplayer với WebRTC
- [ ] Tạo level tự động
- [ ] Mở rộng hệ thống inventory
- [ ] Nhiều kịch bản kết thúc
- [ ] Hệ thống thành tích

### 🎨 **Cải tiến Kỹ thuật**
- [ ] Chuyển đổi sang WebGPU để có hiệu năng tốt hơn
- [ ] Triển khai ray tracing
- [ ] Hệ thống particle nâng cao
- [ ] Tích hợp physics engine
- [ ] Hỗ trợ VR/AR

---

<div align="center">

## 🌟 **Lời kết**

*Dự án "The Backrooms" là thành quả của sự tận tâm và đam mê trong việc áp dụng đồ họa máy tính. Dự án này thể hiện sự hiểu biết sâu sắc về WebGL, lập trình GLSL shader, và các kỹ thuật đồ họa 3D hiện đại trên nền web.*

*Từ việc triển khai pipeline shader tùy chỉnh đến tối ưu hóa cho hiệu năng thời gian thực, mỗi dòng code đều được xây dựng cẩn thận để mang đến trải nghiệm kinh dị đắm chìm.*

**Được phát triển với ❤️ và vô số giờ debug bởi nhóm CS105.P22**  

---

### 📞 **Thông tin Liên hệ**
- **Repository**: [[GitHub Link](https://github.com/HyIsNoob/CS105_GraphicComputer)]
- **Demo**: [[Link Demo trực tiếp](https://drive.google.com/file/d/1brc2R_6W8Wy-5CQ7RMRRmxshyZQgEdG-/view?usp=drive_link)]  
- **Tài liệu**: [[Trang Wiki](https://drive.google.com/file/d/1pIifxtme1o0zXL_oUdHaVv939BXG82_2/view?usp=drive_link)]

<img src="https://img.shields.io/badge/Made%20with-Three.js-black?style=for-the-badge&logo=three.js"/>
<img src="https://img.shields.io/badge/Powered%20by-WebGL-red?style=for-the-badge&logo=webgl"/>
<img src="https://img.shields.io/badge/Built%20with-❤️-red?style=for-the-badge"/>

</div>

## 👨‍💻 **Góc nhìn & Đóng góp của Developer**

**Đóng góp chính (70% codebase):**
- ✅ **Hệ thống Shader hoàn chỉnh**: 6 GLSL shader tùy chỉnh từ đầu
- ✅ **Engine Animation**: Hệ thống animation 7 trạng thái
- ✅ **Logic Game cốt lõi**: Di chuyển player, phát hiện va chạm, cơ chế game
- ✅ **Tối ưu hiệu năng**: Giới hạn FPS, điều chỉnh chất lượng, quản lý bộ nhớ
- ✅ **Thiết kế kiến trúc**: Thiết kế hệ thống modular và tổ chức code
- ✅ **Tài liệu kỹ thuật**: Comment code, README, và thông số kỹ thuật

**Thống kê Phát triển:**
```
Tổng số dòng code: ~2500+ dòng
Code Shader (GLSL): ~800 dòng
Engine cốt lõi (JavaScript): ~1200 dòng
Hệ thống Audio/UI: ~500 dòng
```

**Đầu tư Thời gian:**
- Nghiên cứu & Lập kế hoạch: 2 tuần
- Phát triển cốt lõi: 6 tuần  
- Kiểm thử & Tối ưu: 1 tuần
- Tài liệu hóa: 1 tuần

### 👥 **Hợp tác Nhóm**
Mặc dù chủ yếu được phát triển bởi **Nguyễn Khang Hy**, nhóm đã cung cấp hỗ trợ quý giá:
- **Code review và kiểm thử** bởi các thành viên nhóm
- **Tích hợp asset** và triển khai tính năng cơ bản
- **Hỗ trợ tài liệu** và chuẩn bị thuyết trình
- **Báo cáo lỗi** và phản hồi trải nghiệm người dùng

---
