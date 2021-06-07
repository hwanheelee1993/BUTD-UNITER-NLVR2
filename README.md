This fork of bottom-up-attention is used to support feature extraction of faster-rcnn, which can be used through the pre-built [Docker image](https://hub.docker.com/repository/docker/chenrocks/butd-caffe) `chenrocks/butd-caffe:nlvr2`.

### Running Docker



### Extracting Feature

    Modifying 
    
    ```
    ./tools/generate_npz.py --def models/vg/ResNet-101/faster_rcnn_end2end_final/test.prototxt --cfg experiments/cfgs/faster_rcnn_end2end_resnet.yml --out /output/ --net 
    data/faster_rcnn_models/resnet101_faster_rcnn_final.caffemodel --prefix butd
    
    ```

    


