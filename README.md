# openassistant.cpp

Run a [pythia-based Open Assistant](https://huggingface.co/OpenAssistant/oasst-sft-1-pythia-12b) model locally on your cpu.
This is a combination of [ggml](https://github.com/ggerganov/ggml), and [cformers's](https://github.com/NolanoOrg/cformers) gpt-neox implementation, hacked together to provide a chat interface for Open Asisstant in pure c++.
This is not a serious project; it was hacked together, and is based on an old ggml version.  I created this because I wanted to test out open assistant locally.

## Running it:

Clone this repository, and run make.

Download the model: [oasst-sft-1-pythia-12b](https://huggingface.co/ayushk4/OpenAssistant-.-oasst-sft-1-pythia-12b/resolve/main/int4_fixed_zero.bin).

(The model is already quantized with 4 bit quantization)

Run it with: ```./main -m PATH_TO_MODEL```

## Notes

You could probably run a gpt-neox-20B-based open assistant model with this, but I haven't tested it.  And with some simple modifications, you could adapt this to run stuff like Dolly 2.0, stablelm, and other neox-like chat-tuned llms.  But if you are interested in any of this, I would recommend contributing to the [main](https://github.com/ggerganov/ggml) ggml repo.

If you are confused about how anything else in this repo works, refer to [cformers](https://github.com/NolanoOrg/cformers), as most of the code is shared.
