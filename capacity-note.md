# Capacity note (team, one page)

## The numbers

- Locked model: Qwen/Qwen2.5-1.5B-Instruct-AWQ
- Target p95 end-to-end latency (your SLO today): 2.0 seconds
- Knee concurrency (highest concurrency whose p95 is still under target): 8
- Tokens per second at the knee: 455.56
- Max sustainable request rate at the target p95: 4.39 req/s

## The limiting family

One sentence, using this morning's triage lens (compute vs memory vs overhead):
Memory-bound: throughput continues to rise with concurrency, but p95 latency crosses the 2.0 s SLO at concurrency 16, indicating the useful capacity is limited by increasing serving pressure rather than a lack of available concurrency.

## Why the knee, not the peak

We report the knee because it is the highest concurrency that still meets the latency SLO; the peak throughput at higher concurrency comes with unacceptable p95 latency.