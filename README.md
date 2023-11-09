# About Dataset

A temporary repo for the P2ANET dataset. \
P2ANET dataset is proposed in the paper "P2ANET: A Large-Scale Benchmark for Dense Action Detection from Table Tennis Match Broadcasting Videos". [Source]

## About Data collection methodology

<!--This description gives a detailed process on how the data was collected. It should describe the conditions under which the data was recorded and also the devices used to record the data.-->
The video data is captured by an RGB monocular camera, and the label data is obtained by manual annotation.

### Description of the data

<!--Here you can descibe how the data is organized in this whole dataset. How the data is stored in all the files. You also have to brief about the naming convention of the files in different directories. -->
There are two identical datasets: the original dataset and the processed dataset. The original dataset is obtained from two data collections, called v1 and v2. The processed dataset summarizes these two batches of extracted frames with labels.

```
P2A_dataset/
    -origin_dataset/
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
        
    -processed_dataset/
        -0000000.hdf5
        -0000001.hdf5
    -...
```
### The usage of processed_dataset.
```
import h5py
f = h5py.File('/bosfs/wangtao/TableTennis/0000033.hdf5', "r")
dset = f[[k for k in f.keys()][0]]

# extracted frames
print(dset.shape) 
(18, 1080, 1920, 3)

# label
print([(k,v) for k, v in dset.attrs.items()])
# [('end', 3189), ('name', '7月27日晚场2'), ('start', 3171), ('动作类型', 0), ('发球', 0), ('正反手', 0)]
```


<!--
### And file formats

If the data includes images or audio, you can mention the file format eg.(.svg, .png, .mpeg).
```
-500 images, format svg.
```
 -->
## Online Repository link

* [Baidu Wangpan](https://pan.baidu.com/s/11YT1P8UyronKKxodhsRqoQ)  KEY: P2AN

## License

This project is licensed under the MIT License.
