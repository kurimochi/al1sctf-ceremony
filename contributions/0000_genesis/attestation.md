# Attestation for anonymous Groth16 Phase 2 Trusted Setup Ceremony

**GitHub Handle:** `@kurimochi`  
**Full Name (optional):**  
**Date & Time (UTC):** `2026-02-27 21:03`  
**Contribution Number:** `0000`

## Contribution Details

- **Input (parent) zkey:** N/A (groth16 setup output)
- **Output zkey:** `flag_verifier_0000.zkey`

**Hashes** (copy exactly from `snarkjs` output):
```
[INFO]  snarkJS: Circuit hash: 
                4d53148b 6fd798a2 ca4ee829 a50d7e6b
                31e4d14a e8e24e93 40479d40 0da7ae0b
                e55d395d b683743e d561cc9d 35709a54
                5200e19a f07798bf 3c93a764 99552d9b
```

## Entropy Source (Critical for security)

With `snarkjs groth16 setup`, entropy is not required, so there's no need to be concerned about it here.

## Commands I Executed

```bash
$ curl -fsSLO https://pse-trusted-setup-ppot.s3.eu-central-1.amazonaws.com/pot28_0080/ppot_0080_12.ptau
$ b2sum ppot_0080_12.ptau
3ee85ae13672d1d742117566126f31d678cf72d480f0df8e2aec78d77771433392ae01bb2b11c4ea0e60b244415be0a12a02e51d3f7a4a8b5c1c982fa208c4cd  ppot_0080_12.ptau
$ snarkjs groth16 setup circuits/flag_verifier.r1cs ppot_0080_12.ptau contributes/0000_genesis/flag_verifier_0000.zkey
```

## Environment

- OS: Arch Linux
- `snarkjs` version: 0.7.6
- Hardware/notes: HP Victus 15 fa1xxx

## Declaration

I, `@kurimochi`, solemnly declare that:

- The entropy described above was generated solely by me and was truly random.
- I did not keep, record, or share any part of the toxic waste / trapdoor.
- I understand that the security of the entire ceremony relies on at least one honest participant.
- I securely and permanently deleted files related to toxic waste generation.
