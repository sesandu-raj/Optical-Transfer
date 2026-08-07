# Optical Transfer

Transfer data between devices using visible light and animated QR codes—without relying on a direct network connection between the devices.

## Overview

**Optical Transfer** is a browser-based experiment that encodes data into a sequence of QR-code frames. One device displays the frames, while another device uses its camera to read them and reconstruct the transferred data.

This approach can be useful when conventional transfer methods are unavailable or undesirable, such as when devices are isolated from one another or wireless connectivity is turned off.

## Features

- Screen-to-camera data transfer.
- Browser-based interface with no native application required.
- QR-code frame sequence for transmitting data optically.
- Works across compatible desktop and mobile browsers.
- Useful as an educational demonstration of optical communication and machine-readable visual data.

## How It Works

1. The sender converts the selected data into QR-code frames.
2. The sender displays the frames sequentially on the screen.
3. The receiver points its camera at the sender's display.
4. The receiver decodes the captured frames and rebuilds the transmitted data.

The transfer speed and reliability depend on screen brightness, camera quality, focus, lighting, distance, and the size of each encoded frame.

## Getting Started

### Requirements

- A modern web browser with JavaScript enabled.
- A display device for the sender.
- A camera-equipped device for the receiver.
- Adequate lighting and a clear view of the sender's screen.

### Run Locally

Clone the repository:

```bash
git clone https://github.com/sesandu-raj/Optical-Transfer.git
cd Optical-Transfer
```

Open `optical-transfer.html` in a modern browser. Depending on the browser's security restrictions and the features used by the page, serving the file through a local HTTP server may work more reliably:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000/optical-transfer.html](http://localhost:8000/optical-transfer.html).

Use one device as the sender and a second device as the receiver. Keep the QR-code area fully visible and adjust the distance until the receiver can decode the frames consistently.

## Usage Tips

- Increase screen brightness on the sending device.
- Avoid glare, reflections, and strong backlighting.
- Keep the camera steady and focused on the QR code.
- Use a larger display or move the devices closer when decoding is unreliable.
- Avoid changing tabs or locking the sender's screen during a transfer.

## Limitations

Optical transfer is slower and more sensitive to environmental conditions than network-based transfer. Missed, blurred, partially hidden, or incorrectly ordered frames may prevent successful reconstruction, depending on the implementation and payload format.

Do not use the project to transfer sensitive information unless you have independently reviewed the implementation and understand how the data is encoded, displayed, decoded, and handled by the browser.

## Project Structure

```text
.
├── optical-transfer.html   # Browser interface and transfer logic
└── README.md               # Project documentation
```

## Contributing

Contributions are welcome. To propose a change:

1. Fork the repository.
2. Create a feature branch.
3. Make and test your changes in a modern browser.
4. Open a pull request with a clear description of the change.

## License

No license file is currently documented in this README. Add a `LICENSE` file to the repository if you intend to publish the project under a specific open-source license.

## Author

Created by [sesandu-raj](https://github.com/sesandu-raj).
