# Log

## 2026-11-03 (Setup)
- Evals:
    - Laid the groundwork for the next few months: installed Homebrew, git, the GitHub CLI, and Python, and linked git to my GitHub account
    - Created the finance-evals repo and cloned it to my Mac
    - Built a virtual environment (.venv) with Inspect, inspect_evals, the Anthropic and OpenAI libraries, and stats and plotting packages
    - Saved the package list to requirements.txt so I can rebuild the environment when I migrate to my desktop
    - Kept API keys and local files off my public GitHub with .gitignore
    - Ran my first eval: 3 GSM8K questions on Claude Haiku, 3/3 correct
- Kernels:
    - Connected Colab and Kaggle to free Tesla T4 GPUs and confirmed CUDA works. Colab is my main GPU, Kaggle is the backup
    - Created the cuda-kernels repo
    - Automated saving: Colab works inside a Google Drive copy of the repo and pushes to GitHub with a personal access token
    - Wrote and ran my first CUDA program (hello.cu, 2 blocks of 4 threads)
- Problems solved:
    - Python version mismatch: macOS shipped 3.9 (too old for Inspect) and Homebrew installed 3.15 (too new for one dependency), so I rebuilt everything on 3.13
    - API authentication: my first key was the key's ID, the second was account-level, and the fix was a workspace-scoped key
- Learned: environment and version problems take more time than the code itself, and error messages usually say exactly what's wrong