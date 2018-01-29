Tips when using Caffe
==========================

opencv2 matrix to caffe image

.. code-block:: py

  image = caffe.io.load_image (caffe_root +  'examples / images / cat.jpg' )  
  
  image1 = cv2.imread (caffe_root +  'examples / images / cat.jpg' )  
  image1 = cv2.cvtColor (image1, cv2.COLOR_BGR2RGB)  
  image1 = image1 / 255.  

  
