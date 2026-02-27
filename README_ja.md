# aL1sCTF Groth16 Phase 2 Trusted Setup Ceremony
このリポジトリは、aL1sCTFのGroth16 zk-SNARK回路に対するPhase 2 Multi-Party Computation (MPC) Trusted Setupを行うための公開セレモニーです。

- Circuit: R1CS, 2683 constraints, BN254 curve
- Phase 1: PSE Perpetual Powers of Tau (12 powers)
- Tool: snarkjs 0.7.6

**Current: 開始前**

## セレモニー情報

### Circuit
このセレモニーの対象回路に関するファイルは`circuits/`にあります。
- `circuits/flag_verifier.r1cs`: 回路制約 (R1CS)
- `circuits/flag_verifier.sym`: 回路監査向け (Sym)

また回路のソースコードは[aL1sCTF](https://github.com/kurimochi/aL1sCTF)にあります。

### Phase 1
aL1sCTFのPhase 2は、PSEのPowers of Tauをベースに生成されています。

[PSE Powers of Tau (12 powers)](https://pse-trusted-setup-ppot.s3.eu-central-1.amazonaws.com/pot28_0080/ppot_0080_12.ptau)  (4.6MiB)
