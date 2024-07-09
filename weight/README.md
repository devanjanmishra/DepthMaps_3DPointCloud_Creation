The weights are downloaded from offical [Metric3D Readme](https://github.com/YvanYin/Metric3D/blob/main/README.md). (subject to change in future)  

### Download Checkpoint
|      |       Encoder       |      Decoder      |                                               Link                                                |
|:----:|:-------------------:|:-----------------:|:-------------------------------------------------------------------------------------------------:|
| v1-T |    ConvNeXt-Tiny    | Hourglass-Decoder | [Download 🤗](https://huggingface.co/JUGGHM/Metric3D/blob/main/convtiny_hourglass_v1.pth)        |
| v1-L |   ConvNeXt-Large    | Hourglass-Decoder | [Download](https://drive.google.com/file/d/1KVINiBkVpJylx_6z1lAC7CQ4kmn-RJRN/view?usp=drive_link) |
| v2-S | DINO2reg-ViT-Small  |    RAFT-4iter     | [Download](https://drive.google.com/file/d/1YfmvXwpWmhLg3jSxnhT7LvY0yawlXcr_/view?usp=drive_link) |
| v2-L | DINO2reg-ViT-Large  |    RAFT-8iter     | [Download](https://drive.google.com/file/d/1eT2gG-kwsVzNy5nJrbm4KC-9DbNKyLnr/view?usp=drive_link) |
| v2-g | DINO2reg-ViT-giant2 |    RAFT-8iter     | [Download 🤗](https://huggingface.co/JUGGHM/Metric3D/blob/main/metric_depth_vit_giant2_800k.pth) |

Currently used models:
1) v1-L:ConvNeXt-Large encode with Hourglass-Decoder. For Preprocessing Image and camera model stacks.
2) v2-L:DINO2reg-ViT-Large encoder with RAFT-8iter decoder. For Depth and Normal Estimation.
