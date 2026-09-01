Gelernt:

Der Unterschied zwischen git (Programm auf dem Rechner, führt Buch über Änderungen) und GitHub (Website, auf der man Repositories ablegt und teilt)
Die drei Stationen, die eine Datei durchläuft: Arbeitsverzeichnis → Vormerkung → Repository, und wozu der Sammelkorb dazwischen gut ist
Die Befehlsfolge git init, git status, git add, git commit -m, git log --oneline
Was ein Remote ist: origin als Name für die Gegenstelle, git push -u origin main fürs erste Hochladen
Warum ein Repository auf GitHub leer angelegt werden muss, wenn man lokal schon eine Geschichte hat
Fine-grained Tokens: Rechte so eng wie möglich (nur ein Repo, nur Contents: Read and write) und mit Ablaufdatum
Probleme:

Fehler: externes Repository origin existiert bereits — und in der Adresse stand wörtlich DEIN-BENUTZERNAME, weil ich den Platzhalter mitkopiert hatte
Invalid username or token. Password authentication is not supported for Git operations. — mehrfach, obwohl das Passwort stimmte
Gelöst:

Mit git remote -v nachgesehen, was tatsächlich eingetragen ist, und mit git remote set-url origin ... korrigiert. Gelernt: add legt neu an und scheitert bei vergebenen Namen, set-url überschreibt eine bestehende Adresse.
Die Fehlermeldung genau gelesen — sie sagt wörtlich, dass Passwörter nicht unterstützt werden. Das Feld heißt „Password", verlangt aber den Token. Nach dem Einfügen des Tokens lief der Push sofort durch.