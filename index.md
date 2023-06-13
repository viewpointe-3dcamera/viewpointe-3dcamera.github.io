Our goal is to build a camera that can capture and process surgical microscope images to be directly visualized in 3D.
### Problem
Alcon’s existing Ngenuity system seeks to capture stereo images from an ophthalmic surgical microscope, process the two images on a host computer, and provide a high definition, 3D image that can be displayed on a supporting display. This provides the surgeon with a higher resolution, ergonomic working environment. The use of a separate computer and a USB communication protocol, however, has introduced significant delays and image quality issues into the system, which Alcon seeks to correct.

### Solution
To reduce latency, we attempt to remove the need for intensive graphics processing on the host computer, by utilizing an FPGA. The two image inputs will be processed into a display form suitable for a 3D monitor. The user will have the ability to choose between visual formats, including side-by-side and top-bottom, presented to the monitor in HDMI format. All processing will happen on the camera itself, without requiring an external computer.

