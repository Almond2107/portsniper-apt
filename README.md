#  PortSniper APT Repository

Welcome to the official APT repository for **PortSniper** — a fast, flexible, and lightweight command-line port scanner written in Python.

With this repo, you can install PortSniper just like any other tool using `apt install`, without cloning or chmodding anything manually.


## 🛠️ What is PortSniper?

PortSniper is a modern port scanner for security researchers, developers, and sysadmins.

## Key Features:

    Scans a range of ports

    Shows only open ports (-o)

    Displays known services (-s)

    Grabs service banners for version info (-v)

    Super easy to use with flexible arguments

## Example

portsniper -t 192.168.1.1 -p 20-100 -s -v


---

## ⚙️ Installation (Debian/Ubuntu/Kali-based Systems)

> One-time setup to add the custom APT repository and install PortSniper:

### 1. Add the GPG Public Key

```bash
curl -fsSL https://almond2107.github.io/portsniper-apt/public.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/portsniper.gpg > /dev/null

## 2. Add the APT Source

'''bash
echo "deb [signed-by=/etc/apt/trusted.gpg.d/portsniper.gpg] https://almond2107.github.io/portsniper-apt/ stable main" | sudo tee /etc/apt/sources.list.d/portsniper.list

⚠️ For quick testing without signature verification, you can use this instead:

echo "deb [trusted=yes] https://almond2107.github.io/portsniper-apt/ stable main" | sudo tee /etc/apt/sources.list.d/portsniper.list


## 3. Update APT
'''bash
sudo apt update

### 4. Install PortSniper

'''bash
sudo apt install portsniper
