# Attestation for aL1sCTF Groth16 Phase 2 Trusted Setup Ceremony

**GitHub Handle:** `@kurimochi`  
**Full Name (optional):**  
**Date & Time (UTC):** `2026-02-27 23:26`  
**Contribution Number:** `0001`

## Contribution Details

- **Input (parent) zkey:** `flag_verifier_0000.zkey`
- **Output zkey:** `flag_verifier_0001.zkey`

**Hashes** (copy exactly from `snarkjs` output):
```
[INFO]  snarkJS: Circuit Hash: 
                4d53148b 6fd798a2 ca4ee829 a50d7e6b
                31e4d14a e8e24e93 40479d40 0da7ae0b
                e55d395d b683743e d561cc9d 35709a54
                5200e19a f07798bf 3c93a764 99552d9b
[INFO]  snarkJS: Contribution Hash: 
                e833f9d6 05e467f6 69d033ae 5037e968
                aafa63a8 c5f84725 6f0dd192 89a8b57b
                65de4197 3ab161c2 05e1cec6 3c4d5968
                b19a4bbd 085e0fde 93c4fd14 4aaeee54
```

## Entropy Source (Critical for security)

The 64 bytes were generated as entropy from `/dev/urandom` on an offline machine. The output from `/dev/urandom` can be considered reliable because `/proc/sys/kernel/random/entropy_avail` was 256 just before generation. Additionally, the machine was restarted before being brought back online.

## Commands I Executed

```bash
$ cat /proc/sys/kernel/random/poolsize
256
$ cat /proc/sys/kernel/random/entropy_avail
256
$ snarkjs zkey contribute contributions/0000_genesis/flag_verifier_0000.zkey contributions/0001_Kurimochi/flag_verifier_0001.zkey --name="Kurimochi" -e="$(openssl rand 64)"
```

## Environment

- OS: Arch Linux
- `snarkjs` version: 0.7.6
- Hardware/notes: HP Victus 15 fa1xxx, contribution performed offline

## Declaration

I, `@kurimochi`, solemnly declare that:

- The entropy described above was generated solely by me and was truly random.
- I did not keep, record, or share any part of the toxic waste / trapdoor.
- I understand that the security of the entire ceremony relies on at least one honest participant.
- I securely and permanently deleted files related to toxic waste generation.
