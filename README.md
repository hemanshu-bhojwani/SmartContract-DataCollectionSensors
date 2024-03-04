# CCDS Building Sensor System (DS453 Final Project)

## Overview

Comprehensive sensor system and software designed for data collection in the CCDS building at Boston University. This system captures crucial information related to temperature, energy consumption, and trash collection. The sensors and software work seamlessly to ensure data accuracy, security, and transparency.

## Design

![System Design Diagram](https://github.com/hemanshu-bhojwani/SmartContract-DataCollectionSensors/blob/main/DesignDiagram.png?raw=true)

### Sensors

- Each sensor collects data on energy consumption, temperature, and waste production.
- Securely stores a private key and relevant data locally.
- Collects data every minute and aggregates it daily.

### Data Aggregation

- Utilizes Multi-Party Computation (MPC) to compute daily totals securely.
- Maintains confidentiality by ensuring data from individual sensors remains private.

### Digital Signatures

- Employs a Public Key Infrastructure (PKI) for secure communication and source verification.
- Locally and securely stores its private key for data transmission.

### Smart Contract

- Governs the behavior of sensors to ensure accurate and trustworthy data collection.
- Acts as a governing mechanism for sensors, enforcing standards and integrity.

### Blockchain

- Posts daily totals and corresponding Zero-Knowledge (ZK) proofs to the blockchain.
- Ensures data transparency, with daily totals available publicly while securing intermediate data.

### ZK Proof

- Generates ZK proof using Circom circuits to prove the origin and accuracy of sensor data.
- Two verifiers available for summed totals and averaged totals.

## Code Functionality

- Demonstrates sensor functionality for trash data and can be extended for energy and temperature.
- Captures data with high precision using specialized equipment.
- Sensor behavior governed by a smart contract to maintain data integrity.

## Smart Contract Governance

- Sensitive data remains private to sensors, ensuring confidentiality.
- Only authenticated sensors can access relevant functions, participate in MPC, and post data.
- Posting daily totals limited to once a day and after a specific time for integrity assurance.

## PKI Functionality

- Implemented within the smart contract.
- Sensors use private keys to sign data, creating digital signatures.
- Public keys verify data authenticity, ensuring it comes from the correct sensor.
- Sensors share public keys for network authentication.

## ZK Proof Generation

- Daily ZK proof generated for each data type using Circom circuits.
- Proves the correctness of daily totals and the origin of sensor data.
- Ensures data accuracy and authenticity.

## Conclusion

Our sensor system and software combination provide Boston University with a robust solution for collecting accurate and trustworthy data. The integration of advanced technologies, secure protocols, and a smart contract governance system ensures the system's reliability and confidentiality. Feel free to explore our code repository for a detailed understanding of the implementation.
