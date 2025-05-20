# PyTorch Out-of-tree Accelerator TestInfra

Welcome! This repository is designed to facilitate the integration testing of 
different accelerators with PyTorch. Our primary focus is to ensure seamless 
integration and compatibility across various devices by running comprehensive 
GitHub workflows.

## Accelerator Integration Test Results

<details>

<summary>Click here to view the torchbenchmark report</summary>

<!-- Torchbenchmark start -->

|                                 | npu   |
|---------------------------------|-------|
| alexnet                         | ✅    |
| Background_Matting              | ✅    |
| basic_gnn_edgecnn               | ✅    |
| basic_gnn_gcn                   | ✅    |
| basic_gnn_gin                   | ✅    |
| basic_gnn_sage                  | ✅    |
| BERT_pytorch                    | ✅    |
| cm3leon_generate                | ✅    |
| dcgan                           | ✅    |
| demucs                          | ✅    |
| densenet121                     | ✅    |
| detectron2_fasterrcnn_r_101_c4  | ✅    |
| detectron2_fasterrcnn_r_101_dc5 | ✅    |
| detectron2_fasterrcnn_r_101_fpn | ✅    |
| detectron2_fasterrcnn_r_50_c4   | ✅    |
| detectron2_fasterrcnn_r_50_dc5  | ✅    |
| detectron2_fasterrcnn_r_50_fpn  | ✅    |
| detectron2_fcos_r_50_fpn        | ✅    |
| detectron2_maskrcnn             | ✅    |
| detectron2_maskrcnn_r_101_c4    | ✅    |
| detectron2_maskrcnn_r_101_fpn   | ✅    |
| detectron2_maskrcnn_r_50_c4     | ✅    |
| detectron2_maskrcnn_r_50_fpn    | ✅    |
| dlrm                            | ✅    |
| doctr_det_predictor             | ❌    |
| doctr_reco_predictor            | ❌    |
| drq                             | ✅    |
| fastNLP_Bert                    | ✅    |
| functorch_dp_cifar10            | ✅    |
| functorch_maml_omniglot         | ✅    |
| hf_Albert                       | ✅    |
| hf_Bart                         | ✅    |
| hf_Bert                         | ✅    |
| hf_Bert_large                   | ✅    |
| hf_BigBird                      | ✅    |
| hf_clip                         | ✅    |
| hf_distil_whisper               | ✅    |
| hf_DistilBert                   | ✅    |
| hf_GPT2                         | ✅    |
| hf_GPT2_large                   | ✅    |
| hf_Longformer                   | ✅    |
| hf_Reformer                     | ❌    |
| hf_Roberta_base                 | ✅    |
| hf_T5                           | ✅    |
| hf_T5_base                      | ✅    |
| hf_T5_generate                  | ✅    |
| hf_T5_large                     | ✅    |
| hf_Whisper                      | ✅    |
| LearningToPaint                 | ✅    |
| lennard_jones                   | ✅    |
| llama                           | ✅    |
| llama_v2_7b_16h                 | ❌    |
| llava                           | ❌    |
| maml                            | ❌    |
| maml_omniglot                   | ✅    |
| microbench_unbacked_tolist_sum  | ✅    |
| mnasnet1_0                      | ✅    |
| mobilenet_v2                    | ✅    |
| mobilenet_v2_quantized_qat      | ❌    |
| mobilenet_v3_large              | ✅    |
| moco                            | ❌    |
| moondream                       | ❌    |
| nanogpt                         | ✅    |
| nvidia_deeprecommender          | ❌    |
| opacus_cifar10                  | ✅    |
| phlippe_densenet                | ✅    |
| phlippe_resnet                  | ✅    |
| pyhpc_equation_of_state         | ✅    |
| pyhpc_isoneutral_mixing         | ✅    |
| pyhpc_turbulent_kinetic_energy  | ✅    |
| pytorch_CycleGAN_and_pix2pix    | ✅    |
| pytorch_stargan                 | ✅    |
| pytorch_unet                    | ✅    |
| resnet152                       | ✅    |
| resnet18                        | ✅    |
| resnet50                        | ✅    |
| resnet50_quantized_qat          | ❌    |
| resnext50_32x4d                 | ✅    |
| sam                             | ✅    |
| sam_fast                        | ❌    |
| shufflenet_v2_x1_0              | ✅    |
| simple_gpt                      | ❌    |
| simple_gpt_tp_manual            | ❌    |
| soft_actor_critic               | ✅    |
| speech_transformer              | ✅    |
| squeezenet1_1                   | ✅    |
| stable_diffusion_text_encoder   | ❌    |
| stable_diffusion_unet           | ❌    |
| Super_SloMo                     | ✅    |
| tacotron2                       | ❌    |
| timm_efficientdet               | ❌    |
| timm_efficientnet               | ✅    |
| timm_nfnet                      | ✅    |
| timm_regnet                     | ✅    |
| timm_resnest                    | ✅    |
| timm_vision_transformer         | ✅    |
| timm_vision_transformer_large   | ✅    |
| timm_vovnet                     | ✅    |
| torch_multimodal_clip           | ❌    |
| tts_angular                     | ✅    |
| vgg16                           | ✅    |
| vision_maskrcnn                 | ❌    |
| yolov3                          | ❌    |

<!-- Torchbenchmark end -->

</details>

## Overview

This repository contains workflows and scripts that automate the testing
process for integrating different hardware devices with PyTorch. The tests aim
to validate that PyTorch's device-specific functionalities are working
correctly and efficiently across different platforms.

### Key Features

- **Automated Integration Tests**: Run tests automatically for different devices using GitHub Actions.
- **Reusable Workflows**: Leverage modular and reusable workflows to streamline the testing process.

## Usage

### Running Tests

To run the integration tests, the repository leverages GitHub Actions.
You can trigger the tests by pushing code to the repository or by manually
triggering the workflows.

### Customizing Workflows

For customize your own workflows, here are some reference configuration in [workflow](https://github.com/pytorch-fdn/oota/tree/main/.github/workflows).

## Contributing

We welcome contributions to enhance the integration testing process. Feel free
to submit issues, pull requests, or suggestions to help us improve the
compatibility and performance of PyTorch on various devices. See the 
[CONTRIBUTING](CONTRIBUTING.md) for more details.

### Reporting Issues

If you encounter any issues while using the workflows or integrating a device,
please report them via the [Issues](https://github.com/pytorch-fdn/oota/issues) tab.

## License

This project is licensed under Apache-2.0 license. See the [LICENSE](LICENSE)
file for more details.
