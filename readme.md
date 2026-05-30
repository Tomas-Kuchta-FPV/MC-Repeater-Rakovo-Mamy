# MC Repeater Board - Rakovo Mámy

> **Note:** This project is a work in progress and not as polished as some of our other releases. Please keep this in mind if you plan on ordering or manufacturing the board.

This is a custom PCB designed to host the **E22P-868M30S** $1\text{W}$ LoRa transmission module. 

The board features an onboard solar MPPT charger (**SD30CRMA**), a carefully optimized power rail with robust filtering, a dedicated slot for a **DS3231** Real-Time Clock (RTC), and a **PIC12F** microcontroller dedicated to low-power management.

## Motivation

After *TvojeMama* released his original MC repeater board, *Radek* envisioned several hardware improvements. He drafted the core schematic, and I stepped in to complete the PCB routing and layout. 

---

## Hardware Preview

![PCB](PCB_Front.png)

---

## Firmware (Work in Progress)

### nRF52840
The pinout is compatible with the generic nRF52 Nano v2.0 footprints. 
* **Project Base Documentation:** [MeshCore Repeatery (yomamesh)](https://meshcore.cz/doku.php?id=repeatery:yomamesh#v115_build_1942026_rozsirena_verze_o_pwrmgt_prikazy_a_bootlock_27v)
* **Firmware Repository:** [MeshCore Git - promicro_e22p variant](https://github.com/cncnet-info/MeshCore/tree/feature/promicro-e22p-fw-sync/variants/promicro_e22p)

### PIC Microcontroller
The onboard PIC handles watchdog features and power management sleep cycles.
* **Watchdog Firmware Repository:** [MeshCore_wdt Git](https://github.com/cncnet-info/MeshCore_wdt)