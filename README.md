# Bank DApp

เว็บ DApp สำหรับใช้งาน Smart Contract ระบบธนาคาร (Bank) บนเครือข่าย Sepolia Testnet

- **รหัสนักศึกษา:** 66085170
- **ชื่อ-สกุล:** ศิรินทร์ จันทร์ทนต์
- **เว็บไซต์:** https://sirinchanton.github.io/bank-dapp/
- **Contract Address (Sepolia):** `0xDB05de9bBbBcDD1d0776c2C3d85C9919764F8896`

## ฟังก์ชันของ Smart Contract

| ฟังก์ชัน | หน้าที่ |
|---|---|
| `deposit()` | ฝากเงินเข้าบัญชีของผู้เรียก (ต้องมากกว่า 0) |
| `withdraw(amount)` | ถอนเงินจากยอดของตัวเอง (ต้องไม่เกินยอดคงเหลือ) |
| `checkBlance()` | ตรวจสอบยอดคงเหลือของตัวเอง |

## สิ่งที่ต้องมี

1. เบราว์เซอร์ Chrome / Edge / Firefox
2. ส่วนขยาย [MetaMask](https://metamask.io/)
3. SepoliaETH (เหรียญทดสอบ ไม่มีมูลค่าจริง) ขอฟรีได้จาก Sepolia faucet

## วิธีใช้งานเว็บ

1. เปิดเว็บไซต์ แล้วกด **Connect MetaMask** (ถ้า MetaMask แจ้งเตือน ให้ตรวจว่าเป็นเว็บของตัวเอง แล้วเลือกดำเนินการต่อ)
2. ตรวจว่าเครือข่ายเป็น **Sepolia** ช่อง Contract address จะถูกเติมให้อัตโนมัติ (หรือกด **Connect Contract**)
3. กรอกจำนวน ETH เช่น `0.001`
4. กด **Deposit** เพื่อฝาก / **Withdraw** เพื่อถอน แล้วยืนยันธุรกรรมใน MetaMask
5. กด **Check Balance** เพื่อดูยอดคงเหลือในสัญญา

## วิธี Deploy Smart Contract (Remix)

1. เปิด [Remix IDE](https://remix.ethereum.org/) สร้างไฟล์ `Bank.sol` แล้ววางโค้ดจากไฟล์ `Bank.sol` ใน repo นี้
2. แท็บ **Solidity Compiler** เลือกเวอร์ชัน 0.8.x แล้วกด Compile
3. แท็บ **Deploy & Run** ตั้ง Environment เป็น *Browser Extension / Injected Provider – MetaMask* และเลือกเครือข่าย Sepolia
4. กด **Deploy** แล้วยืนยันใน MetaMask
5. คัดลอก address ของ contract ที่ได้ไปใส่ในตัวแปร `CONTRACT_ADDRESS` ในไฟล์ `index.html`

## วิธีนำเว็บขึ้น GitHub Pages

1. สร้าง repository (Public) แล้วอัปโหลด `index.html`
2. ไปที่ **Settings → Pages**
3. Source: *Deploy from a branch* เลือก branch `main` โฟลเดอร์ `/ (root)` แล้วกด Save
4. รอประมาณ 1-2 นาที URL จะเป็น `https://<username>.github.io/<repo>/`

## เทคโนโลยีที่ใช้

- Solidity ^0.8.0
- HTML / CSS / JavaScript
- [ethers.js](https://docs.ethers.org/) v6 (โหลดผ่าน CDN)
- MetaMask + Sepolia Testnet

## หมายเหตุ

- ชื่อฟังก์ชัน `checkBlance` สะกดตามโจทย์ที่กำหนด
- ใช้เพื่อการศึกษาบนเครือข่ายทดสอบเท่านั้น ห้ามนำไปใช้กับเงินจริง
- ห้ามนำ private key หรือ seed phrase มาใส่ในไฟล์ใด ๆ ใน repo นี้
