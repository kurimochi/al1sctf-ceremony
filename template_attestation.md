# Attestation for [YOUR_CIRCUIT_NAME] Groth16 Phase 2 Trusted Setup Ceremony

Fill in all placeholders before submitting.

**GitHub Handle:** `@yourusername`  
**Full Name (optional):** `Your Full Name`  
**Date & Time (UTC):** `YYYY-MM-DD HH:MM`  
**Contribution Number:** `00XX`

## Contribution Details

- **Input (parent) zkey:** `flag_verifier_00XX.zkey`
- **Output zkey:** `flag_verifier_00YY.zkey`
  - If you overwrote the input file, write the same filename for both.

**Hashes** (copy exactly from `snarkjs` output):
```
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

## Entropy Source (Critical for security)

Describe precisely how you generated entropy. Be specific (device, method, offline/online status, and cleanup).

Example:
> I used a fresh Ubuntu live USB on an offline machine. I rolled a physical 6-sided die 64 times, typed random keystrokes for 60 seconds while using a private passphrase, then mixed in random bytes from `/dev/urandom`. After the contribution, I securely deleted all temporary files.

## Commands I Executed

```bash
# Exact command(s) I ran
snarkjs zkey contribute flag_verifier_00XX.zkey flag_verifier_00YY.zkey --name="Your Name" -v
```

## Environment

- OS: (e.g. macOS 15 / Ubuntu 24.04)
- `snarkjs` version: (e.g. 0.7.6)
- Hardware/notes: (e.g. personal laptop, contribution performed offline)

## Declaration

I, `@yourusername`, solemnly declare that:

- The entropy described above was generated solely by me and was truly random.
- I did not keep, record, or share any part of the toxic waste / trapdoor.
- I understand that the security of the entire ceremony relies on at least one honest participant.
- I securely and permanently deleted files related to toxic waste generation.
