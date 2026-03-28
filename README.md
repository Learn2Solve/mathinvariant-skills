# mathinvariant-skills

My [Claude Code](https://docs.anthropic.com/en/docs/claude-code) custom skills.

## Skills

| Skill | Description |
|-------|-------------|
| **board-of-advisors** | Convene a personal board of directors for high-stake decisions. Dynamically selects advisors, deep-researches each one (20-25K profile), spawns them as independent agents, and produces a formal board resolution with majority view, dissent, and action assignment. Built on [ljg-roundtable](https://github.com/lijigang/ljg-skills) by Li Jigang. |

## Install

```bash
git clone https://github.com/Learn2Solve/mathinvariant-skills.git ~/.claude/skills/mathinvariant-skills
```

Then restart Claude Code. Use `/board-of-advisors` to start.

## Board of Advisors

A multi-agent boardroom skill for high-stake decisions. See [full documentation](skills/board-of-advisors/README.md).

**What it does:**
1. You describe your decision
2. Dynamically selects 3-5 advisors most relevant to your topic
3. Deep-researches each advisor via web search (cached for reuse)
4. Spawns each advisor as an independent Claude agent
5. Runs a structured debate: opening statements, tension identification, focused exchanges
6. Produces a formal board resolution with majority recommendation, dissent, and action assignment

**Pre-loaded advisors:** Charlie Munger, Elon Musk, Zhuangzi, Sun Tzu, Seneca. Any new advisor is automatically researched and cached on first use.

**Interactive commands:** 继续 / 结束 / 深入 / 加人 / 我想说

### Acknowledgments

Board of Advisors builds on [ljg-roundtable](https://github.com/lijigang/ljg-skills/tree/master/skills/ljg-roundtable) by 李继刚 (Li Jigang).

**Borrowed from ljg-roundtable:**
- Dynamic advisor selection (tension network principle)
- 简言之 one-line compression
- Action labels (陈述/质疑/补充/反驳/修正/综合)
- 挖深不铺广 moderator principle
- ASCII structural visualization
- Interactive steering commands
- Surprise voice principle

**What we added:**
- Multi-agent architecture (separate Claude agent per advisor, context isolation)
- Deep research profiles (20-25K per advisor via web search, cached permanently)
- Decision-oriented output (board resolution, not knowledge network)
- @mention system for organic cross-advisor conversation
- Board Chair participation (user joins the debate)
- Fictional character support (e.g., Han Li from "A Record of a Mortal's Journey to Immortality")
- Profile accumulation (advisor library grows over time)

## License

MIT
