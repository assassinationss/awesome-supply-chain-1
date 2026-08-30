# Awesome Supply Chain - Claude Code Plugin

This plugin provides 133 comprehensive AI agent skills for supply-chain decision framing, management, operations research, and logistics optimisation.

## What is this plugin?

This is a Claude Code plugin that gives your AI coding assistant deep expertise in:
- Supply chain planning and forecasting
- Operations research problems (VRP, TSP, facility location, etc.)
- Inventory optimization and warehouse management
- Transportation and logistics
- Manufacturing and production scheduling
- Procurement and sourcing
- Domain-specific solutions for retail, CPG, energy, healthcare, and more

## Skills Included

The plugin contains **133 skills** organized into:
- **Core Supply Chain Functions** (45 skills)
- **Domain-Specific Verticals** (34 skills)
- **Operations Research Problems** (43 skills)
- **Advanced Optimization, AI & Decision Framing** (11 skills)

Each skill provides:
- Expert frameworks and methodologies
- Working Python code implementations
- Optimization algorithms and models
- Real-world problem-solving approaches
- Tool and library recommendations
- Common challenges and solutions

## How Skills Work

Skills are automatically triggered by keywords in your conversation. For example:
- Mentioning "demand forecast" or "time series" triggers the `demand-forecasting` skill
- Saying "vehicle routing" or "VRP" activates the `vehicle-routing-problem` skill
- Asking about "warehouse slotting" triggers the `warehouse-slotting-optimization` skill

You can also invoke skills directly:
```
"Use the knapsack-problems skill to maximize cargo value"
"Apply the lean-manufacturing skill to reduce waste"
```

## Installation

### Option 1: Cross-agent CLI install

Use the Agent Skills CLI to install skills to Claude Code, Codex, Cursor, GitHub Copilot, or another supported agent:

```bash
# List available skills
npx skills add kishorkukreja/awesome-supply-chain --list

# Install the decision-framing skill
npx skills add kishorkukreja/awesome-supply-chain --skill supply-chain-decision-to-delegation

# Install it globally for Claude Code and Codex
npx skills add kishorkukreja/awesome-supply-chain \
  --skill supply-chain-decision-to-delegation \
  --global \
  --agent claude-code \
  --agent codex
```

See [the complete agent installation guide](../docs/agent-installation.md) for standalone and manual options.

### Option 2: Claude Code Plugin
Install via Claude Code's built-in plugin system:

```bash
# Add the marketplace
/plugin marketplace add kishorkukreja/awesome-supply-chain

# Install all supply chain skills
/plugin install supply-chain-skills@awesome-supply-chain
```

### Option 3: Clone and Copy
Clone the entire repo and copy the skills folder:

```bash
git clone https://github.com/kishorkukreja/awesome-supply-chain.git
cp -r awesome-supply-chain/skills/* .claude/skills/
```

### Option 4: Git Submodule
Add as a submodule for easy updates:

```bash
git submodule add https://github.com/kishorkukreja/awesome-supply-chain.git .claude/awesome-supply-chain
```

Then reference skills from `.claude/awesome-supply-chain/skills/`.

### Option 5: Fork and Customize
1. Fork this repository
2. Customize skills for your specific needs
3. Clone your fork into your projects

### For other AI coding assistants

The skills follow the open Agent Skills specification. Use `npx skills add` and select the target agent, or copy an individual skill directory into the agent's documented skill location.

## Directory Structure

```
awesome-supply-chain/
├── .claude-plugin/
│   ├── marketplace.json     # Plugin marketplace metadata
│   └── README.md            # This file
├── skills/                  # 133 skill directories
│   ├── demand-forecasting/
│   │   └── SKILL.md
│   ├── vehicle-routing-problem/
│   │   └── SKILL.md
│   └── [131 more skills...]
└── README.md                # Main repository README
```

## Usage

Once installed, just ask Claude Code to help with supply chain tasks:

**"Help me optimize inventory levels for 500 SKUs"**
→ Uses inventory-optimization skill

**"Build a demand forecast model with seasonality"**
→ Uses demand-forecasting skill

**"Optimize delivery routes for 50 customers"**
→ Uses vehicle-routing-problem skill

**"Design a warehouse slotting strategy"**
→ Uses warehouse-slotting-optimization skill

**"Calculate optimal safety stock levels"**
→ Uses economic-order-quantity skill

## Example Usage

Once installed, your AI assistant will automatically apply these skills:

**Demand Forecasting:**
```
"Build a seasonal demand forecast model for our products"
→ Uses demand-forecasting skill with Holt-Winters, ARIMA, Prophet examples
```

**Vehicle Routing:**
```
"Optimize delivery routes for 50 customers with time windows"
→ Uses vrp-time-windows skill with Google OR-Tools implementation
```

**Warehouse Optimization:**
```
"Help me design optimal warehouse slotting using ABC analysis"
→ Uses warehouse-slotting-optimization skill with QAP formulation
```

**Inventory Management:**
```
"Calculate optimal safety stock and reorder points"
→ Uses inventory-optimization skill with service level calculations
```

## Supported Libraries

Skills leverage powerful Python libraries:
- **Optimization:** pulp, pyomo, ortools, cvxpy, scipy
- **ML/Forecasting:** scikit-learn, xgboost, prophet, statsmodels
- **Simulation:** simpy, networkx
- **Visualization:** matplotlib, seaborn, plotly

## Categories Covered

1. **Planning & Forecasting** - Demand forecasting, S&OP, capacity planning
2. **Inventory & Warehousing** - EOQ, safety stock, warehouse design
3. **Transportation & Logistics** - Routing, fleet management, last mile
4. **Procurement & Sourcing** - Supplier selection, strategic sourcing
5. **Manufacturing & Production** - Scheduling, lean, quality management
6. **Analytics & Technology** - ML, digital twins, optimization modeling
7. **Sustainability & Risk** - Carbon tracking, circular economy, SCRM
8. **Vertical Industries** - Retail, CPG, energy, healthcare, manufacturing

## Who Should Use This?

- Supply Chain Managers
- Operations Research Analysts
- Data Scientists working on supply chain problems
- Logistics Engineers
- Inventory Planners
- Manufacturing Engineers
- Procurement Professionals
- Students & Researchers

## Version

- **Version:** 1.1.0
- **Total Skills:** 133
- **Last Updated:** August 2026

## License

MIT License - Free for commercial and personal use

## Support

- **Repository:** https://github.com/kishorkukreja/awesome-supply-chain
- **Issues:** Report problems via GitHub Issues
- **Discussions:** Share use cases and ask questions

## Related Resources

See the main [README.md](../README.md) for:
- Complete list of all 133 skills
- Detailed skill descriptions and triggers
- Learning paths by experience level
- Contributing guidelines
