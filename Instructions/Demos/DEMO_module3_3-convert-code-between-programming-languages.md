---
demo:
  title: 'Demo: Konvertieren von Code von einer Programmiersprache in eine andere'
  module: 'Module 3: Develop code features using GitHub Copilot tools'
---

# Demo: Konvertieren von Code von einer Programmiersprache in eine andere

## Anweisungen

Die Demoaktivitäten sind für eine Umgebung konzipiert, die die folgenden Ressourcen enthält:

- Visual Studio Code.
- C# Dev Kit-Erweiterung für Visual Studio Code
- GitHub Copilot- und GitHub Copilot Chat-Erweiterungen für Visual Studio Code Ein GitHub-Konto mit einem aktiven Abonnement für GitHub Copilot ist erforderlich.
- Beispielcodeprojekte, die mit C# erstellt wurden

**HINWEIS:** Wir empfehlen, dass Kursleitende die Verwendung ihres eigenen GitHub-Kontos und GitHub Copilot-Abonnements für die Demos in Betracht ziehen. Auf diese Weise können Sie Ihre Entwicklungsumgebung steuern und anpassen. Außerdem wird es einfacher, die Demos an die Bedürfnisse der Kurse anzupassen.

**WICHTIG:** Wenn Sie sich entscheiden, die Demos in der gehosteten Labumgebung und nicht auf dem Kursleiter-PC auszuführen, können Sie die Beispiel-Apps in der gehosteten Umgebung entzippen. Sie müssen die GitHub Copilot-Erweiterungen in der gehosteten Umgebung konfigurieren, bevor Sie die Demos ausführen können. Möglicherweise stellen Sie fest, dass die gehostete Umgebung langsamer ist als Ihre lokale Umgebung. Daher müssen Sie möglicherweise das Tempo der Demos entsprechend anpassen.

### Einführen der Demo

GitHub Copilot kann Ihnen helfen, Code von einer Programmiersprache in eine andere zu konvertieren. Sie können beispielsweise GitHub Copilot bitten, eine Funktion oder einen Codeausschnitt in eine andere Programmiersprache zu konvertieren.

Sie können die folgenden Codekonvertierungen mithilfe von GitHub Copilot abschließen:

- Eine gesamte Codedatei in eine andere Programmiersprache konvertieren.
- Eine Funktion in eine andere Programmiersprache konvertieren.
- Einen Codeausschnitt in eine andere Programmiersprache konvertieren.

Jede der Chatschnittstellen (Chatansicht, Quick Chat-Fenster und Inlinechat) kann verwendet werden, um Code zwischen Programmiersprachen zu konvertieren. Ihre Wahl der Chatschnittstelle hängt von Ihrer Vorliebe und der Komplexität des Codes ab, den Sie konvertieren möchten.

Angenommen, Sie beginnen gerade mit dem `QuarterlyIncomeReport` Projekt. Sie besprechen die Projektziele mit einem Kollegen. Sie erwähnen, dass sie eine Python-Datei haben, die einige der Features bereitstellen könnte, die Sie suchen. Sie verweisen auf das Repository für den Python-Code. Sie entscheiden sich, das Python-Codeprojekt in Visual Studio Code zu öffnen und die Chatansicht zu verwenden, um den Python-Code in C# zu konvertieren.

## Konvertieren von Code zwischen Programmiersprachen mithilfe der Chatansicht

1. Öffnen Sie den Projektordner **APL2007M3Python** in Visual Studio Code.

    Dieses Projekt enthält eine Python-Version des `QuarterlyIncomeReport` Projekts, an dem Sie während dieses Moduls gearbeitet haben. Sie können GitHub Copilot den Code mithilfe der Chatansicht erklären oder diese intelligente Aktion erläutern.

1. Führen Sie die Python-Anwendung aus.

    Beachten Sie, dass die Ausgabe der Python-Anwendung im Wesentlichen mit der Ausgabe der C#-Anwendung übereinstimmt, die Sie zuvor erstellt haben.

1. Öffnen Sie die `main.py` Python-Datei.

    Die Python-Datei enthält eine Funktion, die Umsatzdaten generiert. Sie möchten diesen Python-Code in C# konvertieren.

1. Wählen Sie den gesamten Dateiinhalt aus.

1. Öffnen Sie die Chatansicht, und geben Sie dann die folgende Eingabeaufforderung ein:

    ```plaintext
    Convert #selection to C#
    ```

1. Nehmen Sie sich einen Moment Zeit, um die Antwort von GitHub Copilot zu überprüfen.

    Die Antwort sollte die C#-Version des von Ihnen ausgewählten Python-Codes enthalten.

1. Öffnen Sie eine zweite Instanz von Visual Studio Code.

