+++
authors = ["Jonas Steinhauser"]
title = "YOLO-basierte Objekterkennung"
date = "2025-02-24"
description = "Dieser Artikel behandelt die Fusion von Sensordaten zur Objekterkennung und -lokalisierung in Innenräumen. Aufbauend auf früheren Arbeiten an der RWU, die YOLOv7 und YOLOv8 auf dem YCB-Datensatz benchmarkten, erweitere ich die Analyse auf YOLOv9."
tags = [
"Scientific Project",
]
+++

# Servus 👋  

Aktuell beschäftige ich mich mit **Sensordatenfusion für die Objekterkennung und -lokalisierung in Innenräumen**. In diesem Blog dokumentiere ich meine Arbeit, Fortschritte und Herausforderungen.  

## Was ist YOLO?  

YOLO (**You Only Look Once**) ist eines der bekanntesten Algorithmen für Echtzeit-Objekterkennung. Im Gegensatz zu klassischen Methoden analysiert YOLO ein Bild nicht schrittweise, sondern verarbeitet es in einem einzigen Durchlauf durch ein neuronales Netzwerk. Das macht es extrem schnell und effizient – ideal für Robotik, autonome Systeme und Überwachung.  

Die neuesten Versionen, wie **YOLOv11**, bieten verbesserte Präzision, Geschwindigkeit und Anpassungsfähigkeit, was sie besonders interessant für **Sensordatenfusion und Innenraumlokalisierung** macht. Falls du tiefer in das Thema eintauchen möchtest, schau dir diesen Artikel an: [Roboflow Guide zu YOLO-Modellen](https://blog.roboflow.com/guide-to-yolo-models/).  

## Benchmarking von YOLO auf dem YCB-Datensatz  

An der RWU wurde bereits ein Vergleich von **YOLOv7 und YOLOv8** auf dem **YCB-Datensatz** durchgeführt. Der Datensatz umfasst 77 Alltagsgegenstände, die oft in der Robotik verwendet werden. Ziel war es, die beiden Modelle hinsichtlich Effizienz und Genauigkeit zu bewerten[^1].  

### Wichtige Erkenntnisse:  

- **Datensatz & Training:** Die Studie nutzte die **YCB-Video- und YCB-M-Datensätze** mit 21 Objekten und führte zusätzlich das neue **Robot Domain Dataset (RDD)** mit 259 Bildern aus realistischen Umgebungen ein.  
- **Bewertungsmetriken:** Die Leistung wurde anhand der **MS COCO-Metrik (AP@[.5:.05:.95], mAP50, mAP75)** gemessen.  
- **Ergebnisse:**  
  - **YOLOv8** schnitt auf den **YCB-M- und YCB-Video-Datensätzen** besser oder gleich gut wie **YOLOv7** ab.  
  - **YOLOv7** war auf dem **RDD-Datensatz** überlegen und konnte sich besser an neue Umgebungen mit variierenden Hintergründen und Lichtbedingungen anpassen.  
- **Fazit:** **YOLOv8** eignet sich gut für bekannte Datensätze, aber **YOLOv7** ist robuster in neuen Szenarien. Das macht es für reale Robotik-Anwendungen besonders spannend.  

Mein aktuelles Projekt baut auf dieser Forschung auf, wobei ich **YOLOv9** in das System integriere. Der nächste Schritt ist die Optimierung der Sensordatenfusion, um die Genauigkeit der Objekterkennung und -lokalisierung weiter zu verbessern.  

Ich freu mich, meine Fortschritte hier zu teilen. Bis bald!  

**Servus 👋**  

*Jonas*  

[^1]: Samuel Hafner, Markus Schneider, Benjamin Stähle (2024). *Performance Comparison of YOLOv7 and YOLOv8 Using the YCB Datasets YCB-M and YCB-Video*. EasyChair Preprint 13111, Version 2. [https://easychair.org/publications/preprint/c3GK](https://easychair.org/publications/preprint/c3GK)
