
# React Native Nyx Printer - Usage Examples

This document provides examples for using the Nyx Printer methods in a React Native project, including `printText`, `printBarcode`, `printQrCode`, `printBitmap`, and `paperOut`. The `printText` method accepts optional formatting.

## Installation

Install the `react-native-nyx-printer` module with npm:

```bash
npm install react-native-nyx-printer
```

## Usage Examples

### 1. `multiply(a, b)`
Multiplies two numbers asynchronously.

```javascript
import { multiply } from 'react-native-nyx-printer';

multiply(5, 10).then(result => {
  console.log("Result:", result); // Output: 50
});
```

### 2. `printText(text, textFormat)`
Prints text with an optional `textFormat` object for custom styling.

- **Acceptable `textFormat` options:**
  - `fontSize` (number): Text font size.
  - `bold` (boolean): Bold text if `true`.
  - `alignment` (string): Options are `"left"`, `"center"`, `"right"`.
  - `underline` (boolean): Underlines text if `true`.

**Example:**

```javascript
import { printText } from 'react-native-nyx-printer';

const textStyle = { fontSize: 14, bold: true, alignment: "center", underline: false };
printText("Hello, World!", textStyle).then(response => {
  console.log("Text printed:", response);
});
```

### 3. `printBarcode(content, width, height)`
Prints a barcode with specified width and height.

```javascript
import { printBarcode } from 'react-native-nyx-printer';

printBarcode("1234567890", 100, 50).then(response => {
  console.log("Barcode printed:", response);
});
```

### 4. `printQrCode(content, width, height)`
Prints a QR code with specified width and height.

```javascript
import { printQrCode } from 'react-native-nyx-printer';

printQrCode("https://example.com", 100, 100).then(response => {
  console.log("QR Code printed:", response);
});
```

### 5. `printBitmap(inputBytes)`
Prints a bitmap from a byte array.

```javascript
import { printBitmap } from 'react-native-nyx-printer';

const bitmapData = [/* array of byte values */];
printBitmap(bitmapData).then(response => {
  console.log("Bitmap printed:", response);
});
```

### 6. `paperOut()`
Checks if the paper is out.

```javascript
import { paperOut } from 'react-native-nyx-printer';

paperOut().then(response => {
  console.log(response === 1 ? "Paper is out" : "Paper is available");
});
```

---

These examples cover essential usage patterns.


## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT

## Credits

[yyzz2333/NyxPrinterClient](https://github.com/yyzz2333/NyxPrinterClient)

[Aladdin16659/NyxPrinter](https://github.com/Aladdin16659/NyxPrinter)

---
