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
2. Activate your virtual environment and get started on the tutorial!

```
$ source ./venv/bin/activate
```

3. Train your model!
```
python retrain.py --model_dir ./inception --image_dir ~/flowers --output_graph ./output --how_many_training_steps 500

```

4. Test your model!

```
python -m scripts.retrain \
  --bottleneck_dir=tf_files/bottlenecks \
  --model_dir=tf_files/models/ \
  --summaries_dir=tf_files/training_summaries/"${ARCHITECTURE}" \
  --output_graph=tf_files/retrained_graph.pb \
  --output_labels=tf_files/retrained_labels.txt \
  --architecture="${ARCHITECTURE}" \
  --image_dir=tf_files/food_waste/image1
```