1. Öffnen Sie die Chatansicht, geben Sie die folgende Eingabeaufforderung ein:

    ```plaintext
    @workspace /new console application in C# NET8 named APL2007M3B. Only .cs and .csproj files. Enable ImplicitUsings and Nullable
    ```

    Wenn Copilot mit einer Fehlermeldung über das "Path-Argument" antwortet, versuchen Sie die gleiche Eingabeaufforderung erneut.

1. Wählen Sie **Arbeitsbereich erstellen** aus

1. Wählen Sie im Dialogfeld "Ordner öffnen" den **Desktopordner** und dann **Als übergeordneter Ordner auswählen** aus.

    Warten Sie, bis der Arbeitsbereich erstellt wurde.

1. Wenn der Arbeitsbereich erstellt wird, wählen Sie **Program.cs**aus, und löschen Sie den Dateiinhalt.

1. Wechseln Sie zur Instanz von Visual Studio Code, die den Python-Code enthält.

1. Scrollen Sie zum Oberen Rand der Chatansicht, und klicken Sie auf die Schaltfläche **Kopieren**, um den generierten C#-Code in die Zwischenablage zu kopieren.

1. Wechseln Sie zur Instanz von Visual Studio Code, die den C#-Code enthält.

1. Fügen Sie den C#-Code in die Datei Program.cs ein.

1. Speichern Sie die Datei Program.cs.

1. Führen Sie die C#-Anwendung aus.

    Beachten Sie, dass die Ausgabe der C#-Anwendung im Wesentlichen mit der Ausgabe aus der Python-Anwendung identisch ist.

    Wenn Sie Zeit haben, nehmen Sie sich einige Minuten Zeit, um die Unterschiede zwischen dem konvertierten C#-Code und dem C#-Code aus der vorherigen Einheit zu überprüfen.

## Konvertieren von Code zwischen Programmiersprachen mithilfe des Inlinechats

1. Wechseln Sie zurück zur Visual Studio Code-Instanz, die das zuvor geöffnete Python-Projekt enthält.

1. Wählen Sie den Code in der main.py Datei aus.

1. Öffnen Sie den Inlinechat, und geben Sie die folgende Eingabeaufforderung ein:

    ```plaintext
    Convert #selection to C#
    ```

1. Überprüfen Sie die Antwort von GitHub Copilot, und wählen Sie dann **Annehmen** aus.

    Die Python-Datei sollte jetzt C#-Code enthalten.

1. Kopieren Sie den generierten C#-Code in die Zwischenablage.

1. Schließen Sie die main.py Datei, ohne die Änderungen zu speichern.

1. Wechseln Sie zur Visual Studio Code-Instanz, die das C#-Projekt enthält, und öffnen Sie die Program.cs Datei.

1. Um den vorhandenen C#-Code zu überschreiben, fügen Sie den C#-Code aus der Zwischenablage (konvertiert aus Python mithilfe von Inlinechat) über den Inhalt der Program.cs Datei ein.

1. Speichern Sie die Datei Program.cs.

1. Führen Sie die C#-Anwendung aus.

    Beachten Sie, dass die Ausgabe der C#-Anwendung im Wesentlichen mit der Ausgabe aus der Python-Anwendung identisch ist.

Wenn Sie GitHub Copilot verwenden, um Code zwischen Programmiersprachen zu konvertieren, probieren Sie, sowohl die Chatansicht als auch den Inlinechat zu nutzen. Obwohl beide Tools das gleiche KI-Modell nutzen, können sich ihre Ergebnisse unterscheiden. Wenn Sie beide Tools ausprobieren, können Sie ermitteln, welches Tool für Ihren spezifischen Anwendungsfall am besten geeignet ist.

> [!NOTE]
> Programmiersprachen verfügen häufig über einen zugeordneten „Programmierstil“, und einige Sprachen verfügen möglicherweise über eindeutige Features oder Codebibliotheken. Wenn Sie große Codeabschnitte von einer Programmiersprache in eine andere konvertieren, ist es wichtig, die Zielprogrammiersprache und die Ziele des Codes vollständig zu verstehen. GitHub Copilot-Vorschläge sollten vor der Annahme immer überprüft werden.

### Zusammenfassung

In dieser Demo haben Sie GitHub Copilot verwendet, um Python-Code in C# zu konvertieren. Sie haben die Chatansicht und den Inlinechat verwendet, um den Python-Code in C# zu konvertieren. Anschließend haben Sie die C#-Anwendung ausgeführt, um zu überprüfen, ob die Ausgabe mit der Ausgabe aus der Python-Anwendung identisch war. Mithilfe von GitHub Copilot können Sie Code zwischen Programmiersprachen konvertieren und Code in einer Sprache schnell an eine andere Sprache anpassen. Denken Sie daran, den konvertierten Code zu überprüfen, um sicherzustellen, dass er Ihre Anforderungen erfüllt und dem Programmierstil der Zielsprache entspricht.
