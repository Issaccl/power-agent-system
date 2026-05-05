# Power Agent System

Multi-agent collaborative decision system for smart grid dispatch.

## Architecture

## Core Logic

**Predict Agent**: LSTM-based load forecasting (from my open-source component)

**Monitor Agent**: Real-time anomaly detection, trigger threshold >50MW deviation

**Diagnose Agent**: Chain-of-Thought long-chain reasoning

**Decide Agent**: Multi-objective scoring → output final strategy + explanation

**Feedback Agent**: Record results, optimize Diagnose Agent reasoning strategy

## Demo Run

```python
from agent_core import run_system
result = run_system(predict=1200, actual=1350)
{
  'predict': 1200,
  'actual': 1350, 
  'anomaly': True,
  'diagnosis': 'Step1: Deviation>50 | Step2: Check weather | Step3: Plan B',
  'decision': 'Activate backup unit'
}

---

## 第三步：Q4 + Q5 填写

### Q4 粘贴：
