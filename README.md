##RefCOCOg-Adv: A Referring Expresion Dataset

This folder contains adversarial annotations for part of the test images from [RefCOCOg dataset](http://bvisionweb1.cs.unc.edu/licheng/referit/data/refcocog.zip).


##Prepare Images:
Download "mscoco" into the ``Images`` folder, which can be from [mscoco](http://mscoco.org/dataset/#overview)
Bounding box annotations are also from mscoco dataset


##Dataset Summary:
- In RefCOCOg-adv dataset we have have 976 unique images from RefCOCOg test dataset. In total 3704 referring expressions were annotated with an average length of 11.3.

#Example Annotation of RefCOCOG-adv:
refcocog_adv_annotations.json contains a dict of advesarial referential expressions, where each annotation is

```
{
    'shuffle': 'to giraffes in hat next red white fence over shirt a a a two and woman leaning', 
    'hit_id': '3K3G488TR2FROXACUQOSDKLYTK65Q8', 
    'hit_type_id': '3QH037L2CMDD4RRYVNJWX0CT0B0AWC', 
    'adj_noun': 'giraffes white hat shirt woman next fence red', 
    'GT_bbox_number': '3', 
    'most_confused_bbox_GT_desc': 'A woman in a red shirt, feeding giraffes through a fence.', 
    'raw_str': 'two giraffes leaning over a fence next to a woman in a red shirt and white hat.', 
    'noun_adj': ' giraffes fence woman red shirt white', 
    'batch_id': 'batch18', 
    'bbox_candidates_map': '{"1": [373.0, 78.04, 266.56, 348.96], "2": [0.96, 0.24, 294.58, 398.21], "3": [62.37, 0.14, 329.79, 292.73], "4": [455.08, 177.19, 50.35, 235.29]}', 
    'adj': 'next red white', 
    'most_confused_bbox_number': '1', 
    'assigns': [{'dropdownselect': '2'}, {'dropdownselect': '1'}, {'dropdownselect': '1'}], 
    'must_words': 'giraffes,fence,woman,red,shirt,white', 
    'bbox_html_dropdown': "<option value='0'>Select the Box here</option> <option value='1'>1</option> <option value='2'>2</option> <option value='3'>3</option> <option value='4'>4</option> ", 
    'shuffle_pos': 'two shirt leaning over a fence white to a giraffes in a next woman red hat', 
    'refID': '64809', 
    'stage': 'stage3', 
    'noun': 'giraffes fence woman shirt hat', 
    'imgID': '254291', 
    'annID': '595839', 
    'img_file_name': 'COCO_train2014_000000254291.jpg'
}
```

#From the above example
```
shuffle, adj_noun, noun_adj, noun, must_words, shuffle_pos are paramters used to perturb data for our adversarial data creation
raw_str and GT_bbox_number are from RefCOCOg dataset
bbox_candidates: from mscoco
most_confused_bbox_GT_desc: from our annotation
```


## License

This library is licensed under the CC-BY-4.0 License.


