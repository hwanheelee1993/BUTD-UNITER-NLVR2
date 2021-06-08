This fork of bottom-up-attention is used to support feature extraction of faster-rcnn, which can be used through the pre-built [Docker image](https://hub.docker.com/repository/docker/chenrocks/butd-caffe) `chenrocks/butd-caffe:nlvr2`.

### Running Docker
    bash scripts/extract_imgfeat.sh $PATH_TO_IMG_FOLDER $PATH_TO_IMG_NPY
    
### Extracting Feature

    Modify line 42-43 in 'tools/generate_npz.py' as follows.
    line 42 MIN_BOXES = 100 -> MIN_BOXES = 36
    line 43 MAX_BOXES = 100 -> MAX_BOXES = 36

    ```
    python tools/generate_npz.py --def models/vg/ResNet-101/faster_rcnn_end2end_final/test.prototxt --cfg experiments/cfgs/faster_rcnn_end2end_resnet.yml --out /output/ --net 
    data/faster_rcnn_models/resnet101_faster_rcnn_final.caffemodel --prefix butd
    
    ```
    The output files will be stored in $PATH_TO_IMG_NPY as follows.
    sample.jpg -> butd_sample.npz

    


