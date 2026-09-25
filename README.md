# EMF Induction Lab — web app

Browser front end for the dual-coil Faraday / Lenz teaching kit
(Adafruit Feather ESP32-S2 Reverse TFT running `EMF_Teaching_Kit_Dual_Coil_USB` firmware).

**Open the app:** `https://<your-github-username>.github.io/<repository-name>/`

## Using it in the lab

1. Open the link above in **Chrome** or **Edge** (Firefox and Safari do not support USB serial).
2. Plug the kit into the computer with a USB-C **data** cable.
3. Click **Connect kit** and choose *Feather ESP32-S2 Reverse TFT (COMx)*.
4. Tick **Coil 2 connected** only when a second coil is plugged into A2–A3.

No installation is needed. The kit's data goes from the USB cable straight into the browser;
nothing is sent to this website. Once the page has loaded, the lab works without internet.
**Demo mode** runs a simulated kit for practice without hardware.

Link to this page directly. Embedding it in Google Sites, Moodle or another page's frame
blocks USB access.

## Analysis notebook

`analysis/EMF_Lab_Analysis.ipynb` analyses the CSV files the app downloads (waveform
frequency, amplitude and phase; ε₀ versus ω fit giving N·B·A). It runs as-is on the simulated
files in `analysis/sample_data/`. In Google Colab, upload your own CSV files and change the
file names in the first code cell.

## Updating the site

Replace `index.html` with the new `EMF_Lab.html` (renamed to `index.html`): on GitHub,
**Add file → Upload files**, drop the file in and **Commit changes**. The site updates within
about a minute; students may need **Ctrl+F5** once.
