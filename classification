# Using Pandas in Python: Supervised or Unsuperviesed Learning?
#Read CSV(Very Important Starting Point!!)
#You need to mark the correct directory before reading the file
#option 1: use pandas library
import pandas as pd
pd.read_csv("train.csv")
#option 2: use csv library
import csv
with open("train.csv") as csvfile:
    readCSV = csv.reader(csvfile, delimiter = ",")
    print(read CSV)
    #https://www.kaggle.com/go1dfish/clear-mask-visualization-and-simple-eda

import pandas as pd
from collections import defaultdict
import matplotlib.pyplot as plt
import seaborn as sns
from tqdm import tqdm
import os
from PIL import Image

train_df = pd.read_csv("/Users/yue/Desktop/BU Grad Courses/19fallEC601/TermProject/Raw_Data/severstal-steel-defect-detection/train.csv")
sample_df = pd.read_csv("/Users/yue/Desktop/BU Grad Courses/19fallEC601/TermProject/Raw_Data/severstal-steel-defect-detection/sample_submission.csv")
print(train_df.head())
print(sample_df.head())
#defaultdict: a modified dict to supply missing values for arbitrary keys
class_dict = defaultdict(int)
kind_class_dict = defaultdict(int)
no_defects_num = 0
defects_num = 0
for col in range(0, len(train_df), 4):
    img_names = [str(i).split("_")[0] for i in train_df.iloc[col:col + 4, 0].values]
    if not (img_names[0] == img_names[1] == img_names[2] == img_names[3]):
        raise ValueError
    labels = train_df.iloc[col:col + 4, 1]
    if labels.isna().all():
        no_defects_num += 1
    else:
        defects_num += 1
    kind_class_dict[sum(labels.isna().values == False)] += 1
    for idx, label in enumerate(labels.isna().values.tolist()):
        if label == False:
            class_dict[idx + 1] += 1
print("the number of images with no defects: {}".format(no_defects_num))
print("the number of images with defects: {}".format(defects_num))
#Checking the status of pip
#Need help in installing pyplot
#How to add many hashtage at one time?

fig, ax = plt.subplots()
sns.barplot(x=list(class_dict.keys()), y=list(class_dict.values()), ax=ax)
ax.set_title("the number of images for each class")
ax.set_xlabel("class")
plt.show()
#print(class_dict)

#How to define the Path and Image?
#What is the
#Path
#Image
# print(Path = sys.path())
# Path = os.getcwd()
# train_size_dict = defaultdict(int)
# train_path = Path
# for img_name in train_path.iterdir():
#     img = Image.open(img_name)
#     train_size_dict[img.size] += 1
# #train_size_dict
# test_size_dict = defaultdict(int)
# test_path = Path
# TestPath = "~/test-images"
# TrainingPath = "~/training-images"
# for img_name in test_path.iterdir():
#    img = Image.open(img_name)
#    test_size_dict[img.size] += 1
#test_size_dict

#How to define idx_no_defect
#for idx in idx_no_defect[:5]:
#    show_mask_image(idx)
#for idx in idx_class_1[:5]:
#    show_mask_image(idx)
#for idx in idx_class_2[:5]:
#    show_mask_image(idx)
#for idx in idx_class_3[:5]:
#    show_mask_image(idx)
#for idx in idx_class_4[:5]:
#    show_mask_image(idx)
#for idx in idx_class_multi[:5]:
#    show_mask_image(idx)
#for idx in idx_class_triple:
#    show_mask_image(idx)

#What is name_and_mask?
#how to manipulate the train.csv(does the R code give us some hitn?)
#for col in tqdm(range(0, len(train_df), 4)):
#    name, mask = name_and_mask(col)
#    if (mask.sum(axis=2) >= 2).any():
#        show_mask_image(col)

#https://www.kaggle.com/mullerismail/steel-defect-understand-plot-with-r-novice
read.csv("train.csv")
# too large for R
read.csv("sample_submission.csv")
list.files("/Users/yue/Desktop/BU Grad Courses/19fallEC601/TermProject/Raw_Data/severstal-steel-defect-detection/train_images")[1:5]
list.files("/Users/yue/Desktop/BU Grad Courses/19fallEC601/TermProject/Raw_Data/severstal-steel-defect-detection/test_images")[1:5]
library(tidyverse)
library(magrittr)
library(imager) ## something wrong with my package
path_to_image  <- list.files(path = "/Users/yue/Desktop/BU Grad Courses/19fallEC601/TermProject/Raw_Data/severstal-steel-defect-detection/train_images", 
                             pattern = ".jpg",recursive = TRUE, full.names=TRUE)[1]
path_to_image # 0002cc93b.jpg
image_to_plot <- imager::load.image(path_to_image)
print(image_to_plot)
str(image_to_plot)
plot(image_to_plot)
#for tayo: please continue

https://docs.google.com/document/d/13KuHDx7hyi4nFFSxomL6C1C6LTj8TZo1B8pDZjJ8XjQ/edit?usp=sharing
