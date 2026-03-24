# NGSpice Circuit Simulations

A collection of professional analog circuit simulations built with [ngspice](https://ngspice.sourceforge.io/) — an open-source SPICE circuit simulator.

---

## Simulations

### 1. Sallen-Key 2nd Order Active Low-Pass Filter

A professional active low-pass filter design using the Sallen-Key topology with an ideal op-amp (VCVS model).

**Specifications**

| Parameter | Value |
|---|---|
| Filter Type | Sallen-Key Active LPF |
| Order | 2nd Order |
| Cutoff Frequency | ~1 kHz |
| Roll-off | -40 dB/decade |
| R1, R2 | 15.9 kΩ |
| C1, C2 | 10 nF |
| Analysis | AC Sweep (10 Hz – 100 kHz) |

**Frequency Response**

- Passband (< 1 kHz): ~0 dB gain — signals pass through unchanged
- Cutoff (~1 kHz): -3 dB attenuation
- Stopband (> 1 kHz): -40 dB/decade roll-off (characteristic of 2nd-order filter)

**Files**

| File | Description |
|---|---|
| `sallen_key_lpf.cir` | NGSpice netlist |
| `lpf_response.txt` | Simulation output — frequency vs gain (dB) |

---

## Requirements

- [ngspice](https://ngspice.sourceforge.io/) v45.2 or later
- macOS / Linux / Windows

**Install on macOS (Homebrew):**
```bash
brew install ngspice
```

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/KazmirFahrier/ngspice-simulations.git
cd ngspice-simulations

# Run the simulation
ngspice sallen_key_lpf.cir

# View the output data
cat lpf_response.txt
```

---

## Project Structure

```
ngspice-simulations/
├── README.md
├── sallen_key_lpf.cir       # Sallen-Key LPF netlist
└── lpf_response.txt         # AC analysis output data
```

---

## About

These simulations are part of my personal exploration of analog circuit design and SPICE simulation. More circuits coming soon — including high-pass, band-pass filters, and op-amp circuits.

---

## License

MIT License — feel free to use, modify, and share.
