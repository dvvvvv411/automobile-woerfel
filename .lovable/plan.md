
# Domain-Konfiguration aktualisieren

## Problem
Die Vite-Konfiguration enthält noch die alte Domain "eweret-automobile.de" in den `allowedHosts`. Da die Seite jetzt für "Automobile Wörfel GmbH" ist, muss die neue Domain "automobile-woerfel.de" hinzugefügt werden.

---

## Änderung

### vite.config.ts aktualisieren
Die `allowedHosts` in beiden Abschnitten (`server` und `preview`) werden auf die neue Domain "automobile-woerfel.de" geändert:

**Vorher:**
```typescript
allowedHosts: ["eweret-automobile.de"]
```

**Nachher:**
```typescript
allowedHosts: ["automobile-woerfel.de"]
```

---

## Technische Details
- **Datei:** `vite.config.ts`
- **Zeile 12:** `server.allowedHosts` ändern
- **Zeile 17:** `preview.allowedHosts` ändern

Dies behebt den "Blocked request" Fehler und ermöglicht den Zugriff über die neue Domain.
