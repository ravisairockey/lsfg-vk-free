
# 🖥️ LSFG-VK: Lossless Scaling Frame Generator for Vulkan
*A Complete Setup Guide for CachyOS & Arch Linux Users*

---

## 📌 Introduction

This repository contains a guide for setting up `lsfg-vk`, the Vulkan-based Lossless Scaling Frame Generator, tailored for **CachyOS** and **Arch Linux** users. This utility enhances your gaming and graphical experience by providing high-quality upscaling with minimal performance loss.

Whether you're gaming at a lower resolution or seeking a more efficient method of scaling without compromising on image clarity, **LSFG-VK** is your solution.

---

## 🎯 Features

- 🔍 Pixel-perfect integer scaling
- 🖼️ No blurry interpolation like bilinear or bicubic
- 🚀 Vulkan-based performance
- 🛠️ GUI-based configuration
- 🐧 100% Linux-native

---

## 🛠️ Step-by-Step Installation

### ✅ Step 1: Install Required Tools

Make sure you have [`paru`](https://wiki.archlinux.org/title/Paru) (an AUR helper) installed.

Then, install Lossless Scaling:

```bash
paru --needed lossless-scaling
```

If you don't have `paru`, install it with:

```bash
sudo pacman -S paru
```

### 📥 Step 2: Clone and Install LSFG-VK

Clone the `lsfg-vk` repo from GitHub and compile it:

```bash
git clone https://github.com/lossless-scaling/lsfg-vk.git
cd lsfg-vk
make
sudo make install
```

> ⚠️ Ensure dependencies like `vulkan-headers`, `glslang`, and build tools are installed.

---

## 🧰 Configuration

Once installed, open the LSFG-VK configuration window:

```bash
lsfg-vk --config
```

This will open the GUI to customize scaling settings.

![🖼️ Configuration Screenshot](Screenshot%20From%202025-08-06%2011-52-59.png)

Refer to the above screenshot to match your settings.

---

## 🖼️ SVG Explanation of Workflow

Here's a basic visual SVG representation of the process pipeline:

```svg
<svg width="600" height="300" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="40" width="150" height="50" fill="#4CAF50" rx="10"/>
  <text x="95" y="70" font-size="14" text-anchor="middle" fill="white">Install Paru</text>
  
  <line x1="170" y1="65" x2="200" y2="65" stroke="black" stroke-width="2" marker-end="url(#arrow)"/>
  
  <rect x="200" y="40" width="150" height="50" fill="#2196F3" rx="10"/>
  <text x="275" y="70" font-size="14" text-anchor="middle" fill="white">Install LSFG-VK</text>
  
  <line x1="350" y1="65" x2="380" y2="65" stroke="black" stroke-width="2" marker-end="url(#arrow)"/>
  
  <rect x="380" y="40" width="180" height="50" fill="#FF9800" rx="10"/>
  <text x="470" y="70" font-size="14" text-anchor="middle" fill="white">Open Config GUI</text>

  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="10" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="black" />
    </marker>
  </defs>
</svg>
```

You can render this using any markdown SVG plugin or by embedding it into your GitHub Pages.

---

## 🧪 Tips & Troubleshooting

- ❌ GUI not launching?
  ```bash
  LSFG_VK_DEBUG=1 lsfg-vk --config
  ```
- 🖼️ Vulkan not working? Make sure your GPU supports Vulkan and proper drivers are installed.
- 🧼 Clean builds by running `make clean` before recompiling.

---

## 📜 License & Credits

- 🔗 You can also install it directly via Steam:
- 👉 [Lossless Scaling on Steam](https://store.steampowered.com/app/993090/Lossless_Scaling/)
- 📂 Project: [LSFG-VK GitHub](https://github.com/lossless-scaling/lsfg-vk)
- 🤝 Community: Arch Wiki, CachyOS Users
- 🧑‍💻 Author: You

---

*Generated on August 06, 2025 — README designed for maximum clarity and appeal.*



---

## 📂 Additional Setup for Steam Users

To integrate **Lossless Scaling** with your Steam games:

📁 **Step 4: Move the `Lossless Scaling` Folder**

Place the `Lossless Scaling` folder inside your Steam installation directory:

```bash
mv ~/Downloads/Lossless\ Scaling ~/.local/share/Steam/steamapps/common/
```

> 📝 Make sure the folder is named exactly `Lossless Scaling`.

After placing it:
- You can configure it as a non-Steam game or link it with launch options.
- Great for Proton games or native titles requiring pixel-perfect scaling.
