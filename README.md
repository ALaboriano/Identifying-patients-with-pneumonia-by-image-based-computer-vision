# Identificación de pacientes con neumonía mediante imágenes, utilizando técnicas de Visión Computacional

## Descripción
Se busca predecir que pacientes tienen neumonía, basados en imágenes de Rayos X del Tórax de pacientes que han sido diagnosticadas con neumonía severa y de pacientes que no han tenido neumonía severa, después de un diagnóstico médico realizado por expertos.  
Para ello se debe entrenar un modelo de visión computacional que tome como entrada una imagen de Rayos X del Tórax y determine si en la imagen hay o no presencia de neumonía.

## Preparación de datos.
Los datos provienen de 2 fuentes:
1. Archivos planos que contienen el id, el nombre y label de las imágenes.
2. Las imágenes de Rayos X del Torax de pacientes.

En el script `1.Preparacion de datos.ipynb`, se encuentra todo el proceso de preparación de los directorios de trabajo, desde las fuentes de las cuales se extrae la data, hasta un breve análisis exploratorio.

La estrategía de preparación de datos se presenta en la siguiente imágen.

![Fig1 Preparacion datos](https://user-images.githubusercontent.com/52020337/195968286-cdaeff15-d011-4958-9080-05048c7ea3f5.JPG)

## Experimentación.
En el scripts 2 y 3 se  encuentra todos los experimentos realizados, en los cuáles se aplicó estrategías de `Data Augmentation`, `Transfer Learning` y `Fine Tuning`, para mejorar el rendimiento de las diferentes arquitecturas entrenadas. 
Entre las arquitecturas que se probó están: `ResNet50`, `ResNet152V2`, `VGG16`, `VGG19`, `InceptionV3`, `InceptionResNetV2`.

## Resultados
Los mejores resultados se obtuvieron, con una `ResNet50` y las arquitecturas basadas en `VGG`, logrando un auc superior al 99% en la data de validación, en la mayoría de las arquitecturas probadas.
![Fig2 comparacion - auc](https://user-images.githubusercontent.com/52020337/195968351-dc42228d-a84c-4617-b5ff-bfd3da7c390c.JPG)

Para ver más a detalle los resultados, consultar el archivo `CNN-InClass Competition Kaggle.pptx`.

# repository
