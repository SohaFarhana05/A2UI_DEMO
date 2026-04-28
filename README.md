# A2UI_DEMO

A demo repository for running the [google/A2UI](https://github.com/google/A2UI) research agent — an open standard that lets AI agents generate rich, interactive UIs via declarative JSON.

## Quick Start in GitHub Codespaces

1. Click **Code → Codespaces → Create codespace on main** in this repository.
2. Once the codespace is ready, set your Gemini API key:
   ```bash
   export GEMINI_API_KEY="your_gemini_api_key"
   ```
   Get a free key at [Google AI Studio](https://aistudio.google.com/apikey).
3. Run the Restaurant Finder demo (agent + web client in one command):
   ```bash
   cd A2UI/samples/client/lit
   npm run demo:restaurant
   ```
4. The web app will open at `http://localhost:5173`. Try prompts like:
   - *"Book a table for 2"*
   - *"Find Italian restaurants near me"*

## Running Other Agents

The A2UI repository includes several sample agents under `A2UI/samples/agent/adk/`:

| Agent | Description |
|---|---|
| `restaurant_finder` | Book restaurant tables via a dynamic form UI |
| `personalized_learning` | Adaptive learning experience with OpenStax content |
| `rizzcharts` | Data visualization charts |
| `orchestrator` | Multi-agent orchestration demo |

To run any agent manually:
```bash
# Terminal 1 — start the agent
cd A2UI/samples/agent/adk/<agent_name>
uv run .

# Terminal 2 — start the web client
cd A2UI/samples/client/lit/shell
npm run dev
```

## Requirements

- **GEMINI_API_KEY** — set as a Codespace secret or environment variable
- Python 3.13+ (pre-installed in the codespace via `uv`)
- Node.js 20+ (pre-installed in the codespace)

## Setting GEMINI_API_KEY as a Codespace Secret

For persistent access without re-exporting on every session:

1. Go to **github.com → Settings → Codespaces → Secrets**
2. Add a secret named `GEMINI_API_KEY` and set it to your key
3. Grant access to this repository