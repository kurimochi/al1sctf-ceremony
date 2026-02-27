# Participation Guide

This document describes the steps for participating in the Groth16 Phase 2 Trusted Setup.

## Rules

- Always use the **zkey from the latest Release**.
- Obtain the zkey **only from GitHub Releases** (PR attachments and external mirrors are not allowed).
- **Securely generate your own entropy** (`/dev/urandom`, physical dice, etc.).
- After the work, **completely delete** temporary files used for entropy generation and intermediate processing.

## Steps

### Prerequisites

- `snarkjs` ([Installation Guide](https://github.com/iden3/snarkjs?tab=readme-ov-file#install-snarkjs))
- `gpg` (a key for signing should be ready)

### Step 1: Download the latest zkey

Obtain `flag_verifier_00XX.zkey` from the latest Releases.

### Step 2: Perform the Contribution

```bash
snarkjs zkey contribute flag_verifier_00XX.zkey flag_verifier_00YY.zkey --name="{Your Name}" -v
Enter a random text. (Entropy): xxxxxxxxxxxxxxxxxxxxxxxxxx
[INFO]  snarkJS: Circuit Hash:
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
[INFO]  snarkJS: Contribution Hash:
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
```

- Enter high-quality entropy at `Enter a random text. (Entropy):`.
- Keep `Circuit Hash` and `Contribution Hash` as they are (needed for attestation).

Example of directly passing random numbers from `/dev/urandom`:

```bash
snarkjs zkey contribute flag_verifier_00XX.zkey flag_verifier_00YY.zkey --name="{Your Name}" -v -e="$(openssl rand -hex 64)"
```

### Step 3: Create Attestation

1. Copy `template_attestation.md`.
2. Fill in the required fields and save it as `00XX_{Your Name}/attestation.md`.

### Step 4: Create a Signature

Execute the following in the same directory as `attestation.md`.

```bash
gpg --detach-sign --armor attestation.md
```

`attestation.md.asc` will be generated.

### Step 5: Create a Pull Request

1. Create a `contrib/00XX` branch.
2. Confirm that `flag_verifier_00YY.zkey`, `attestation.md`, and `attestation.md.asc` are located under `contributions/00XX_{Your Name}/`.
3. Commit the changes under `contributions/00XX_{Your Name}/`.
4. Create a Pull Request.