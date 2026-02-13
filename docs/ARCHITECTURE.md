# Memory System Architecture

## Core Concepts

### Salience Scoring

Every memory gets a base confidence score (0.0-1.0) at creation time, then modified over time.

### Memory Categories

1. **USER_PERSONAL**: York's preferences, identity, boundaries
2. **AGENT_IDENTITY**: Vesper's self-definition, lessons learned
3. **DOCUMENT_KNOWLEDGE**: PDFs, articles, external materials
4. **SYSTEM_CONFIG**: Infrastructure, secrets, integrations

### Lifecycle

```
Capture → Score → Route → (Confirm) → Decay → Promote/Demote
```

## Implementation Phases

### Phase 1: Quick Wins (This Weekend)
- [ ] Directory structure (`memory/salience/`)
- [ ] Metadata template with salience fields
- [ ] Update AGENTS.md guidelines

### Phase 2: Structural (Week 1-2)
- [ ] `memory_decay.py` script
- [ ] Weighted search implementation
- [ ] Confirmation loop for uncertain facts

### Phase 3: Advanced (Month 2+)
- [ ] Memory Dashboard web UI
- [ ] Contradiction detection
- [ ] Knowledge graph visualization

## Integration Points

- OpenClaw: Tool execution
- Notion: Planning documents
- Claude: Design/architecture
- ChatGPT: Strategy/analysis
