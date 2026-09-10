Concept    
The artifact is imagined as a high-energy reactor core recovered by Techfest engineers: a glowing metallic sphere sealed inside layered protective lattices, orbited by control nodes and stabilizing rings. Visitors act as operators at a diagnostic console, able to rotate around the core, probe it with the cursor, trigger energy impulses, and monitor its telemetry live through the HUD.

   
Key Features
Central Hero Mesh      
Multi-layered procedural object: emissive MeshPhysicalMaterial core with clearcoat, an additive glow halo, a faceted metallic icosahedral shell, dual wireframe icosahedrons, twin torus rings, and six orbiting octahedral nodes.
Every layer rotates independently on X, Y and Z axes, with a gentle floating motion.
Deep-Space Particle Field
   
2,200 particles generated with BufferGeometry and rendered via THREE.Points using a custom vertex/fragment shader for soft, pulsing, depth-scaled light points.
Particles slowly drift and rebound within a spherical volume for a living background.
Cinematic Lighting   

Ambient base light (#111122) plus two high-intensity orbiting point lights in Neon Cyan (#00f3ff) and Cyber Magenta (#ff0055) that pulse and swap colors on interaction, producing rich specular highlights on the metallic surfaces.
Camera & Interaction    

Perspective camera controlled by damped OrbitControls (zoom enabled, pan disabled, slow auto-rotate).
Mouse raycasting: hovering the core scales it up, intensifies its glow, shifts the lighting, and reveals a cursor-following telemetry panel; clicking fires a scale pulse, light surge, and a status alert.
HUD Overlay
      
Top-left branding with live FPS, frame counter and sync indicator.
Top-right controls to cycle rotation speed, switch between five core shader palettes (recoloring both the 3D scene and the UI), and smoothly reset the camera.
Bottom diagnostics panel streaming rotation vector, core temperature (340 K baseline), vertex count, light frequency, particle count, camera distance and core state.
Cyberpunk aesthetics: dark glassmorphism, neon borders, angled corner cuts, scanline overlay, and Orbitron/Rajdhani typography.






Technology Stack:  
HTML5, CSS3, vanilla JavaScript (ES5-compatible IIFE)  
Three.js r128 + OrbitControls via CDN  
Custom GLSL shaders for the particle system  
Google Fonts (Orbitron, Rajdhani)  
Performance & Responsiveness  
Single requestAnimationFrame loop targeting 60 FPS  
Device pixel ratio capped at 2, throttled DOM updates, ACES tone mapping  
Renderer and camera aspect automatically adapt to window resize; HUD reflows for mobile screens   


Deliverable

One self-contained index.html file — open it in any modern browser and the experience runs immediately with no installation or server required.
