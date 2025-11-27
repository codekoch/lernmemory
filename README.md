# <a href= href=https://codekoch.github.io/lernmemory/> Lernmemory </a>

🧠🎮Ein interaktives Lernspiel für zwei Spieler, das klassisches Memory mit einem Rate-Duell verbindet. Findet Paare, deckt das Spielfeld auf und erratet die geheime Botschaft des Gegners!

🌟 SpielprinzipSetup: Zwei Spieler geben verdeckt eine geheime Nachricht ein und wählen einen Anzeigemodus (Normal, Spiegelverkehrt oder Buchstabensalat).Memory: Die Spieler decken abwechselnd Karten auf. Die Kartenpaare bestehen aus zusammengehörigen Lerninhalten (z. B. Funktion und Graph).Das Duell: Gefundene Paare verschwinden und geben den Blick auf die geheime Nachricht im Hintergrund frei.Gewinnen: Wer ein Pärchen findet, darf für 3 Sekunden versuchen, die Nachricht zu erraten. Wer sie zuerst korrekt eintippt (oder am Ende die meisten Punkte hat), gewinnt!

🚀 NutzungDas Tool ist eine Single-File-Application.Öffne die Datei MemoryBuilder.html in einem modernen Browser.Editor-Modus: Erstelle eigene Kartenpaare oder importiere sie.Export: Klicke auf "Als HTML speichern", um das fertige Spiel als eigenständige Datei herunterzuladen. Diese Datei läuft offline und kann einfach weitergegeben werden.

📝 Erstellung von JSON-VorlagenDu kannst Kartensets extern vorbereiten und über den "JSON Import" Button laden.GrundstrukturDie Datei muss ein valides JSON-Objekt sein, das ein Array pairs enthält.{
  "pairs": [
    {
      "a": "Inhalt Karte 1",
      "b": "Inhalt Karte 2"
    }
  ]
}
Inhalte formatierenDas Spiel unterstützt reinen Text, HTML und mathematische Formeln (LaTeX/MathJax).1. Einfacher Text{ "a": "Hund", "b": "Dog" }

2. HTML (Formatierung)Nutze HTML-Tags für Fettgedrucktes, Zeilenumbrüche oder Farben.Wichtig: Verwende innerhalb der Tags einfache Anführungszeichen ', damit das JSON nicht bricht.{
  "a": "Hauptstadt von<br><b>Frankreich</b>",
  "b": "<span style='color:blue'>Paris</span>"
}

3. Mathematik (LaTeX)
   
🧮Formeln werden mit MathJax gerendert.Wrapper: Die Formel muss in \( ... \) stehen.Escaping: Da der Backslash \ in JSON ein Steuerzeichen ist, muss er verdoppelt werden (\\).Beispiel: $f(x) = x^2${
  "a": "Normalparabel",
  "b": "\\( f(x) = x^2 \\)"
}
Beispiel: Bruch $\frac{1}{2}${
  "a": "0,5",
  "b": "\\( \\frac{1}{2} \\)"
}
Vollständiges Beispiel-Set{
  "pairs": [
    {
      "a": "<b>Binomische Formel</b> (+)",
      "b": "\\( (a+b)^2 = a^2 + 2ab + b^2 \\)"
    },
    {
      "a": "Sinus von 90 Grad",
      "b": "1"
    },
    {
      "a": "Verschiebung um 2 nach <br><i>oben</i>",
      "b": "\\( f(x) = x^2 + 2 \\)"
    }
  ]
}

🛠 TechnologienReact (Logik & UI)Tailwind CSS (Styling)MathJax (Formel-Rendering)Single-File-Architecture (Kein Build-Prozess nötig, läuft direkt im Browser)
