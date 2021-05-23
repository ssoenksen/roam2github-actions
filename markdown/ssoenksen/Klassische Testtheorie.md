- # Grundlagen
    - Basis vieler Testverfahren, Ursprung im 20. Jahrhundert, dann bei Gulliksen (1950) und Lord und Novick (1968)
    - Messfehler-Theorie: Kernüberlegung ist dass Messwert aus true score und Messfeher zusammengesetzt ist
    - **Grundlage**: Schließen von mehreren Messungen $$x_{vi}$$ eines Pb v in Items i → wahre Ausprägung $$\tau_v$$ (true score) im Persönlichkeitsmerkmal
    - Axiome der KTT enthalten nur eine beobachtbare Größe, $$x_{vi}$$
    - ## Axiome
        1. Existenzaxiom: $$\tau_{vi} = E(x_{vi})$$, $$E(x)$$: Erwartungswert
        2. Verknüpfungsaxiom: $$x_{vi} = \tau_{vi} + \varepsilon_{vi}$$, $$\varepsilon$$: Messfehler
Aus 1. und 2. ergibt sich: $$E(\varepsilon_{vi})=0$$
        3. Unabhängigkeitsaxiom: $$Corr(\tau_{vi}, \varepsilon_{vi})=0$$
    - ## Zusatzannahmen
        - Unabhängigkeit der Messfehler zwischen Items: $$Corr(\varepsilon_{vi}, \varepsilon_{vj})=0$$
        - Unabhängigkeit der Messfehler zwischen Personen: $$Corr(\varepsilon_{vi}, \varepsilon_{wi})=0$$
- # Bestimmung von true score
    - Statistischer Ansatz der Mittelwertbildung aus mehrfachen Messungen zur Neutralisierung des Messfehlers nicht möglich (Erinnerungseinflüsse etc. → Axiome verletzt)
    - **Lösung**: Mehrere Messungen mit unterschiedlichen Items, die gleiches Merkmal erfassen → Neutralisierung der Zufallsfehler durch Zusammenführung in einen Messwert
    - Testwert (Rohwert) $$x_v = \sum_{i=1}^{m} x_{vi}$$
    - Testwert $$x_v$$ stimmt im Durchschnitt mit true score $$\tau_v$$ überein: $$x_v = \hat{\tau}_v$$ 
        - $$\begin{aligned} E(x_v) &= E(\sum_{i=1}^{m} x_{vi}) \\
&= \sum_{i=1}^{m} E(x_{vi}) \\
&= \sum_{i=1}^{m} \tau_{vi} \\
&= \tau_v \\
\Rightarrow x_v &= \hat{\tau}_v \end{aligned}$$
- # Bestimmung der Varianzen
    - **Grundlage**: Untersuchung der Testwerte über alle Probanden hinweg → Testwertevariable $$x$$ und true-score-Variable $$\tau$$, Fehlervariable $$\varepsilon$$ mit $$\varepsilon_v = x_v-\tau_v$$
        - $$\begin{aligned}
Var(x) &= Var(\tau + \varepsilon) \\
&= Var(\tau) + Var(\varepsilon) + 2 \cdot Cov(\tau, \varepsilon) \\
&= Var(\tau) + Var(\varepsilon)
\end{aligned}$$
    - $$x$$ und $$Var(x)$$ bekannt → **Ziel**: Schätzung von $$Var(\tau)$$ und $$Var(\varepsilon)$$
- ## Wahre Varianz
    - **Voraussetzung**: Bei parallelen bzw. $\tau$-äquivalenten Tests gilt: $$\tau_p = \tau_q = \tau$$
    - Berechnung der wahren Varianz: $$Var(\tau) = Cov(x_p, x_q)$$
        - $$\begin{aligned} Cov(x_p, x_q) &= Cov(\tau_p + \varepsilon_p, \tau_q + \varepsilon_q) \\
&= Cov(\tau_p, \tau_q) + Cov(\tau_p, \varepsilon_q) + Cov(\varepsilon_p, \tau_q) + Cov(\varepsilon_p, \varepsilon_q) \\
&= Cov(\tau_p, \tau_q) \\
&= Cov(\tau, \tau) \\
&= Var(\tau)
\end{aligned}$$
- ## Fehlervarianz
    - $$Var(\varepsilon) = Var(x) - Var(\tau)$$
- # Gütekriterium Reliabilität
    - Reliabilität $$Rel$$ bezeichnet die Messgenauigkeit eines Tests und ist als Anteil der Varianz der wahren Werte $$\tau$$ an der Varianz der beobachteten Testwerte $$x$$ definiert: $$Rel = \frac{Var(\tau)}{Var(x)}$$
    - Bei parallelen Tests gilt: $$Rel = r_{tt}$$
        - $$Rel = \frac{Var(\tau)}{Var(x)} = \frac{Cov(x_p, x_q)}{SD(x_p)\cdot SD(x_q)} = Corr(x_p, x_q) = r_{tt}$$
    - Zusammenhang mit Testlänge: [[Spearman-Brown-Formel]]
- # Standardmessfehler
    - Grundlage (bekannt): $$Var(x)$$, $$Rel$$
        - $$SD(\varepsilon) = SD(x)\cdot \sqrt{1-Rel}$$
- # Konfidenzintervall für true score
    - Bereich um Punktschätzung $$\hat{\tau}_v = x_v$$: 95%/ 99% aller wahren Werte, die Punktschätzung erzeugt haben können
    - Bei Stichproben mit $$n < 60$$ t-Verteilung statt z
    - $$\hat{\tau}_v - z_{\alpha /2} \cdot SD(\varepsilon) \leq \tau_v \leq \hat{\tau}_v + z_{\alpha /2} \cdot SD(\varepsilon)$$
- # Bewertung
    - Bewährter Ansatz, ökonomisch praktisch
    - Aber: Wahrer Wert und Fehlerwert nicht empirisch überprüfbar, deshalb Verknüpfungsaxiom nicht überprüfbar
    - Aber: Intervallskalierung nicht überprüfbar
