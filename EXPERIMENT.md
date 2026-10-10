# Feit–Thompson CogAnchor experiment

Source: the identical `feit_thompson` templates in the two LeanEval gap collections fetched on 2026-10-10. The benchmark source revision is `38361be884302c7edce1908c4aef8296eb2cb27e`. Original source bytes are retained separately; this is a new proof run, with no imported proof checkpoints or model solutions.

Workflow: [feature/coganchor-remote-workers](https://github.com/humanfia/math-lean-flow/tree/feature/coganchor-remote-workers). A controller discovers ready issues, obtains durable claims, and uses CogAnchor to launch one-shot remote workers. Two physical nodes are configured; independent child issues can run concurrently after decomposition. The global claim ledger prevents overlap with existing jobs.

Worker and independent reviewer: `codex/gpt-6-astra:max`. Network search disabled. Automatic merge and issue closure disabled. Lean 4.35.0-rc4 with Mathlib `a02a63c2100af866343c74550041885f8f39f099`; the original snapshot used rc3. The theorem contract is unchanged. Acceptance requires exact-type comparison, kernel and transitive-axiom checks, and Nanoda. A successful baseline build containing sorry is not proof acceptance.

[Live theorem status](https://zhengyangzhang06.github.io/Feit/theorem-status/index.html). Proof status begins unsolved. Worker heartbeat observations do not measure live model processes.
