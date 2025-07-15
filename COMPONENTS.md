# DIY Photonic Quantum Computer Design idea - never tested, probably not working as is, but hey, why not?

## Overview
This design outlines a basic photonic quantum demonstration system that can showcase quantum principles like superposition and entanglement using readily available components.

## Core Components

### 1. Light Source
- **Component**: 405nm violet laser diode (5mW)
- **Purpose**: Coherent photon source
- **Cost**: ~$20
- **Notes**: Must be properly collimated and filtered

### 2. Single Photon Generation
- **Method**: Heavy attenuation using neutral density filters
- **Components**: 
  - ND filter stack (OD 6-8 total)
  - Spatial filter (pinhole + lenses)
- **Cost**: ~$100
- **Alternative**: Use spontaneous parametric down-conversion (SPDC) with BBO crystal

### 3. Quantum State Preparation

#### Polarization Encoding
- **Components**:
  - Linear polarizers (3x)
  - Half-wave plates (2x)
  - Quarter-wave plates (2x)
- **Cost**: ~$150
- **Purpose**: Create and manipulate qubit states using photon polarization

### 4. Beam Splitting Network
- **Components**:
  - 50/50 beam splitters (4x)
  - Mirrors (8x)
  - Adjustable mounts
- **Cost**: ~$200
- **Purpose**: Create interferometric paths for quantum gates

### 5. Detection System
- **Components**:
  - Avalanche photodiodes (APDs) or PMTs (2x minimum)
  - Coincidence counting circuit
  - Time-to-digital converter (TDC)
- **Cost**: ~$500-1000
- **Notes**: This is the most expensive component

### 6. USB Interface
- **Components**:
  - Arduino Due or Teensy 4.1 (for timing precision)
  - Custom PCB for signal conditioning
  - USB 3.0 interface chip
- **Cost**: ~$100

## Quantum Gates Implementation

### Hadamard Gate
- Implemented using a half-wave plate at 22.5°
- Creates superposition states

### Phase Gates
- Quarter-wave plates at various angles
- Introduce relative phase shifts

### CNOT Gate (Challenging)
- Requires nonlinear optical elements
- Alternative: Use post-selection with coincidence counting

## System Architecture

```
[Laser] → [Attenuator] → [State Prep] → [Interferometer] → [Detectors] → [USB]
                              ↓
                        [Beam Splitter Network]
                              ↓
                        [Quantum Circuit]
```

## Software Requirements

### Data Acquisition
- High-speed photon counting (>1 MHz)
- Coincidence detection (<1ns resolution)
- Real-time histogram generation

### Quantum Circuit Simulation
- Compare experimental results with theory
- Tomography reconstruction
- Fidelity calculations

## Limitations & Considerations

### Temperature Stability
- Use enclosure with thermal insulation
- Monitor temperature drift
- Optical table or breadboard recommended

### Alignment Challenges
- Requires precise optical alignment
- Use kinematic mounts
- Consider active stabilization for long experiments

### Coherence Time
- Limited by environmental noise
- Typical coherence: microseconds
- Sufficient for basic quantum operations

## Simplified Starter Version

For initial experiments, consider:
1. Single photon interference demonstration
2. Hong-Ou-Mandel dip measurement
3. Basic polarization entanglement

## Total Estimated Cost
- Basic system: $1,000-1,500
- Advanced system: $3,000-5,000

## Safety Considerations
- Use laser safety goggles
- Enclose beam paths
- Follow local laser safety regulations

## Next Steps
1. Start with classical optics alignment
2. Implement single photon detection
3. Build up to quantum interference
4. Attempt basic quantum algorithms

This design provides a foundation for exploring quantum optics at home while being realistic about the challenges and limitations of DIY quantum computing.
