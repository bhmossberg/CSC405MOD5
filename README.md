# CSC405MOD5

**CSC405 Computer Graphics, CSU Global (Winter 2026, Session A). Module 5: Viewing**

OpenGL Java interactive viewer.

## Enabling Objectives

By the end of this module, you will be able to:

1. Characterize classical viewing.
2. Compare and contrast computer viewing.
3. Describe positioning of the camera.
4. Examine hidden-surface removal.
5. Examine perspective projections.

## Readings

**Required**

- Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning.
  - Chapter 3
    - Section 3.7: Eye Space and the Synthetic Camera
    - Section 3.8: Projection Matrices
    - Section 3.9: Look-At Matrix
    - Section 3.10: GLSL Functions for Building Matrix Transforms
  - Chapter 4
    - Section 4.4: Model-View and Perspective Matrices
    - Section 4.7: Rendering Multiple Different Models
    - Section 4.8: Matrix Stacks
    - Section 4.9: Combatting Z-Fighting
    - Section 4.10: Other Options for Primitives

**Recommended**

- Akenine-Möller, T., Haines, E., Hoffman, N., Pesce, A., Iwanicki, M., & Hillaire, S. (2022). Real-time rendering (4th ed.). A K Peters / CRC Press.
  - Chapter 4: Transforms — https://learning-oreilly-com.csuglobal.idm.oclc.org/library/view/real-time-rendering-fourth/9781351816144/xhtml/ch04.xhtml

## Assignment: Module 5: Portfolio Milestone

Interactive Viewer (80 Points)

Read Chapter 3, Sections 3.7–3.10 and Chapter 4, Sections 4.4 and 4.7–4.10 of Gordon & Clevenger (2021). Pay close attention to how the look-at matrix and the perspective projection matrix combine in the model-view–projection chain.

In a 1–2 paragraph Word document, briefly discuss the role of the projection matrix and the look-at matrix in OpenGL viewing, citing the textbook.

Then, using Java with JOGL and JOML, build an interactive viewer based on the cube (or a model of your choice) you produced in Module 4. Your program must:

Allow the user to translate the camera in 3D space (e.g., WASD keys for forward/back/left/right, Q/E for down/up).

Allow the user to look around (e.g., arrow keys or mouse drag), updating the look-at matrix from a yaw/pitch state.

Display at least two distinct objects in the scene (use the matrix-stack / separate model-view matrix pattern from Section 4.7).

This milestone is the foundation for your Module 8: Portfolio Project — keep your code organized!


### Submission Guidelines

Your Java source files and shaders.

A screenshot of your viewer with both objects visible.

The 1–2 paragraph discussion Word document.

Your paper must be formatted according to APA guidelines in the CSU Global Writing Center (available in the left-hand navigation panel).

Refer to the rubric below for more details about how you will be graded for this assignment.

