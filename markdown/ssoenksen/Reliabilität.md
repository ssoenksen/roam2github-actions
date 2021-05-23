- # Reliabilität
    - = Genauigkeit einer Messung. Ein Testverfahren ist perfekt reliabel, wenn die damit erhaltenen Testwerte frei von zufälligen Messfehlern sind. Das Testverfahren ist umso weniger reliabel, je größer die Einflüsse von zufälligen Messfehlern sind.
    - = $$Rel$$ bezeichnet die Messgenauigkeit eines Tests und ist als Anteil der Varianz der wahren Werte $\tau$ an der Varianz der beobachteten Testwerte $$x$$ definiert: $$Rel = \frac{Var(\tau)}{Var(x)}$$ mit $$Rel: \{0; 1\}$$
    - Reliabilität ist immer eine Schätzung, Grundlage ist Korrelation eines Tests mit sich selbst: $$r(x,x)=\frac{\sigma(x,x)}{\sigma(x) \cdot \sigma(x)}=\frac{\sigma^2(\tau)}{\sigma^2(x)}$$ (wegen [[Annahmen KTT]])
    - Extremformen:
        - Test misst wahren Wert: $$Var(x) = Var(\tau) \Rightarrow Rel = \frac{Var(\tau)}{Var(x)} = \frac{Var(\tau)}{Var(\tau)} = 1$$ 
        - Testwert __nur__ von Messfehlern abhängig: $$Var(x) = Var(\varepsilon) \Rightarrow Var(\tau) = Var(x)-Var(\varepsilon)=0 \Rightarrow Rel=\frac{0}{Var(x)}=0$$
    - Erhöhung der Reliabilität durch Hinzunahme paralleler Testteile 
        - Überprüfung: [[Parallelität von Tests]]
        - [[Spearman-Brown-Formel]] zur Berechnung der neuen Reliabilität
        - Effekte (→ lohnt sich eher bei geringer Reliabilität, auch umgekehrt denkbar): ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fssoenksen%2F-pP1_mqCJE.png?alt=media&token=d33ea657-874b-4187-88e7-25d44de15756)
    - ## Methoden der Reliabilitätsbestimmung
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fssoenksen%2FBwcGo926hT.png?alt=media&token=dfde6961-4c5e-4912-a15b-71269711382c)
        - ### Retest-Reliabilität
            - Vorgehen:
                1. Durchführung des Tests an gleicher Stichprobe zweimal
                2. Berechnung: $$Rel(x) = r_{tt} = Corr(x_1, x_2)$$
            - Annahmen:
                - Keine Veränderung der wahren Werte (unproblematisch: systematische Veränderungen in der gesamten Stichprobe)
                - Gleiche Messfehlereinflüsse
                - Keine Erinnerungseffekte
                - Auswirkungen: ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fssoenksen%2FW-vRQ8X5D3.png?alt=media&token=3df778f8-7911-4baa-90c7-7226a1d1880d)
        - ### Paralleltest-Reliabilität (Königsweg)
            - Vorgehen:
                1. Konstruktion von zwei parallelen Tests ([[Parallelität von Tests]])
                2. Vorlage bei gleicher Stichprobe
                3. Berechnung: $$Rel(x) = Corr(x_p, x_q)$$
            - Annahmen:
                - Abweichung von Parallelität → Unterschätzung der Reliabilität
                - Einfluss durch Übungseffekte
                - Einfluss durch zeitliche Merkmalsveränderungen
        - ### Splithalf-Reliabilität
            - Vorgehen:
                1. Teilung der Testitems in zwei möglichst parallele Testhälften $$x_p$$ und $$x_q$$
                2. Berechnung: $$Rel(x) = Corr(x_p, x_q)$$
            - Methoden der Testhalbierung:
                - **Odd-Even-Methode:** v.a. für Leistungstests mit steigenden Schwierigkeiten
                - **Zeitpartitionierungsmethode**: v.a. bei gleichartigen Items, bspw. Konzentrationstests
                - **Methode der Itemzwillinge:** Paarbildung aufgrund Schwierigkeit und Trennschärfe, dann zufällige Zuweisung auf Testhälfte; v.a. bei heterogenen Items
        - ### Interne Konsistenz (Cronbachs Alpha)
            - Jedes einzelne Item entspricht separatem Testteil zur Messung des Merkmals → Cronbachs Alpha: Verallgemeinerung auf beliebig viele Testteile
            - Berechnung: $$Rel(x)=\alpha= \frac{m}{m-1}\cdot (1-\frac{\sum_{i=1}^{m} Var(x_i)}{Var(x)})$$
            - Grundlage ist [[Parallelität von Tests]]; wenn nicht möglich:
                - $$\tau$$-Äquivalenz: Gleiche wahre Werte, unterschiedliche Fehlervarianzen
                - Essentielle $$\tau$$-Äquivalenz: Wahre Werte unterscheiden sich um additive Konstante, unterschiedliche Fehlervarianzen ($$\tau_i = \tau + c_i$$)
