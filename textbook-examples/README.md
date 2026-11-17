# CSC405 Module 5 — Textbook Example Programs

Example code from Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning and Information. Used for coursework study.

Official companion files were downloaded from the author’s page,
[Computer Graphics Programming in OpenGL with Java, 3rd Edition](https://athena.ecs.csus.edu/~gordonvs/textJ3E.html)
(`J3E_CompanionFiles.zip`). Each program folder is self-contained:
its `.java` sources, `.glsl` shaders, utility classes (`Utils.java`,
`Sphere.java`, `Torus.java`, `ImportedModel.java` as needed), and any
textures or models that program loads are copied into that folder.

**Assigned reading:** Chapter 3, Sections 3.7–3.10; Chapter 4, Sections 4.4 and 4.7–4.10.

## Programs in this module

### Program3_1 — Building Transformation Matrices in GLSL

- **Section:** 3.10 GLSL Functions for Building Matrix Transforms
- **Source:** transcribed from the book listing (no official companion folder).
- **Note:** Overlap: also in Module 4, which assigns all of Chapter 3. GLSL-only; see the note under Module 4.

### Program4_3 — Cube and Pyramid

- **Section:** 4.7 Rendering Multiple Different Models in a Scene
- **Official folder:** `Chapter_04_graphicsData/Prog4_3_multipleModels`

### Program4_4 — Simple Solar System Using Matrix Stack

- **Section:** 4.8 Matrix Stacks
- **Official folder:** `Chapter_04_graphicsData/Prog4_4_matrixStack`

## Assigned sections without a numbered program

- Section 4.4 (model-view and perspective matrices) is used by Programs 4.3 and 4.4; the first complete 3D cube that introduces those matrices is Program 4.1 in Module 4 (Section 4.5 is not assigned here).
- Sections 4.9 (Z-fighting) and 4.10 (other primitive options) have no numbered example programs. The book discusses glPolygonOffset, depth-buffer settings, and glDrawArrays primitive types as modifications you can apply to earlier programs. Section 4.9 is also assigned in Module 8.

## Compile and run

These programs use the official companion layout: Java sources and shaders live in a `code/` package (`package code;`), and textures or `.obj` models sit in the program folder (the working directory when you run). Shaders are loaded with paths such as `code/vertShader.glsl`.

You need **JDK 11**, **JOGL 2.4** (`jogl-all.jar`, `gluegen-rt.jar`, plus the native jars for your OS), and **JOML 1.10** (`joml-1.10.0.jar`) on the classpath. The textbook’s Appendix A (Windows) and Appendix B (macOS) cover installation. On Linux, put the jars in a `lib` directory (or any folder you prefer) and run the following from a program folder, for example `Program2_5`:

```bash
# Adjust these paths to where you keep the jars
CP="lib/jogl-all.jar:lib/jogl-all-natives-linux-amd64.jar:lib/gluegen-rt.jar:lib/gluegen-rt-natives-linux-amd64.jar:lib/joml-1.10.0.jar"

# Compile (from the program folder that contains the code/ directory)
javac -cp "$CP" code/*.java

# Run (also from that program folder, so shader and texture paths resolve)
java -cp "$CP:." \
  --add-exports java.base/java.lang=ALL-UNNAMED \
  --add-exports java.desktop/sun.awt=ALL-UNNAMED \
  --add-exports java.desktop/sun.java2d=ALL-UNNAMED \
  -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 \
  code.Code
```

On Windows, use `;` instead of `:` in the classpath, and the official `compile.bat` / `run.bat` in each folder assume the JOGL and JOML jars are already on your global `CLASSPATH` (as the book’s setup appendix describes):

```bat
javac code/Code.java
java --add-exports java.base/java.lang=ALL-UNNAMED --add-exports java.desktop/sun.awt=ALL-UNNAMED --add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 code.Code
```

Programs that open a window need a display; compiling does not.


This `textbook-examples` folder contains **15** files.
