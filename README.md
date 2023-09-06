# blender-colab

<a href="https://colab.research.google.com/github/ynshung/blender-colab/blob/master/blender_render.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Dies ist ein Python-Skript, mit dem Sie Blender 3.0+ und ältere Versionen mit Google Colaboratory rendern können. Sie können die Blender-Dateien über direkten Upload, Google Drive oder URL hochladen. Die gerenderten Frames können direkt oder über Google Drive heruntergeladen werden. Dieses Skript bietet grundlegende Funktionen, sodass Sie das Skript nach Belieben anpassen können, um Ihren Anforderungen gerecht zu werden.

## Verwendung
### Hochladetyp
* `direct`: Laden Sie Ihre Blender-Datei in der nächsten Zelle hoch.
* `google_drive`: Die Blender-Datei wird direkt von Google Drive heruntergeladen. Sie müssen den Pfad zur Blender-/Zip-Datei unter `drive_path` angeben.
* `url`: Direkter Link zur Blender-Datei unter `url_blend`.
* `gdrive_relative`: Der bei `drive_path` angegebene Google Drive-Ordner wird direkt kopiert (als ob es eine Zip-Datei wäre).

### Downloadtyp
* `direct`: Ausgabedateien werden automatisch in Ihrem Browser heruntergeladen. (Funktioniert wahrscheinlich nicht mit mehreren Dateien?)
* `google_drive`: Die Ausgabedateien werden in den angegebenen `drive_output_path` eingefügt, sobald das Rendern abgeschlossen ist.
* `gdrive_relative`: Die Ausgabeframes werden automatisch in den angegebenen `drive_output_path` gerendert.

### Ein paar Anmerkungen
1. Sie müssen ein Google-Konto besitzen.
2. Ein Notebook kann nur maximal 12 Stunden (24 Stunden für Google Colab Pro) ausgeführt werden, aber nicht garantiert.
3. EEVEE-Rendering wird in einer virtuellen Maschine nicht unterstützt.
4. Dieses Skript wurde noch nicht vollständig getestet. Rechnen Sie mit einigen Fehlern.
5. Beachten Sie, dass Ihr Zugriff auf die GPU eingeschränkt oder blockiert sein kann, wenn Sie viele Stunden lang rendern.
6. Dieses Skript ist für diejenigen gedacht, die keinen Zugang zu High-End-GPU für das Rendern haben. Bitte verwenden Sie es verantwortungsbewusst!

## FAQ
### Ein Fehler ist aufgetreten!
Überprüfen Sie, welcher Abschnitt des Codes fehlgeschlagen ist und identifizieren Sie den Fehler (z.B. falsch geschriebene Dateien oder Pfad). Wenn Sie den Fehler nicht verstehen, versuchen Sie, den Code mit der Wiedergabetaste auf der Seite erneut auszuführen. Wenn es immer noch fehlschlägt, gehen Sie zu `Laufzeit > Alles neu starten`, um den Code neu zu starten, oder versuchen Sie es mit `Laufzeit > Werkseinstellungen zurücksetzen`. Wenn alles andere fehlschlägt, öffnen Sie ein Issue in GitHub mit dem Fehlerprotokoll, das Sie angehängt haben, und den Details Ihrer Einrichtung.

Häufige Fehler:
* `MessageError: TypeError: Failed to fetch` beim Herunterladen: Der Tab muss geöffnet sein, damit die Frames heruntergeladen werden können.

## Haftungsausschluss
Google Colab richtet sich an Forscher und Studenten, um AI/ML-Aufgaben, Datenanalyse und Bildung durchzuführen, nicht aber um 3D-Szenen zu rendern. Da die bereitgestellte Rechenleistung kostenlos ist, können sich die Nutzungslimits, Leerlauf-Timeouts und die Geschwindigkeit des Renderings von Zeit zu Zeit ändern. [Colab Pro und Colab Pro+](https://colab.research.google.com/signup) stehen für diejenigen zur Verfügung, die eine leistungsstärkere GPU und längere Laufzeiten für das Rendern wünschen. Weitere Informationen finden Sie in den [FAQs](https://research.google.com/colaboratory/faq.html). In einigen Fällen kann es schneller sein, einen Online-Blender-Renderfarm zu verwenden.
