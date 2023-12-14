# About Dataset

A temporary repo for the P2ANET dataset. P2ANET dataset is proposed in the following paper. 

Bian, Jiang, Xuhong Li, Tao Wang, Qingzhong Wang, Jun Huang, Chen Liu, Jun Zhao, Feixiang Lu, Dejing Dou, and Haoyi Xiong. "P2ANet: A Large-Scale Benchmark for Dense Action Detection from Table Tennis Match Broadcasting Videos." ACM Transactions on Multimedia Computing, Communications and Applications (2023). [PDF](https://dl.acm.org/doi/pdf/10.1145/3633516) [arXiv](https://arxiv.org/abs/2209.08716)

## About Data collection methodology

<!--This description gives a detailed process on how the data was collected. It should describe the conditions under which the data was recorded and also the devices used to record the data.-->
The video data is captured by an RGB monocular camera, and the label data is obtained by manual annotation.

### Description of the data

<!--Here you can descibe how the data is organized in this whole dataset. How the data is stored in all the files. You also have to brief about the naming convention of the files in different directories. -->
There are two identical datasets: the original dataset and the processed dataset. The original dataset is obtained from two data collections, called v1 and v2. The processed dataset summarizes these two batches of extracted frames with labels.

```
P2A_dataset/
    -dataset/
        -video/
            -v1/
                -0000000.mp4
                -0000001.mp4
                -...
            -v2/
                -0000000.mp4
                -0000001.mp4
                -...
        -label/
            -v1.json
            -v2.json
        -proj.json # Contains the mapping relationship between the original video name and the id name
```

## Online Repository link

* [Baidu Wangpan](https://pan.baidu.com/s/11YT1P8UyronKKxodhsRqoQ)  KEY: please apply the KEY via email (bj911125@outlook.com).

## Citation

```
@article{bian2023p2anet,
  title={P2ANet: A Large-Scale Benchmark for Dense Action Detection from Table Tennis Match Broadcasting Videos},
  author={Bian, Jiang and Li, Xuhong and Wang, Tao and Wang, Qingzhong and Huang, Jun and Liu, Chen and Zhao, Jun and Lu, Feixiang and Dou, Dejing and Xiong, Haoyi},
  journal={ACM Transactions on Multimedia Computing, Communications and Applications},
  year={2023},
  publisher={ACM New York, NY}
}
```

## License

This project is licensed under the MIT License.
