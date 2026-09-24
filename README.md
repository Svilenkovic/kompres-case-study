<a href="https://compress.svilenkovic.rs/"><img src="media/cover.jpg" alt="Kompres, home page on a laptop and a phone" width="100%"></a>

# Kompres

Browser tool that compresses a batch of JPEG, PNG, WebP and AVIF images on the device, with separate modes for email and for websites.

**[compress.svilenkovic.rs](https://compress.svilenkovic.rs/)** · [App page](https://svilenkovic.com/en/aplikacija-kompres) · [Srpski](README.sr.md)

> [!NOTE]
> My own product. The source code is private. This page describes what it does and how it is built.

<table>
  <tr><td><b>Client</b></td><td>Own product</td></tr>
  <tr><td><b>Industry</b></td><td>Image compression tool</td></tr>
  <tr><td><b>Location</b></td><td>Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Web app (PWA)</td></tr>
  <tr><td><b>My role</b></td><td>Design, development and hosting</td></tr>
  <tr><td><b>Stack</b></td><td>TypeScript, Vite, Web Workers, WebAssembly, PWA</td></tr>
</table>

## About the project

Kompres is my own tool for making images smaller before they go into an email or onto a website. You drop in or paste a batch, pick a mode, and download the results one by one, as a ZIP or straight into a folder. The server only delivers the app; the images never leave the device.

Each image is encoded several ways and the smallest result wins. MozJPEG, WebP, AVIF and OxiPNG compete depending on the mode and on whether the image has transparency, and if nothing beats the original, the original stays. The email mode sticks to JPEG and PNG, which mail clients show inside the message. A separate button steps down size and quality until a whole batch fits under the 25 MB limit of one Gmail message.

## What I built

- WebAssembly codecs running in Web Workers, with the number of workers set from the device's cores and memory so the interface stays responsive
- Four modes (email, smart, lossless and aggressive) with quality and maximum dimension controls
- Input in JPEG, PNG, WebP, AVIF, GIF and BMP, by drag and drop or paste
- A before and after slider for comparing each result with the original
- Download one by one, as a ZIP, or into a chosen folder where the browser allows it
- An installable PWA that works offline and appears in the Android share menu for images

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 100 | 96 | 100 | 100 |
| Desktop | 100 | 96 | 100 | 100 |

Lighthouse, lab test of the live site, September 2026.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Kompres, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Kompres, home page on a phone"></td>
  </tr>
</table>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
