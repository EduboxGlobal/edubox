# EduBox: Open-Source Offline Education Platform

## Mission
Bring quality education to the 258.4 million children worldwide who lack access to schools and internet, using low-cost, sustainable technology.

## What is EduBox?
EduBox is an affordable education server (starting at $200) that provides:
- Complete offline access to Khan Academy, Wikipedia, and educational content
- Creates its own WiFi network - no internet required
- Serves 30-50 students simultaneously (200-300 daily in shifts)
- Works with any WiFi-enabled device (phones, tablets, computers)
- Includes everything needed: server, WiFi router, and setup

### Package Options
- **Basic Education Server ($200)**: Serves small schools (up to 200 students)
  - Raspberry Pi-based server with built-in WiFi
  - 30-50 concurrent users
  
- **Standard Education Server ($350)**: Serves medium schools (200-500 students) 
  - More powerful hardware, enterprise WiFi
  - 75-100 concurrent users
  
- **Complete Classroom ($500-750)**: Includes server + basic tablets
  - Everything in Standard package
  - 5-10 shared tablets for schools without devices

## Key Features
- **Affordable**: 90% cheaper than traditional computer labs
- **Self-Contained**: Creates its own WiFi network - no internet needed
- **Realistic Capacity**: 30-50 concurrent users, 200-300 daily users
- **Complete Package**: Includes server, WiFi router, and all setup
- **Content**: 50GB+ of curated educational materials in 40+ languages
- **Power Efficient**: 15-25W consumption, battery backup options
- **Offline Updates**: Content updated via USB when internet is available

## Hardware Components

### Basic Package (~$200)
- Raspberry Pi 4 (8GB RAM): $75
- 128GB high-speed SD card: $20
- Quality WiFi router/access point: $40
- Power supply with backup: $30
- Cooling & weatherproof case: $20
- Cables and accessories: $15

### Standard Package (~$350)
- Mini PC (Intel NUC or similar): $200
- 256GB SSD storage: $40
- Enterprise WiFi access point: $60
- UPS battery backup: $30
- Professional enclosure: $20

## Software Stack
- **OS**: Raspberry Pi OS Lite
- **Content Server**: KA Lite (offline Khan Academy)
- **Additional Content**: RACHEL, Kiwix (offline Wikipedia)
- **Management**: Custom EduBox interface
- **Languages**: Python, JavaScript, HTML/CSS

## Impact Goals
- Reach 1 million children in first 2 years
- Partner with 1,000 schools in developing countries
- Train 10,000 teachers
- Support 40+ languages
- Create local job opportunities for maintenance

## 🚀 Quick Start

### 🐳 Using Docker (Recommended)

#### Docker Compose (Easiest)
```bash
# Clone the repository
git clone https://github.com/yinzara/edubox.git
cd edubox

# Build and start EduBox
docker-compose up -d

# Access the portal
open http://localhost
```

#### Docker Run
```bash
# Build the image
docker build -t edubox:latest .

# Run the container
docker run -d \
  --name edubox \
  -p 80:80 \
  -v $(pwd)/content:/opt/edubox/content \
  -v $(pwd)/logs:/opt/edubox/logs \
  edubox:latest
```

#### Adding Educational Content
1. Download ZIM files from [Kiwix Library](https://download.kiwix.org/zim/)
2. Place files in the `content/` directory
3. Restart the container: `docker restart edubox`
4. Access Wikipedia directly at http://localhost:8080

Recommended starter content:
- [Simple English Wikipedia](https://download.kiwix.org/zim/wikipedia/) (~200MB)
- [Khan Academy](https://download.kiwix.org/zim/khan-academy-videos/)
- [Project Gutenberg Books](https://download.kiwix.org/zim/gutenberg/)

### 🔧 Manual Installation (Raspberry Pi)
```bash
# Download and run the installer
curl -fsSL https://raw.githubusercontent.com/yinzara/edubox/main/install.sh | bash
```

### 🛠️ Troubleshooting

**Port 80 not accessible?**
If you built the container before June 1, 2025, run:
```bash
./fix-nginx.sh
```
Then rebuild for a permanent fix:
```bash
docker-compose down && docker-compose build --no-cache && docker-compose up -d
```

### 🌐 Access Points

- **Main Portal**: http://localhost/
- **Wikipedia/Kiwix**: http://localhost/wikipedia/ (or http://localhost:8080/)
- **Content Browser**: http://localhost/content/

**Note**: Wikipedia is accessible through both the reverse proxy at `/wikipedia/` and directly on port 8080.

## Getting Started
1. [Build Your Own EduBox](docs/build-guide.md)
2. [Deploy in Your Community](docs/deployment-guide.md)
3. [Contribute to Development](docs/contributing.md)
4. [Partner With Us](docs/partnerships.md)

## Current Partners
- Foundation for Learning Equality
- Raspberry Pi Foundation
- World Possible (RACHEL)
- Khan Academy
- Local NGOs in 15+ countries

## Open Source
All code, documentation, and content curation lists are available under MIT License.

---
*"Education is the most powerful weapon which you can use to change the world." - Nelson Mandela*