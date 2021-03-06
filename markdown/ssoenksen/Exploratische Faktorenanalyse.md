- # Ziele von Faktorenanalysen
    1. Datenreduktion: Variation von Variablen wird auf geringere Zahl von gemeinsamen Dimensionen zurückgeführt / Itemanalyse
    2. Überprüfung der Konstruktvalidität von Fragebögen/ Tests
- Exploratische Faktorenanalyse: Hypothesengenerierend ([[Konfirmatorische Faktorenanalyse]]: Hypothesenprüfend)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fssoenksen%2FfNtCAfCK3f.png?alt=media&token=5eb72477-19ed-4f6a-9d35-866120759710)
- # Fundamentaltheorem der Faktorenanalyse 
    - **Auf Personenebene:** $$z_{vi} = \lambda_{i1} f_{1v} + \lambda_{i2} f_{2v} + ... + \lambda_{ik} f_{kv} + ... + \lambda_{iq} f_{qv} + \varepsilon_{vi} = \sum_{k=1}^{q} (\lambda_{ik} f_{kv}) + \varepsilon_{vi}$$
    - **Auf Itemebene:** $$z_i = \lambda_{i1} F_1 = \lambda_{i2} F_2 + ... + \lambda_{ik} F_k + ... + \lambda_{iq} F_q + \varepsilon_i = \sum_{k=1}^{q} (\lambda_{ik} F_k) + \varepsilon_i$$
    - $$Var(z_i) = 1,0 = \lambda^2_{i1} + \lambda^2_{i2} + ... + \lambda^2_{ik} + ... + \lambda^2_{iq} + Var(\varepsilon_i)$$
    - ($$v$$: Person; $$i$$: Item; $$k = 1, ..., q$$: Anzahl Faktorwerte ($$f$$); $$\lambda$$: Faktorladungen)
    - **Faktorladungen** $$\lambda = -1, ..., 1$$, interpretierbar als **Korrelationskoeffizient** zwischen $$z_vi$$ und $$f_{iv}$$ / **Zusammenhang** zwischen Faktor und Variable/ Item
    - ## Eigenwert eines Faktors
        - $$Eig(F_k) = \sum_{i=1}^{m} \lambda^2_{ik}$$ (__wie viel Varianz über alle Variablen/ Items erklärt ein Faktor?__)
        - $$Eig(F_k) > 1$$ --> Faktor erklärt mehr Varianz als die einer einzigen Variable, da $$s^2_{z_i} = 1$$, also Datenreduktion
    - ## Kommunalität einer Variable
        - $$h^2_i = \sum_{k=1}^{q} \lambda^2_{ik}$$ (__wie viel Varianz einer Variable wird durch alle Faktoren erklärt?__)
        - Da variablen standardisiert: Kommunalität bei PCA maximal 1, bei PFA maximal so groß wie Reliabilität
- # Extraktionsmethoden
    - Durch Datenreduktion entsteht in beiden Verfahren ein Fehlerterm, der Messfehler und systematische Varianz enthält
    - **Vorgaben**
        - Faktoren wechselseitig unabhängig voneinander
        - Faktoren klären sukzessiv maximale Varianz auf
    - ## Hauptkomponentenanalyse (principal components analysis, PCA)
        - Annahme: Variablen sind messfehlerfrei
        - Ziel: Erklärung maximaler Varianz der Variablen durch Hauptkomponenten (Faktoren) 
        - Varianz jeder standardisierten Variable = 1 --> Gesamtvarianz aller Variablen = Anzahl Variablen
        - Extraktion von weniger Faktoren als beobachtete Variablen --> Fehlerterm (__uniqueness__) entsteht
    - ## Hauptachsenanalyse (principal axes factor analysis, PFA; **Präferenz!**) 
        - Annahme: Variablen enthalten Messfehler
        - Ziel: Aufdeckung von Faktoren, mit denen Beziehungsmuster zwischen Variablen erklärt werden kann, unter Ausschluss der Messfehler
        - Schätzung der wahren Varianz der Variablen aufgrund quadrierter multipler Korrelation mit allen anderen Variablen --> Varianz jeder standardisierten Variable < 1
- # Abbruchkriterien zur Festlegung der Faktorenanzahl
    - Auf Basis des Eigenwerteverlaufs
    - ## Kaiser-Guttman-Kriterium
        - Faktoren mit $$Eig(F) > 1$$ ausgewählt, da mehr Varianz aufgeklärt wird als eine einzelne Variable aufweist
        - Probleme: Führt bei vielen Variablen zu Überschätzung der Faktorenanzahl; Eigenwerte nur Populationsschätzungen (keine Nutzung von Konfidenzintervallen)
    - ## Scree-Test
        - Darstellung des Eigenwerteverlaufs in Screeplot, Auswahl der Faktoren vor "Knick", ab dem sich Graph asymptotisch der Abszisse annähert
    - ## Parallelanalyse (**Präferenz** mit anschließendem Einbezug der beiden anderen Kriterien)
        - In Stichprobe treten oft Zufallskorrelationen auch bei orthogonalen Variablen auf
        - Durchführung
            1. Parallele Faktorenanalyse mit theoretischen Stichproben, die Korrelationen aufweisen aber in Population unkorreliert sind
            2. Darstellung in Scree-Plot (Eigenwerte der theoretischen Faktoren sind gemittelte Eigenwerte der theoretischen Stichproben)
            3. Auswahl der Faktoren (der empirischen Stichprobe), die höheren Eigenwert haben als Parallelanalyse-Faktoren
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fssoenksen%2FJ0FB4DwsXD.png?alt=media&token=04131c95-d833-4a50-b4b2-2e16cd620165)
- # Faktorenrotation
    - Ergebnis der Faktorenextraktion: Maximale Eigenwerte der Faktoren; Problem: Faktorenraum inhaltlich oft nicht interpretierbar
    - Lösung: Drehung des Faktorenraums mit Ziel eines Ladungsmusters, das Kriterium der Einfachstruktur entspricht
        - Kriterium der Einfachstruktur: Jede Variable lädt hoch auf nur einem Faktor (Primärladung) und niedrig/ nicht auf allen anderen (Sekundärladungen)
    - ## Orthogonale Rotationsverfahren
        - Unkorreliertheit der bereits extrahierten Faktoren wird beibehalten, rotierte Faktoren ebenfalls orthogonal und unabhängig interpretierbar
        - Bspw. Varimax-Rotation
    - ## Oblique Rotationsverfahren (**Präferenz**)
        - Unkorreliertheit der bereits extrahierten Faktoren wird aufgegeben
        - Bspw. Oblimin-Rotation
- **Faktorielle Validität**: Stützung der theoretischen Merkmalsstruktur durch Faktoranalyse
    - Eindimensionalität des Konstrukts: Zusammenhänge zwischen Items rückführbar auf gemeinsames latentes Konstrukt (Faktor)
