# Drone Detection

## Інструмент розмітки

- Інструмент: [Label Studio](https://labelstud.io/)
- Тип розмітки: Об’єктна детекція (Bounding Boxes)
- Клас об'єкта: `drone`
- Шаблон розмітки (`label_config.xml`):

```xml
<View>
  <Image name="image" value="$image"/>
  <RectangleLabels name="label" toName="image">
    <Label value="drone" background="#ffcc00"/>
  </RectangleLabels>
</View>
```

## Додавання розміток 

```
dvc add data/yolo_annotations
git add data/yolo_annotations.dvc .gitignore
git commit -m "Add YOLO annotations for drone detection"
```
