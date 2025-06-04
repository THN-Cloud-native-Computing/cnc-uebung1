# Übung 1 - Workload Analysis

**Aufgabe 0 - Aufwärmübung mit der Kommandozeile**

Im cloud-nativen Umfeld arbeitet man häufig mit der Kommandozeile. Deshalb machen wir eine kurze Aufwärmübung dazu. Erledigen Sie folgende Aufgaben ausschließlich über die Kommandozeile:

a) Öffnen Sie ein Terminal  
b) Lassen Sie sich den absoluten Pfad des Verzeichnisses anzeigen, in dem Sie gerade arbeiten  
c) Wechseln Sie in ein Verzeichnis ihrer Wahl  
d) Gehen Sie ein Verzeichnis nach oben im Verzeichnispfad  
e) Gehen Sie ein Verzeichnis nach unten im Verzeichnispfad  
f) Legen Sie dort ein Verzeichnis namens CloudComputing an  
g) Legen Sie in diesem Verzeichnis eine Datei namens server.log an  
h) Lassen Sie sich alle Dateien im Verzeichnis CloudComputing anzeigen  
i) Löschen Sie die Datei server.log  
j) Löschen Sie das Verzeichnis CloudComputing (oder behalten Sie es, um dort alle weiteren Materialen zur Vorlesung und zu den Übungen abzulegen)  
k) Lassen Sie sich alle Prozesse anzeigen, die gerade laufen  
l) Beenden Sie ihren Terminal-Prozess  


**Aufgabe 1 - Repository Klonen**

Um Repositories zu klonen, sollten Sie zunächst [git](https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren) installieren (das geht auch über die Kommandozeile). Sie können dann dieses Repository klonen mit:

   ```bash
git clone https://github.com/THN-Cloud-native-Computing/cnc-uebung1
   ```
Anmerkung: Mit den Repositories zu den weiteren Übungen können Sie genauso verfahren.

**Aufgabe 2 – Workload-Analyse**

Hinweis: Die Theorie und praktischen Übungen zu den Aufgaben 2 bis 5 sind (in ähnlicher Weise) zu finden in Nane Kratzke, Cloud-Native
Computing, Hanser Verlag, 2022, [Cloud-native Computing](https://cloud-native-computing.de) 

In der zu dieser Übung bereitgestellten Excel-Tabelle Demands.xlsx sind 7 Services mit ihren Demands (im zeitlichen Verlauf von oben nach unten in der jeweiligen Spalte) dargestellt. Pro Zelle ist die Anzahl der Ressourceneinheiten (vCPUs) angegeben, welche pro Zeiteinheit (Stunde) genutzt werden.
Stellen Sie die Services jeweils grafisch dar und ordnen Sie sie dem jeweiligen Workload-Typ aus der Vorlesung zu.

**Aufgabe 3 – Peak-to-Average-Ratio**

Berechnen Sie für jeden Service aus Übung 1 das Peak-to-Average $\frac{p}{a}$ Ratio mit   

$p = max(D(t))$  für  $0 < t \leq T$

$a = \frac{1}{T} \displaystyle\sum_{t=1}^{T} D(t) $  

wobei  

$D(t)$ : Anzahl der Demands pro Zeiteinheit $t$
$T$ : Gesamtzeit

**Aufgabe 4 – Cloud-Kosten und das Peak-to-Average-Ratio**

Im Folgenden werden die Kosten (in €) einer vCPU für eine Cloud-Ressource c und eine On-premise-Ressource d betrachtet. Bestimmen Sie für die folgenden Kostenverhältnisse, welcher der Services sich für eine Cloud-Lösung eignet:

| Nr.  | c  | d  |
|:----------|:----------|:----------|
| a)    | 1,0    | 1,0    |
| b)    | 1,5    | 1,0   |
| c)    | 1,7    | 1,0   |
| d)    | 2,0    | 1,0   |
| e)    | 1,0    | 1,01   |
| f)    | 1,0    | 2,0   |
| g)    | 5,0    | 1,0    |
| h)    | 19,0    | 1,0    |
| i)    | 20,0    | 1,0    |



**Aufgabe 5 – Kosten für IaaS, PaaS und SaaS**

Wir betrachten nun den Fall, dass wir die Services aus Übung 1 entweder On-Premise betreiben, oder durch eine IaaS, PaaS oder SaaS Lösung (mit unterschiedlichen Kosten) realisieren. Für die On-Premise-Lösung seien Kosten von 1€ pro Ressource und Zeiteinheit angenommen. In der folgenden Tabelle sind Kosten-Staffelungen der IaaS-, PaaS- und SaaS-Dienste verschiedener Anbieter gelistet. Welcher Service wäre in welcher Variante bei welchem Anbieter am wirtschaftlichsten?

| Anbieter  | c(IaaS)  | c(PaaS)  | c(SaaS)  |
|:----------|:----------|:----------|:----------|
| 1    | 1,0    | 2,0    | 3,0   |
| 2    | 3,0    | 5,0    | 7,0    |
| 3    | 1,0    | 1,1    | 1,2    |
| 4    | 1,0    | 1,3    | 1,8    |
| 5    | 0,8    | 1,1    | 1,2    |
| 6    | 0,8    | 0,9    | 1,1    |


