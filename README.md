# UPC-RA
### Universal Product Code Rounded A-Format

**A proposed circular barcode system for product identification.**

UPC-RA is an experimental barcode symbology designed to represent product identification data using a circular structure rather than the traditional rectangular layout of conventional barcodes.

The project explores a combination of concentric rings and radial sectors to create a barcode that can be printed on cylindrical packaging, such as bottles, containers, and other rounded products.

> **Project status:** Experimental — Initial Design and Research  
> **Version:** 0.1.0  
> **Type:** Proposed barcode symbology

---

## 1. Introduction

Traditional barcodes, such as UPC-A, use parallel vertical bars arranged in a rectangular format.

Although these barcodes are widely used, their rectangular layout can be inconvenient for certain product designs, especially cylindrical packaging.

UPC-RA explores a different approach: arranging barcode information around a circular center.

The main idea is to create a circular barcode that combines:

- Concentric circular rings.
- Radial divisions or sectors.
- Small square or line-shaped data modules.
- Three small circular reference markers.
- A structured system for encoding and decoding product identification data.

The objective is to investigate whether this structure can provide reliable product identification when printed on curved surfaces.

---

## 2. Design Concept

UPC-RA uses a hybrid circular architecture.

Instead of arranging all information in straight horizontal or vertical lines, information is distributed around a circular structure.

### 2.1 Hybrid Architecture

The proposed design combines two geometric structures:

**Concentric rings**

Circular rings surround the center of the barcode. Different rings can have different responsibilities, such as synchronization, identification data, and error correction.

**Radial sectors**

The rings can be divided into smaller sections using lines extending outward from the center.

These sections create individual areas where data modules can be placed.

### 2.2 Three-Circle Reference System

The design includes three small circles positioned at specific locations.

Their proposed purpose is to help a decoder identify:

- The barcode's orientation.
- Its rotational position.
- Its geometric alignment.
- Its approximate center.

The exact positions, sizes, and decoding rules for these circles will be defined in the technical specification.

### 2.3 Data Modules

The encoded information will be represented using two-dimensional visual modules.

Possible module shapes:

- Small squares.
- Short lines.
- Radial segments.
- Other defined geometric patterns.

These modules will be distributed across the circular structure.

The final module shape must be selected based on printing quality, camera readability, and decoding reliability.

---

## 3. Main Objectives

UPC-RA aims to:

1. Develop an alternative circular barcode architecture.
2. Explore product identification using a UPC-style numeric identifier.
3. Investigate barcode readability on cylindrical packaging.
4. Support rotational orientation detection.
5. Develop a reliable encoding and decoding algorithm.
6. Investigate error detection and error correction.
7. Provide an open technical specification.
8. Allow independent developers to implement compatible encoders and decoders.

---

## 4. Proposed Architecture

The following architecture is a starting proposal, not a finalized specification.

| Component | Proposed purpose |
|---|---|
| Center region | Geometric reference |
| Three reference circles | Orientation and alignment |
| Inner ring | Synchronization or control information |
| Middle rings | Product identification data |
| Outer rings | Additional data or error correction |
| Radial sectors | Divide rings into data regions |
| Outer boundary | Define the barcode's physical limits |

The exact number of rings, sectors, and modules will be determined during development.

---

## 5. Data Encoding

UPC-RA intends to investigate compatibility with UPC-style product identification.

UPC-A traditionally represents a 12-digit numeric identifier.

A future UPC-RA specification will define how an identifier is converted into binary data and distributed across the circular modules.

The encoding specification must define:

- Supported character set.
- Numeric identifier format.
- Binary representation.
- Bit ordering.
- Module placement.
- Synchronization information.
- Error detection.
- Error correction.
- Version identification.

**Important:** Using UPC-A's 12-digit identifier does not make UPC-RA equivalent to UPC-A. The circular geometry and decoding algorithm will be different.

---

## 6. Decoding Process

A UPC-RA decoder is expected to follow a process similar to this:

1. Capture an image containing the barcode.
2. Detect the circular structure.
3. Locate the three reference circles.
4. Estimate the barcode's center and orientation.
5. Correct perspective and rotational distortion where possible.
6. Identify the rings and radial sectors.
7. Read the individual data modules.
8. Convert the modules into binary data.
9. Apply error detection and correction.
10. Decode the product identifier.
11. Validate the resulting identifier.

A successful implementation should be able to decode a barcode from different rotational positions and reasonable camera angles.

---

## 7. Cylindrical Packaging

One of the main research directions is printing UPC-RA on cylindrical objects.

Potential applications include:

- Water bottles.
- Soft drink bottles.
- Food containers.
- Cosmetic packaging.
- Cylindrical product labels.

However, a circular barcode does not automatically solve the optical distortion caused by curved surfaces.

Testing will be required to investigate:

- Different bottle diameters.
- Different printing sizes.
- Camera distances.
- Camera angles.
- Lighting conditions.
- Reflections.
- Label materials.
- Partial obstruction.

---

## 8. Project Structure

The repository will use the following structure as the project develops:

```text
UPC-RA/
│
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── CHANGELOG.md
│
├── specification/
│   ├── UPC-RA-SPEC-v0.1.md
│   ├── architecture.md
│   ├── geometry.md
│   ├── encoding.md
│   ├── decoding.md
│   ├── error-correction.md
│   └── physical-dimensions.md
│
├── docs/
│   ├── introduction.md
│   ├── how-it-works.md
│   ├── design-decisions.md
│   ├── examples.md
│   └── faq.md
│
├── encoder/
│
├── decoder/
│
├── tests/
│
├── examples/
│
├── hardware/
│
└── assets/
    ├── diagrams/
    └── prototypes/
```

---


## 9. Standards and Compatibility

UPC-RA is an independent experimental proposal.

It is not currently an official GS1 barcode format or an officially recognized replacement for UPC-A.

Existing barcode standards provide useful technical references:

- **ISO/IEC 15420:** EAN/UPC barcode symbology.
- **ISO/IEC 15416:** Linear barcode print quality.
- **ISO/IEC 15415:** Two-dimensional barcode print quality.
- **ISO/IEC 18004:** QR Code symbology.
- **ISO/IEC 16022:** Data Matrix symbology.

These standards can help guide the development of encoding, decoding, physical dimensions, and quality-testing procedures.

Official references:

- [ISO](https://www.iso.org/)
- [GS1 General Specifications](https://ref.gs1.org/standards/genspecs/)

Publishing UPC-RA on GitHub does not make it an officially recognized barcode standard. Formal recognition would require a separate standardization process.

---

## 10. Contributions

Contributions are welcome.

Areas where developers and researchers can contribute include:

- Circular barcode geometry.
- Binary encoding.
- Image processing.
- Computer vision.
- Barcode generation.
- Barcode decoding.
- Error correction.
- Optical testing.
- Cylindrical printing experiments.

Before implementing a feature, please document the proposed behavior and how it relates to the UPC-RA specification.

---

## 11. License

The project's source code and specification should use clearly defined licenses.

The final license selection will be documented here.

---

## Author 
Deadcode

# License 
MIT
