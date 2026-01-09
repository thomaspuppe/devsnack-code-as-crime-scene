


<section>
Welcher Code ist komplexer?
TODO: beide Grafiken von p70 nebeneinander
</section>



<section>
TODO: 
</section>
<aside>
komplexer Code kommt von 
- accidental vs essential complexity
- scaling (no one has a holistic view)	


cyclomatic complexity:
- counting the number of logical paths
- fails to capture _impact_


p26: Complexity
- Cyclomatic
- Halstead
- Cognitive
- LOC (genauso gut)

Combined: Hotspot

Auch cool: Histogram of changes in Files
<section>

> Complex code is only a problem if we need to deal with it.
</section>
<aside>
Daher hilft uns der Blick auf statische Daten nur bedingt, um Probleme zu finden.
</aside>



<section>
- Adam Tornhill: Studierter Kriminalpsychologe
- Buch Cover (links)
- Hotspot Jack The Ripper (rechts)
</section>

<aside>
- Hotspot Analyse reduziert eine große Codebasis auf Teile, kritische Module, bei denen z.B. Testing und Refactoring mehr Wert haben als in anderen.
- https://wettel.github.io/codecity.html
- Aber das ist nur statische Analyse, das hatten wir schon. 
- Wichtig: wer ist dort wie häufig unterwegs?
</aside>


Code Churn messen: Welche Files werden häufig angefasst?

Change Coupling: keine Abhängigkeit im Quellcode, aber zwei Dinge werden in Commits oder PRs immer gemeinsam angefasst.

<section>
> Number of times that a code changes is a better predictor of defects than code size.
> – (Studie p18 und p43)
</section>
<aside>
- Komplexität + Energie, die reingesteckt wird.
</aside>


TODO: Übergang zum WIE (also Git Analysen)


Software: 
- Code-Maat


Visualisierung: "Zoomable Circle Packing" mit JSON+D3 (Script p39)
gut: Sprach-agnostisch

zeitliche Einschränkung: forever? 1 Jahr, rund um Projekte

next Level: Vergleich von Zeiträumen

p47: k8s

<section>
Was tun mit den Hotspots?
- Tech Debt
- Refactoring
- Code Reviews
- Tests
- Onboarding
</section>



<section>
Next Level: Complexity Trends

- Komplexität via "nagative space", also indentations per line (auf p52)
- Nesting als Proxy für Komplexität
- Script für Trend auf p55
- plus: LOC + Complexity nebeneinander (Example k8s auf p60)
- Refactoring: (well) named functions extrahieren

</section>





<section>
	Technical Debt Folie (erst Zitat, dann Headline)
	> Individuals with short time horizons face higher risk of criminal involvement, simply because they can reap the rewards of the crime here and now, whereas the punishment lies in an indefinite future. (p84)
</section>

Und auch: 
- conceptual debt
- workflow debt



<section>
	- time-in-development per file: Assoziation von Code zu Jira in-Progress Status.
	- nuber of defects per file: Bugtickets (oder FIX-commits)
	- percentage of unplanned work
</section>


p87: "code health" Links -> slower and more buggy
p97: "code health" Viz
  - focus on relevant parts
  - priority priming


p104) dev-Log und ADR gegen "falsche Zeugenaussagen/biases/falsche erinnerungen" (zB Loftus, aber das weglassen)


p109: Modus Operandi in Code Change
- "change coupling" - files are coupled, if they are repeatedly changed together in one commit/PR
- hidden/implicit coupling. (explicit couling is: module+unittest)
- p111: Link zu Beisiel
- p113: Bsp of how to react/what to do
- p119: Sum of Coupling: Wie häufig werden andere Dateien geändert, wenn diese hier geändert wird?
- level up: zeitgewichtet (aktuelle wichtiger). Aber simpel ist genauso gut, also zu bevorzugen.

- Interpretationssache: wenn Tests immer zusammen mit dem Code angefasset werden ...
	- entweder werden Tests erweitert und angepasst
	- oder die Tests hängen zu sehr an den konkreten Implementierungsdetails und zu wenig am Feature



part 3: The social side of code

- unterhaltsam: Word Cloud aus den Commit Messages der Projekte

- number of unique authors (or teams) in each file (during the last year)
- brooke's law and conways law
- aber auch Truck factor
	- p228 Source = truck factor of popular github repositories
- "how many people can leave before we lose 50% of the code?"
- p232: Viz of truck factor with hotspots
- p239: knowledge map via git blame, and fractal viz -> docs zB ?


https://github.com/angular-architects/detective

