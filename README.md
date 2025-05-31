
# 🔧 Power Rail Debug Toolkit (For TPM / Hardware PM)

本筆記包含 BIOS、EC、Power Rail、VRM 等平台啟動與 Debug 知識，提供 TPM / Debug PM 快速參考與實戰對照。

---

## 🚀 Notebook Power Rail 啟動時序

1. AC / Battery 插入 → EC 上電  
2. EC 啟動 Standby Rail（3.3V / 5V）  
3. Power IC (VRM) 開始輸出電壓  
4. CPU 開始執行 BIOS  
5. BIOS 檢查各 Rail 狀態  
6. BIOS 設定電壓參數  
7. 進入 Bootloader

---

## 🆚 Notebook vs Server Power Rail 對比表

| 項目 | Notebook | Server |
|------|----------|--------|
| 供電來源 | Battery / Adapter | Redundant PSU |
| 控制模組 | EC + PMIC | BMC + VRM |
| 電壓種類 | 3.3V, 5V, 12V, VCORE | 加上 VPP, VDDQ 等 |
| Power Good 控制 | EC / PMIC | VRM / BMC |
| 熱插拔 | ❌ | ✅ |
| Power Rail 數量 | 較少 | 較多 |

---

## ❗ 常見 Debug 情境

### EC Reset / Power 問題
- Reset 過快 → VRM 尚未穩定，造成無法啟動  
- VRM 初始化失敗 → BIOS 卡在 POST  
- Power Rail 漏電 → 無風扇、無畫面  

---

### BIOS POST Code × Power Rail 對照

| POST Code | 階段說明 | 問題 Rail |
|-----------|----------|-----------|
| 0x30~0x3F | Early CPU Init | VCORE/VCCSA |
| 0x50~0x5F | Memory Init | VDDQ/VPP |
| 0xC0~     | ME Init | VCCST/ME Domain |

---

## 📟 EC Debug Pin 表

| Pin | 功能 | 備註 |
|-----|------|------|
| ACIN | AC 偵測 | 高為接上 |
| ALL_SYS_PWRGD | 全 Rail OK 訊號 | |
| PWRBTN# | Power Button | 低為按下 |
| EC_UART_TX/RX | UART 訊號 | 抓取 log |

---

## 🔊 BIOS Beep Code 對照

| Beep | 錯誤 | 原因 |
|------|------|------|
| 1 short | 正常 | 無問題 |
| 1 long 2 short | 顯示錯誤 | VAXG 未供電 |
| No beep | 無啟動 | CPU/BIOS 錯誤 |

---

## 📤 EC UART Log 判讀建議

- `EC_Init OK` → 初始化成功  
- `Watchdog Reset` → BIOS 異常  
- `ACIN LOST` → AC 電壓不穩  
- 無 log → Rail 啟動失敗或卡住

---


> Maintained by TPM/Debug PM Team · Last updated: 2025-05
