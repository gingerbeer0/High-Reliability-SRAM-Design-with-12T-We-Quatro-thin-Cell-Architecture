# 📐 12T We-Quatro SRAM Design with Thin-Cell Layout

> A VLSI project implementing a **radiation-hardened 12-transistor SRAM** using the **We-Quatro** architecture and **thin-cell layout**. Includes schematic design, simulation, layout, and DRC/LVS verification.

---

## 🔍 Overview

This project implements a high-reliability **12T We-Quatro SRAM** cell optimized for **parametric variation tolerance**, **soft-error resilience**, and **writability**, especially under scaled CMOS technologies. We designed and simulated the cell using a thin-cell layout to meet modern lithographic constraints.
![image](https://github.com/user-attachments/assets/6f073052-dbef-4061-9a45-68555b8108cd)
![image](https://github.com/user-attachments/assets/7a6d3fcf-eb61-4d53-986a-6995bffb1324)



---

## 🧠 Key Features

- ✅ **12-Transistor We-Quatro Cell**: Improved writability vs. standard Quatro 10T cell
- ✅ **Thin-Cell Layout**: Enables dense integration and EUV-friendly design
- ✅ **Radiation-Hardened**: Dual-interlocked structure resists SEUs
- ✅ **Optimized Transistor Sizing**: 
  - Pull-down NMOS: ~1.5× minimum size
  - Pull-up PMOS & Access NMOS: minimum size
- ✅ **Verified by DRC / LVS / Monte Carlo simulations**

---

## 📊 Simulation Results

We simulated 5 wordlines (WL[0] to WL[4]) and verified the correct operation of each SRAM cell.

![image](https://github.com/user-attachments/assets/1326fa03-9a5b-4971-b315-110b8cb54f8b)
![image](https://github.com/user-attachments/assets/64c5fd6e-10c5-459f-8fdf-12d553ec772a)

-WL[0]
![image](https://github.com/user-attachments/assets/42aead2c-b2ad-4237-90c5-78ebf17133f1)

-WL[1]
 ![image](https://github.com/user-attachments/assets/3bc6d58b-c79f-4b42-be87-7a95352b8e24)

-WL[2]
![image](https://github.com/user-attachments/assets/f83f83fc-cfd0-45f4-ace1-a93791466abe)

-WL[3]
 ![image](https://github.com/user-attachments/assets/a3c8ec58-5a54-44f6-bc64-7b8cf78d8cb2)

-WL[4]
 ![image](https://github.com/user-attachments/assets/7f632932-f25b-4b28-8c4b-7dacca866c5b)



---

## 🧱 Layout Highlights

- Layouts created for:
  - We-Quatro Cell
  - Precharger (3 PMOS)
  - Sense Amplifier
  - 5x5 Cell Array
- Final layout is **DRC/LVS clean**
- Cell array dimensions: `3.235μm × 10.475μm = 33.89μm²`

-We-Quatro Cell
 ![image](https://github.com/user-attachments/assets/8db167b4-ab73-4088-ada4-009839fd75cd)

-Precharger
 ![image](https://github.com/user-attachments/assets/dc088aad-ab2f-4e91-b11b-c49fd3e85052)

-Sense Amplifier
 ![image](https://github.com/user-attachments/assets/29db8a76-5ed2-4512-b23a-a4e2a93c80b1)

- Cell array(5X5)
 ![image](https://github.com/user-attachments/assets/b428c070-649f-4cbb-adba-c9ce7bcd1842)

- Full layout
 ![image](https://github.com/user-attachments/assets/88b38aec-aaa9-4725-981d-19cc0ce58f45)

-DRC, LVS

![image](https://github.com/user-attachments/assets/23769a72-0da2-4e09-a921-46526afd5bce)

![image](https://github.com/user-attachments/assets/ea66f151-9f88-460e-baf8-35c8d7856219)


---

## 🔬 Peripheral Circuits

### Precharger (3 PMOS)
- M0, M1: Charge BL, BLB
- M2: Equalize BL and BLB before access
![image](https://github.com/user-attachments/assets/69dd047e-10ed-4d85-aec3-c272cf7f5845)

### Sense Amplifier
- Differential voltage sensing
- Low static power consumption

![image](https://github.com/user-attachments/assets/f1ac592e-d80a-4ac9-a574-be8934cabd7a)

---

## 🧠 Why Thin-Cell We-Quatro?

> Referenced from [IEEE TNS, 2017 - Dang et al.]  
The **We-Quatro** structure improves upon the 10T Quatro by:
- Adding 2 more access transistors to address poor writability
- Maintaining similar area using efficient thin-cell layout
- Providing **comparable soft-error resilience** with enhanced **write margin**
- Achieving faster 100 mV bitline swing (≥27% faster than 6T)

---

## 📚 References

- Dang, L.D.T., Kim, J.S., Chang, I.J., “We-Quatro: Radiation-Hardened SRAM Cell With Parametric Process Variation Tolerance”, IEEE Transactions on Nuclear Science, 2017.
- VLSI Project #2 Report – Korea University, 2025


