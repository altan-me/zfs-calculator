# ZFS Storage Calculator 🧮💾

**Calculate your ZFS pool’s usable & effective capacity with ease!**  
A lightweight, responsive web app to help you plan ZFS storage pools, compare redundancy levels, and estimate real-world usable space after ZFS overhead. Built with Tailwind CSS, Font Awesome, and vanilla JavaScript.

---

## 🚀 Features

- 🎛️ **Dynamic Inputs**
  - Number of disks
  - Disk size (TB / GB toggle)
  - Redundancy level (None, RAIDZ1/2/3, Mirror)
- 📊 **Instant Results**
  - Usable Capacity (pre-overhead)
  - Effective Capacity (after redundancy & ZFS overhead)
  - Calculated ZFS Overhead (%)
  - Mirror pair count & fault-tolerance explanation
- ⚙️ **Accurate Overhead Model**
  - Partition labels, alignment, reserved partitions
  - VDEV labels, boot blocks, metaslab loss, slop space
- 🌐 **Responsive & Accessible**
  - Mobile-first layout
  - Keyboard-accessible controls & ARIA labels
- 🎨 **Modern UI**
  - Dark theme with TikTok-inspired gradient accents
  - Tailwind CSS utility classes
  - Font Awesome icons

---

## 🛠️ Installation & Usage

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-username/zfs-storage-calculator.git
   cd zfs-storage-calculator
   ```
2. **Open `index.html` in your favorite browser**
   ```bash
   open index.html
   ```
3. **Start calculating!**
   - Enter disk count & size
   - Select TB or GB
   - Choose your redundancy level
   - View results instantly

_No build tools or servers required – just static HTML/CSS/JS!_

---

## 📚 How It Works

1. **Raw Capacity** = number_of_disks × disk_size
2. **ZFS Overhead**
   - Partition & alignment labels
   - Reserved partitions & boot blocks
   - Metaslab allocation loss (0.5% estimate)
   - Slop space (1/32 of pool)
3. **Usable Capacity** (pre-overhead) = usable_disks × disk_size
4. **Effective Capacity** = (usable_capacity × (1 − total_overhead%))

All calculations assume 1 GB = 10⁹ bytes, 1 TB = 10¹² bytes.

---

## ✍️ Contributing

1. Fork it (🔀 “Fork” button at the top right)
2. Create your feature branch:
   ```bash
   git checkout -b feature/my-awesome-calc
   ```
3. Commit your changes
4. Push to the branch
5. Open a Pull Request ✨

Please follow the existing code style and include descriptive commit messages.

---

Made with ❤️ by [altan.me](https://zfs-calculator.com)  
Enjoy calculating! 🎉
