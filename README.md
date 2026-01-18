_**Case Study, Shader based scanning**_


**Gameplay**

This project is a casual game inspired by popular “hidden imposter” mechanics. The core gameplay loop revolves around identifying disguised invaders hidden among a group of non-player characters (NPCs). Within each level, 
the environment is populated by multiple characters that appear visually identical on the surface. Some of these characters are harmless NPCs, while others are imposters. The player is equipped with a  scanner that can be used 
to inspect characters and a laser gun to shoot if invader found.
When an NPC is scanned, the scanner reveals an internal skeletal structure, confirming that the character is human. When an imposter is scanned, the scanner instead exposes the alien hidden beneath the surface of character. 
This reveal mechanic creates a clear and intuitive deduction system, allowing players to identify targets based on visual feedback rather than abstract indicators. 

**Problems Encountered**

The primary technical challenge in this project was achieving the scanner reveal effect while maintaining strong graphical performance on mobile devices. The core mechanic relied on real-time visual transformations, 
which can be computationally expensive if implemented naïvely.
The reveal system was implemented using custom shaders that selectively altered character rendering based on scan state. NPCs and imposters shared a common base model, but the shader dynamically switched rendering layers to 
expose either skeleton structures or hidden imposter visuals.
Early implementations caused noticeable performance drops, particularly when scanning multiple characters in quick succession. To address this, the rendering pipeline was carefully optimized by minimizing shader complexity, 
reducing overdraw, and reusing shared materials wherever possible. Visual fidelity was balanced against performance to ensure consistent frame rates across a wide range of devices.
Another challenge involved ensuring that the scanner feedback was both visually clear and performant. The effect needed to be instantly readable by the player without relying on expensive post-processing or multiple render passes.
Iterative profiling and optimization were key to achieving a stable and scalable solution. 

**Learning** 

By implementing a shader-based scanning and reveal system, I gained hands-on experience with GPU-driven visual effects and the practical constraints of mobile hardware. The project reinforced the importance of performance-aware 
rendering techniques, including material reuse, shader simplification, and draw-call optimization.
From a systems perspective, the project deepened my understanding of how gameplay mechanics and rendering pipelines interact. The scanner was not merely a visual effect, but a gameplay-critical system that required tight integration
between logic, rendering, and user feedback—an essential concept in real-time interactive systems.
Additionally, developing this game in a professional studio environment strengthened my awareness of production constraints, including device diversity, optimization targets, and clean separation between proprietary assets and 
reusable technical concepts. This experience reflects industry-aligned practices emphasized in applied game technology programs.
Overall, this project demonstrates my ability to design and optimize visually driven gameplay systems under real-world performance constraints. It highlights applied knowledge of graphics programming, real-time systems, and 
optimization strategies, aligning well with the technical and interdisciplinary expectations of graduate-level study in Game Technologies.


This project was developed as part of my professional work at a mobile game studio. The case study focuses solely on publicly observable mechanics and my technical contributions, with all proprietary assets and internal details 
omitted.”

Game Link: https://play.google.com/store/apps/details?id=com.hb.find.the.invader
