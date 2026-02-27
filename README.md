[日本語](README_ja.md)

# aL1sCTF Groth16 Phase 2 Trusted Setup Ceremony
This repository contains the public ceremony for conducting the Phase 2 Multi-Party Computation (MPC) Trusted Setup for the aL1sCTF Groth16 zk-SNARK circuit.

- Circuit: R1CS, 2683 constraints, BN254 curve
- Phase 1: PSE Perpetual Powers of Tau (12 powers)
- Tool: snarkjs 0.7.6

**Current: Before Start**

## Ceremony Information

### Circuit
Files related to the target circuit for this ceremony are located in `circuits/`.
- `circuits/flag_verifier.r1cs`: Circuit constraints (R1CS)
- `circuits/flag_verifier.sym`: For circuit auditing (Sym)

The circuit's source code can also be found in [aL1sCTF](https://github.com/kurimochi/aL1sCTF).

### Phase 1
Phase 2 of aL1sCTF is generated based on PSE's Powers of Tau.

[PSE Powers of Tau (12 powers)](https://pse-trusted-setup-ppot.s3.eu-central-1.amazonaws.com/pot28_0080/ppot_0080_12.ptau) (4.6MiB)

## How to Participate
Please refer to the [Participation Guide](CONTRIBUTING.md).
