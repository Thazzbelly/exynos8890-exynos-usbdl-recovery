# SM-A226B Recovery Binaries

This directory contains the split bootloader binaries for Samsung Galaxy A22 (SM-A226B).

## Required Files

Place the following split binaries in this directory:

- `fwbl1.bin` - BL1 (First stage bootloader)
- `el3_mon.bin` - EL3 monitor (ARM Trusted Firmware)
- `bl2.bin` - BL2 (Second stage bootloader)
- `bootloader.bin` - Main bootloader (U-Boot)

## Device Information

**Model:** SM-A226B (Galaxy A22)

**Firmware Version (from last known state):**
- BL: A226BXXSBDYA2
- AP: A226BXXSBDYA2
- CP: A226BXXSBDYA1
- CSC: A226BODMBDYA2
- Country: INS

**Serial:** R9WR50EBV0J

## Extraction

These binaries should be extracted from the device's `SBOOT.BIN` using the `split-sboot` script.
Reference the main README for extraction instructions.

## Usage

Once binaries are placed here, use the recovery script:
```bash
cd ..
sudo ./exynos-usbdl-recover.sh
# Select option 6 for SM-A226B
```

## Notes

- Ensure device is in USB-DL mode before running recovery
- Keep POWER button pressed during the entire flashing process
- On Windows, use the config file: `exynos-usbdl_a226b.cfg` with MultiDownloader
