# enhancing-prediction-performance-by-introducing-structural-information
This repository includes four machine-learning predictive models of the processing-structure-property relationships of carbon black-reinforced rubber composites.

## File description

- P-S DNN.h5:

  DNN model for predicting CRC dispersion from processing features

- PSP DNN.h5:

  DNN model for predicting CRC properties obtained using feature fusion

- PSP max-DNN.h5：

  DNN model for predicting CRC properties obtained using feature fusion and experimental structural information

- PSP tf-DNN.h5：

  DNN model for predicting CRC properties obtained using transfer learning

## Dependencies

1. Install Anaconda <https://www.anaconda.com>
2. Create a virtual environment
3. Activate this virtual environment
4. Install [Tensorflow](https://www.tensorflow.org/get_started/os_setup), [Pandas](https://pandas.pydata.org/getting_started.html), [Numpy](https://numpy.org/install)

## Using
  An example:
  
 ```shell
  data = pd.read_csv('data.csv')
  model = tf.keras.models.load_model('P-S DNN.h5')
  predict_results = model.predict(data)
  ```
  Notice:
In actual use, the predicted values ​​of the DNN model need to be multiplied by 35(strength), 7(log-fatigue), 700(elongation), 5(D-low), 25(D-mid), 15(D-high) respectively.

## Cite
 If you use any of our data or code, partly or as it is, please cite our paper.
