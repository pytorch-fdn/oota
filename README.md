# PyTorch Accelerator Integration

This repository is dedicated to improving and streamlining the integration of diverse AI hardware accelerators with PyTorch. It supports the efforts of the Accelerator Integration Working Group to reduce integration complexity, enhance the integration mechanism, and establish reliable CI infrastructure for out-of-tree accelerators. The goal is to build a scalable and inclusive PyTorch hardware ecosystem. 

## Working Group Members

*All names below are arranged in alphabetical order; sequence carries no priority or seniority.*

### Co-Chairs

- Guangye Yu ([@guangyey](https://github.com/guangyey))
- Zesheng Zong ([@zeshengzong](https://github.com/zeshengzong))

### Voting Members

- Alban Desmaison ([@alband](https://github.com/alband))
- Guangye Yu ([@guangyey](https://github.com/guangyey))
- Zesheng Zong ([@zeshengzong](https://github.com/zeshengzong))

## Accelerator Integration Guide

New hardware accelerators can integrate with PyTorch using the shared dispatch key [PrivateUse1](https://docs.pytorch.org/tutorials/advanced/privateuseone.html). We're currently working on a comprehensive guide to help developers connect their custom hardware to PyTorch. This guide will include step-by-step instructions and practical examples based on the [OpenReg](https://github.com/pytorch/pytorch/tree/main/test/cpp_extensions/open_registration_extension/torch_openreg) reference implementation. For more details, refer to the related [RFC](https://github.com/pytorch/rfcs/blob/f6048cbd4fcc7877de6b049f96c0b9dece74cbd8/RFC-0045-PyTorch-Accelerator-Integration-Enhancements.md).

This effort is actively in progress. You can follow related discussions and open issues labeled [OpenReg](https://github.com/pytorch-fdn/accelerator-integration-wg/issues?q=is%3Aissue%20state%3Aopen%20label%3AOpenReg). Community contributions are highly encouraged and welcome.

## Accelerator Integration Tests

This repository contains workflows and scripts that automate the testing process for integrating different hardware devices with PyTorch. The tests aim to validate that PyTorch's device-specific functionalities are working correctly and efficiently across different platforms.

### Key Features

- **Automated Integration Tests**: Run tests automatically for different devices using GitHub Actions.
- **Reusable Workflows**: Leverage modular and reusable workflows to streamline the testing process.

### Integration Test Results

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
| detectron2_fasterrcnn_r_101_c4  | ❌    |
| detectron2_fasterrcnn_r_101_dc5 | ❌    |
| detectron2_fasterrcnn_r_101_fpn | ❌    |
| detectron2_fasterrcnn_r_50_c4   | ❌    |
| detectron2_fasterrcnn_r_50_dc5  | ❌    |
| detectron2_fasterrcnn_r_50_fpn  | ❌    |
| detectron2_fcos_r_50_fpn        | ❌    |
| detectron2_maskrcnn             | ❌    |
| detectron2_maskrcnn_r_101_c4    | ❌    |
| detectron2_maskrcnn_r_101_fpn   | ❌    |
| detectron2_maskrcnn_r_50_c4     | ❌    |
| detectron2_maskrcnn_r_50_fpn    | ❌    |
| dlrm                            | ✅    |
| doctr_det_predictor             | ✅    |
| doctr_reco_predictor            | ✅    |
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
| maml                            | ✅    |
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
| torch_multimodal_clip           | ✅    |
| tts_angular                     | ✅    |
| vgg16                           | ✅    |
| vision_maskrcnn                 | ❌    |
| yolov3                          | ✅    |

<!-- Torchbenchmark end -->

</details>


## Contributing

We welcome contributions to all aspects of the PyTorch accelerator integration mechanism — including APIs, tooling, CI infrastructure, documentation, and device support.

You can explore open tasks and priorities on our [project dashboard](https://github.com/orgs/pytorch-fdn/projects/13/views/2), and look for issues labeled `help wanted` to get started. Feel free to submit issues, pull requests, or suggestions to help us build a more flexible and scalable hardware integration ecosystem. See the [CONTRIBUTING](CONTRIBUTING.md) guide for details.

Stay connected:

* **Slack channel**: `#tac-accelerator-integration-wg` on the [PyTorch Slack](https://pytorch.slack.com/)
* **Participate working group meeting**: [Meeting Notes](https://docs.google.com/document/d/10G2fib_76CV4TCf47S-r6R6sg845-ty_ujur_giMNMI)


### Reporting Issues

If you encounter any issues while using the workflows or integrating a device,
please report them via the [Issues](https://github.com/pytorch-fdn/accelerator-integration-wg/issues) tab.

## License

This project is licensed under Apache-2.0 license. See the [LICENSE](LICENSE)
file for more details.
