# 🛒 Einkaufs-Tracker PWA

Eine Progressive Web App zum Verwalten von Einkaufslisten mit integriertem Ausgaben-Tracker.

## ✨ Features

- ✅ **Einkaufsliste** mit Produkten, Kategorien und Preisen
- 💰 **Automatische Ausgaben-Berechnung**
- 📊 **Statistiken** über Ausgaben und Kategorien
- 📱 **Installierbar** auf Android (und anderen Geräten)
- 🔄 **Offline-Funktionalität** - funktioniert ohne Internet
- 💾 **Lokale Datenspeicherung** - deine Daten bleiben auf deinem Gerät
- 📤 **Export-Funktion** zum Teilen mit Familie/Mitbewohnern
- 🎯 **Kategorien**: Obst & Gemüse, Milchprodukte, Backwaren, Getränke, Fleisch & Fisch, Sonstiges

## 📲 Installation auf Android

### Methode 1: Über Chrome Browser
1. Öffne die `index.html` in Chrome
2. Tippe auf das **Menü** (⋮) oben rechts
3. Wähle **"Zum Startbildschirm hinzufügen"**
4. Bestätige mit **"Hinzufügen"**
5. Die App erscheint als Icon auf deinem Homescreen! 🎉

### Methode 2: Über lokalen Server
```bash
# Mit Python (wenn Python installiert ist)
python3 -m http.server 8000

# Oder mit PHP
php -S localhost:8000

# Dann öffne im Browser:
http://localhost:8000
```

### Für Web-Hosting (z.B. GitHub Pages, Netlify)
1. Lade alle Dateien in dein Repository/Hosting hoch
2. Stelle sicher, dass die `manifest.json` und Icons korrekt verlinkt sind
3. Besuche die URL auf deinem Android-Gerät
4. Installiere die App wie oben beschrieben

## 🎯 Nutzung

### Artikel hinzufügen
1. Gib Produktname, Kategorie und Preis ein
2. Klicke auf "Artikel hinzufügen"
3. Der Artikel erscheint in deiner Liste mit automatischer Summenberechnung

### Einkauf durchführen
- Hake gekaufte Artikel ab durch Antippen der Checkbox
- Lösche einzelne Artikel mit dem ×-Button
- Schließe den Einkauf ab mit "Einkauf abschließen"

### Verlauf ansehen
- Wechsle zum **"Verlauf"**-Tab
- Sieh alle vergangenen Einkäufe mit Datum und Summe
- Exportiere Daten als JSON-Datei

### Statistiken
- Im **"Statistik"**-Tab findest du:
  - Gesamtausgaben
  - Durchschnitt pro Einkauf
  - Ausgaben nach Kategorien

### Daten teilen
1. Gehe zum "Verlauf"-Tab
2. Klicke auf "Daten exportieren"
3. Teile die JSON-Datei mit Familie/Mitbewohnern
4. Sie können die Datei importieren (Import-Funktion kann ergänzt werden)

## 📁 Dateistruktur

```
shopping-pwa/
├── index.html          # Haupt-App-Datei
├── manifest.json       # PWA-Manifest für Installation
├── service-worker.js   # Service Worker für Offline-Funktion
├── icon-192.png        # App-Icon (192x192px)
├── icon-512.png        # App-Icon (512x512px)
└── README.md           # Diese Datei
```

## 🔧 Technische Details

- **Keine Frameworks** - Pure HTML, CSS, JavaScript
- **LocalStorage** für Datenpersistenz
- **Service Worker** für Offline-Caching
- **Responsive Design** für alle Bildschirmgrößen
- **PWA-Standard** - funktioniert auf allen modernen Browsern

## 💾 Datenspeicherung

Alle Daten werden lokal im Browser gespeichert:
- Aktuelle Einkaufsliste
- Einkaufs-Verlauf
- Keine Cloud-Synchronisation (Datenschutz!)

## 🎨 Anpassungen

### Farben ändern
In der `index.html` im `<style>`-Bereich:
```css
/* Hauptfarbe ändern */
.header {
    background: linear-gradient(135deg, #2c5aa0 0%, #1e3a6f 100%);
}
```

### Kategorien erweitern
In der `index.html` im `<select id="itemCategory">`:
```html
<option value="Neue Kategorie">🔥 Neue Kategorie</option>
```

### Icons ändern
Ersetze einfach `icon-192.png` und `icon-512.png` mit eigenen Bildern.

## 🚀 Erweiterungsideen

- [ ] Import-Funktion für geteilte Daten
- [ ] Barcode-Scanner Integration
- [ ] Ausgaben-Budgets setzen
- [ ] Monatliche/wöchentliche Reports
- [ ] Push-Benachrichtigungen für Erinnerungen
- [ ] Multi-Listen Support (verschiedene Läden)

## 📄 Lizenz

Frei verwendbar für persönliche und kommerzielle Zwecke.

## 🐛 Fehlerbehebung

**App lässt sich nicht installieren?**
- Stelle sicher, dass du HTTPS oder localhost verwendest
- Chrome/Edge Browser verwenden
- Cache leeren und neu laden

**Daten gehen verloren?**
- LocalStorage wird beim Browser-Cache löschen gelöscht
- Exportiere regelmäßig deine Daten!

**Offline funktioniert nicht?**
- Service Worker muss einmal geladen werden (mit Internet)
- Danach funktioniert alles offline

---

Viel Spaß beim Einkaufen! 🛒💰
