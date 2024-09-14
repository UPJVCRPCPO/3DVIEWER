# Depth Map 3D Effect with Normal Maps and Advanced Lighting Controls

This project creates an interactive 3D effect using both depth maps and normal maps, with advanced lighting controls. It's built using Three.js and vanilla JavaScript, demonstrating sophisticated real-time graphics techniques in the web browser.

## Features

- Load custom images, depth maps, and normal maps
- Real-time 3D parallax effect based on mouse movement
- Utilizes both depth maps for displacement and normal maps for lighting detail
- Two customizable point lights with advanced controls:
  - Enable/disable lights
  - Adjust color, intensity, and position
  - Flickering and pulsing effects
- Resizable interface with draggable controls
- Background color customization

## Technical Description

This project leverages several advanced computer graphics techniques:

1. **Depth Map Displacement**: The vertex shader uses the depth map to displace the geometry, creating the 3D effect. The displacement is also used for parallax, making the image respond to mouse movement.

2. **Normal Map Integration**: Normal maps are used to add fine surface detail without increasing geometric complexity. This enhances the lighting effects and surface appearance.

3. **Custom Shaders**: The project uses custom GLSL shaders for both vertex and fragment processing:
   - The vertex shader handles displacement and parallax effects.
   - The fragment shader manages lighting calculations, including the use of normal maps.

4. **Dynamic Lighting**: Two point lights are simulated in the fragment shader, with real-time updates to their properties (position, color, intensity).

5. **Advanced Lighting Effects**: The lights support dynamic effects like flickering and pulsing, simulated through JavaScript and passed to the shader uniforms.

6. **Texture Blending**: The final output blends the original image with lighting calculations, preserving transparency where present in the original image.

7. **Responsive Design**: The interface uses flexbox for layout and includes a resizable control panel, demonstrating responsive web design principles alongside advanced graphics.

## Setup

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/depth-map-3d-effect.git
   ```

2. Open the `index.html` file in a modern web browser.

3. Alternatively, you can use a local server to run the project. For example, with Python:
   ```
   python -m http.server
   ```
   Then open `http://localhost:8000` in your browser.

## Usage

1. Click the "Choose File" buttons to select your image, depth map, and normal map.
2. Click the "Load Images" button to apply the selected images.
3. Use the controls on the left side to adjust lighting and effects:
   - Toggle lights on/off
   - Change light colors
   - Adjust light intensity and position
   - Enable flickering and pulsing effects
4. Move your mouse over the image to see the 3D parallax effect.
5. Drag the resize bar to adjust the size of the control panel.

## Requirements

- A modern web browser with WebGL support
- Three.js library (included via CDN in the HTML file)

## Customization

You can easily customize this project by modifying the HTML, CSS, and JavaScript code:

- Add new lighting effects in the `updateLightUniforms` function
- Modify the vertex and fragment shaders for different visual effects
- Adjust the UI layout and styling in the CSS section

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check [issues page](https://github.com/yourusername/depth-map-3d-effect/issues) if you want to contribute.

## Author

https://github.com/UPJVCRPCPO/

## Acknowledgments

- [Three.js](https://threejs.org/) for 3D rendering
- Inspiration from various depth map and normal map techniques in real-time graphics
