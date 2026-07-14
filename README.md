# Hi, I'm Ramisa Fariha Mridha

Machine learning researcher with an MSc in Biomedical Engineering
(University of Oulu, Finland), specialising in deep learning, computer
vision, and multimodal data analysis. My research at the Center for
Machine Vision and Signal Analysis (CMVS) spans transformer-based
architectures for multi-sequence image segmentation, affective
computing, and applying deep learning to biosignal and image data.

I'm currently seeking PhD and research positions in medical image
analysis, computational imaging, and applied deep learning.

- **Email:** rf.mridha.13@gmail.com
- **ORCID:** [0009-0001-5194-586X](https://orcid.org/0009-0001-5194-586X)
- **LinkedIn:** [ramisa-fariha-mridha](https://www.linkedin.com/in/ramisa-fariha-mridha-6a25a01ab)
- **GitHub:** [@Ramisa13](https://github.com/Ramisa13)

## Research

First author of a manuscript under review at *Information Fusion*
(Elsevier) benchmarking deep learning architectures for myocardial
infarction segmentation on cardiac MRI. My master's thesis (assessed 5/5,
Excellent) developed a novel deep learning method for multi-sequence
cardiac MRI segmentation — full details are being held back until the
related journal submission is out.

## Projects

Deep learning coursework and independent projects, all with full code,
documentation, and (where applicable) verified results:

- **[Transfer Learning for Diabetic Retinopathy Detection](https://github.com/Ramisa13/dr-transfer-learning)** — fine-tuning, two-stage training, self-attention, ensembling, and Grad-CAM explainability on the DeepDRiD dataset.
- **[FaceForge: DCGAN Transfer Learning](https://github.com/Ramisa13/faceforge-dcgan)** — a DCGAN pretrained on CelebA and fine-tuned to generate AnimeFace-style images.
- **[ThreadNet: CNN for Fashion-MNIST](https://github.com/Ramisa13/threadnet-fashion-cnn)** — a LeNet-style convolutional network with a custom stratified-split dataset class.
- **[PureGrad: From-Scratch Neural Network](https://github.com/Ramisa13/puregrad-fashion-mnist)** — a fully NumPy feedforward network with hand-derived backpropagation, verified against finite-difference gradient checks.
- **[AdCurve: Linear Regression from Scratch](https://github.com/Ramisa13/adcurve-linear-regression)** — multivariate linear regression built without `nn.Linear`, trained with gradient descent.

## About this repository

This repo is the source for my personal site at
[ramisa13.github.io](https://ramisa13.github.io) — a single-page HTML,
CSS, and vanilla JS build (no framework, no build step) covering my
background, education, experience, research, projects, skills, awards,
and contact details, structured so a recruiter or hiring committee can
get a complete picture in one pass.

```
ramisa-portfolio/
├── index.html      all page content and section markup
├── style.css        design system: colors, type, layout, the scan-line hero motif
├── script.js          sets the footer year
└── assets/
    ├── CV.pdf          downloadable CV
    └── profile.jpg      headshot (add your own — see below)
```

### Deploying changes

The site is served directly by GitHub Pages from this repo. To make
changes: edit the files, then commit and push to `main` —

```bash
git add .
git commit -m "Update site"
git push
```

GitHub Pages picks up the change automatically within a minute or two.

### Still to add

- `assets/profile.jpg` — a headshot, square-ish crop recommended since
  it's displayed in a circle. The site works fine without it; the frame
  just stays empty until the file is added.

### Local preview

No build tooling required:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```
