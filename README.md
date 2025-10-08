# ASCII-Image-Converter
A script that takes an image and visualises it as a text-based ASCII art in a browser.

## Preview
![Preview Image](preview.png)

## How to Use
1. Upload an image file in the same folder as index.html
2. Replace the value to your filename at `const imageFile = 'yourImageFile.png';`
3. Run a local server - Opening the HTML file does not work <br />
   For example:
   ```bash
   python -m http.server
   ```

## How It Works
1. Each pixel's RGB value is converted into a greyscale value
2. The greyscale intensity is used to map brightness to ASCII density
3. Based on brightness, a character from the ASCII set is selected:
   ```javascript
   "@$#Y!=+~- "
   ```
4. The characters are arranged in order to form the image's shape

## Customization
Tune how the ASCII image looks by:
- Adjusting the sampling rate:
  ```javascript
  const step = 3;
  ```
- Modifying the contrast by changing ASCII character set to darker/lighter characters:
  ```javascript
  const ascii = "@$#Y!=+~- ";
  ```
- Changing the font family or size in the `<h4>` style:
  ```html
  <h4 style="font-family: consolas; font-size: 6px; letter-spacing: 0px;"></h4>
  ```
  
