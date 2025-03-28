Below is an example README.md you can use for your project:

⸻

Fourier Wave Creator

An interactive web tool that lets you create custom waveforms—either by drawing or by loading pre‐defined template signals—and then view their Fourier reconstruction and power spectral density (PSD). It is inspired by code from: https://github.com/Jezzamonn/fourier

Overview

The Fourier Wave Creator is built with p5.js and allows you to:
	•	Draw a custom waveform on a dedicated panel.
	•	Load a variety of template waves (square, white noise, pink noise, triangle, sine, multi-sine, etc.).
	•	View a Fourier reconstruction of your waveform, where the composite signal is scaled to a vertical range of –1 to 1.
	•	Inspect the frequency content of your waveform with an interactive PSD panel.

This tool is ideal for exploring how different waveforms decompose into sine components and for learning about Fourier analysis in a visual and interactive way.

Features
	•	Custom Drawing Panel:
Draw your own waveforms with your mouse. The drawing area is clipped to a defined plot region with clearly labeled axes.
	•	Fourier Reconstruction Panel:
The DFT is calculated from your drawn (or template) waveform. The reconstruction is displayed by summing the individual sine components and then scaling the output to a –1 to 1 vertical range.
	•	PSD Panel:
View the power spectrum of your waveform, which shows the relative amplitude of the different frequency bins (e.g., from 0 to 30 Hz).
	•	Template Waves:
Load pre-defined signals such as a 10 Hz sine wave, square wave, triangle wave, white noise, pink noise, and more with a single click.

How It Works
	•	Drawing and Input:
The tool converts mouse coordinates to domain coordinates based on the effective plot region. This ensures that your drawn wave appears exactly where you click.
	•	Fourier Transform:
Once you finish drawing (or load a template), the script resamples the composite waveform and computes its discrete Fourier transform (DFT). The reconstruction is then built by summing a configurable number of sine components.
	•	Visualization:
All panels (custom drawing, reconstruction, and PSD) use consistent margins, padding, and clipping to ensure that waveforms and axes are clearly displayed.

Installation and Usage
	1.	Clone or Download:
Clone this repository or download the HTML file (e.g., fourier-demo_v7.html).
	2.	Open in a Browser:
Simply open the HTML file in any modern web browser (Chrome, Firefox, Edge, etc.). No additional server setup is required.
	3.	Drawing & Templates:
	•	To draw your own waveform, click and drag in the Custom Drawing panel.
	•	Alternatively, click one of the template buttons (e.g., “10 Hz Sine”) to load a pre-defined waveform.
	•	Use the slider to adjust the number of sine components used in the reconstruction.
	4.	View Analysis:
	•	The Fourier Reconstruction panel will show the sum of individual sine components along with the final reconstructed signal (scaled to –1 to 1).
	•	The PSD panel displays the power distribution across frequency bins.

Customization
	•	Modifying Samples and Duration:
The current configuration uses 1000 samples over 1 second. You can adjust the T (duration) and N (sample count) constants in the script if needed.
	•	Changing Margins and Padding:
The margins and internal plot padding are defined as constants at the top of the script. Adjust these values to fit your desired layout.

Dependencies
	•	p5.js v1.4.0

License

This project is open source and available under the MIT License.

⸻

Feel free to customize the content as needed. Enjoy exploring Fourier analysis interactively!