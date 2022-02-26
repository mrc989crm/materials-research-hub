<img src="https://user-images.githubusercontent.com/95081818/155694682-66596058-45d0-4e76-b51c-e3be46fc978c.png" width=40%>

This repository contains jupyter notebooks for (i) classifying electron microscopy images of bainitic steels, (ii) training costumized models of the detection and segmentation library [detectron2](https://github.com/facebookresearch/detectron2) and (iii) testing them. The models are trained to identify and segment Martensite-Austenite (M-A) islands in scanning electron microscopy images of a bainitic steel after various cooling strategies. The resulting microstructures show distinct characteristics seperated into sub-datasets I,II and III. On each sub-dataset, models were trained and tested.  

<img width="500" alt="Screenshot 2022-02-24 111803" src="https://user-images.githubusercontent.com/95081818/155505240-80a75f7c-11fe-46a0-9a32-f57d90784ddc.png">

trained-models.md provides further information how to get trained segmentation models. Models can be used for predictions on new images of bainitic microstructures (the selected models should match the size of the image, e.g. "512x_i_model", "512x_ii_model", "512x_iii_model" are suitable for 512x512 images). 

The original reference size of the images (1536x2048) was cropped into specific sizes (64x,128x,256,512x,768x). Image data and labels are available in figshare:
https://figshare.com/articles/dataset/Image_data_and_labels/19232523

Training and testing of models followed the following structure in drive: <br />
![schema git_resize](https://user-images.githubusercontent.com/95081818/155836175-913b6c48-4165-416a-aadd-1903419d8161.png) <br />
Images in 'im_train' and 'im_val', labels (train.json, val.json) in 'label' and models in the output folder should match with the corresponding cropping size (1536x,768x,512x,256x,128x,64x) and the sub-dataset number (i,ii,iii) which are associated with specific cooling regime of the steel.

