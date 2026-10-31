# jac_qwen_chat

My qwen bot

# Ollama environment setup

Use these instructions with an AI assistant to set up Ollama for building with open models. Ollama can run models locally or in its cloud. Local performance depends on the computer's hardware; cloud models run on Ollama's servers and may require usage credits or a paid plan.

## Instructions for the assistant

Before making changes, read the [Ollama documentation index](https://docs.ollama.com/llms.txt), [quickstart](https://docs.ollama.com/quickstart.md), [cloud documentation](https://docs.ollama.com/cloud.md), and [hardware support](https://docs.ollama.com/gpu.md).

If building an application that calls Ollama, also read the [API introduction](https://docs.ollama.com/api/introduction.md). If the project uses an OpenAI or Anthropic SDK, read the corresponding [OpenAI compatibility](https://docs.ollama.com/api/openai-compatibility.md) or [Anthropic compatibility](https://docs.ollama.com/api/anthropic-compatibility.md) documentation. For other questions, search the [full documentation](https://docs.ollama.com/llms-full.txt).

1. Check whether Ollama is installed. If it is not, follow the current official installation instructions for the operating system: [Windows](https://docs.ollama.com/windows), [macOS](https://ollama.com/download), or [Linux](https://docs.ollama.com/linux).
2. Check the computer's GPU and memory against the hardware documentation.
3. Ask the person what they want to build.
4. Recommend suitable local models, cloud models, or both, and explain the choice. Consider speed, available memory, privacy, and cost.
5. Help verify that the selected model works before proceeding to application or agent setup.

Do not sign in, create an API key, or use an API key on the person's behalf. If they choose cloud models, tell them to run `ollama signin` or create a key at [Ollama API keys](https://ollama.com/settings/keys). Never place keys in source control.

Local models run on the person's computer. Cloud models run on Ollama's servers; the CLI uses names ending in `:cloud`. Consult the cloud documentation for the current model names and API details.


## Example local agent

The [local agent instructions](examples/local-agent/AGENTS.md) define a simple project helper. To try them, download or clone this repository to your computer, open PowerShell in the `examples/local-agent` folder, and run `ollama launch codex`. Select a local model such as `qwen3.5:9b` if available. Codex CLI must be installed; see [Ollama's Codex guide](https://docs.ollama.com/integrations/codex).

Try asking: “Read AGENTS.md, create a short hello.md introducing this project, and explain what you did.” The model runs locally when the local Ollama model is selected. GitHub stores the instructions; running an agent still requires a local copy of the folder.
