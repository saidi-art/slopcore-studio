# slopcore-studio

ACE-Step 1.5 production studio for the Sphere slopcore soundtrack line. Zero-bill setup: nothing in this stack touches Google Cloud billing.

## Run the studio (free Colab T4)

1. Open `studio/ace_step_colab_studio.ipynb` and upload it to Colab (File > Upload notebook). The same notebook lives in Google Drive as `ace_step_colab_studio.ipynb`.
2. Runtime > Change runtime type > T4 GPU > Save.
3. Run the cells top to bottom. Cell 2 clones the model fork (github.com/saidi-art/ACE-Step-1.5, MIT) and installs with uv. Cell 3 launches the studio and prints a public .gradio.live link; the first run downloads about 10 GB of weights (10-20 minutes).
4. Generate. Keep cell 3 running while you work.
5. When done: Runtime > Interrupt execution, or just disconnect. Nothing keeps running on its own.

## Why this costs nothing

- Colab free T4: Google's free tier. No GPU quota on the project is touched and nothing bills the Google Cloud account.
- This repo: GitHub free tier, private.
- Outputs: Google Drive, never git.

## Where outputs live

Generated tracks land in the Drive outputs folder, never in this repo (audio does not belong in git). Log every session in `sessions.md`: date, prompt, seed, output filename, verdict.

## Model notes

- Stay on the base model on T4: the XL upgrade wants 12-20 GB of VRAM.
- ACE-Step 1.5 weights are MIT, so commercial use of self-generated tracks is clean. Only ship tracks you generated yourself.

## License

Repo content: private to KubeAI. Upstream ACE-Step: MIT.
