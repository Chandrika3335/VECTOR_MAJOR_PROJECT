🏦 ATM Banking System – Embedded + PC Backend Integration

This project simulates a complete ATM–Banking architecture, integrating:

LPC2148 Embedded Firmware (ATM Frontend)

Linux-based ATM Backend (PC Application in C)

Central Banking Application with file-based database

It is a modular, scalable, real-time simulation of how a real ATM communicates with a bank server using UART and secure command responses.


PROJECT STRUCTURE:

ATM-BANK-PROJECT/
├── ATM/          # ATM Microcontroller Frontend (LPC2148 MCU Firmware)
├── BANK/         # Central Banking Application (PC Backend in C)
├── FIRMWARE/     # Compiled HEX/BIN files for flashing LPC2148
└── README/       # Documentation (optional)

🧠 Project Explanation
🔐 ATM/ – ATM Frontend (LPC2148 MCU Firmware)

Implements complete ATM user interface:
RFID Card Reading
PIN Authentication
Keypad Input
LCD Display
UART Communication with bank server
ATM Operations:
Balance Inquiry
Deposit
Withdrawal
Transfer
PIN Change
Mini Statement

✔ Written entirely in Embedded C
✔ Runs on LPC2148 ARM7TDMI controller
✔ Communicates with PC backend via UART0/UART1

🧪 Build & Run (MCU Side)

Open Keil uVision / VS Code (with embedded extensions)

Load source code from /ATM/

Build → Generate HEX

Flash using Flash Magic

Connect LPC2148 UART to PC

🛠️ BANK/ – Central Banking Application (PC Backend)

This is the brain of the system, containing:

Account Creation

Deposit

Withdrawal

Balance Inquiry

Transfer

PIN Change

Transaction Log Storage

File-based Database for All Accounts

✔ Written in pure C (No SQL needed)
✔ Interacts with MCU in real time
✔ Stores persistent data in .txt or structured files

🧪 Build and Run (Linux PC Side)
cd BANK
make
./atm
The backend waits for requests from MCU through UART and processes transactions instantly.

How to Run:

1. CLone the respository using the below link:
git clone https://github.com/Chandrika3335/VECTOR_MAJOR_PROJECT>.git
cd <VECTOR_MAJOR_PROJECT>

2. Install Build Tools
sudo apt update
sudo apt install build-essential

3.Compile and Run ATM Backend

cd ATM make -f makeATM ./bank

Compile and Run Bank Application

cd ../BANK make -f makeBANK ./bank

4.Load Firmware to LPC2148 (Optional)

Open Keil or Flash Magic
Load hex/bin files from FRIMWARE/
Flash to LPC2148
Connect serial to ATM backend


