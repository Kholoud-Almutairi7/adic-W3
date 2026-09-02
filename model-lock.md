# Model Lock Record

## The locked model

- Model id: Qwen/Qwen2.5-1.5B-Instruct-AWQ
- Quantisation: awq
- Why this one: Passed the function-calling smoke test with 10/10, with both distractor attempts staying call-free.

## The launch flags

--model Qwen/Qwen2.5-1.5B-Instruct-AWQ
--dtype half
--max-model-len 4096
--gpu-memory-utilization 0.85
--port 8000
--quantization awq
--enable-auto-tool-choice
--tool-call-parser hermes

- Tool-call parser: hermes

## The smoke score

- Score (valid behaviours out of 10): 10
- Distractor stayed call-free in the majority: yes
- Passed the gate (>= 8/10 and distractor majority clean): yes
- Measured against: AWQ

## Quality spot check note

AWQ produced usable answers across the five-prompt spot check. There were some wording and quality issues on individual prompts, but no obvious catastrophic degradation was observed.