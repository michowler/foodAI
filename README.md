# Food Waste or Trash Image Classification
trash or food waste? with Tensorflow

# Prerequisites: 
> - Tensorflow installed
> - Python 3.6.x 
```
$ export PYTHONPATH="/usr/local/Cellar/python/3.6.6/bin/python3:$PYTHONPATH”
```
> - 2 image folders (e.g. food waste and trash), you can download them using FatKun Chrome extension

# Steps:
1. Base on the steps using Tensorflow for Poets on Codelab, you should be able to install Tensorflow
2. Activate your virtual environment and get started on the [tutorial](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/)

```
$ source ./venv/bin/activate
```

3. Add your image folder (e.g food_waste) containing two folders (trash and food waste/food) into tf_files. 
- tf_files/food_waste/food
- tf_files/food_waste/trash

4. Train your model with 4000 steps instead of 500!
```
$ python retrain.py --model_dir ./inception --image_dir ~/food_waste --output_graph ./output --how_many_training_steps 4000

```

5. Test your model with an image you'd like by altering the last line, image_dir to the path of your image!

```
$ python -m scripts.retrain \
  --bottleneck_dir=tf_files/bottlenecks \
  --model_dir=tf_files/models/ \
  --summaries_dir=tf_files/training_summaries/"${ARCHITECTURE}" \
  --output_graph=tf_files/retrained_graph.pb \
  --output_labels=tf_files/retrained_labels.txt \
  --architecture="${ARCHITECTURE}" \
  --image_dir=tf_files/food_waste/image1
```


# Outcome example

- Trash (0.98249)
- Food (0.01751)
