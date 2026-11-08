# Magnesium Store & Cape Registry

Dieses Repository steuert den Magnesium-Store und die geteilte Cape-Registry.
Der Store startet leer: die früheren Capes und Cosmetics wurden entfernt.

## Dateien

- `magnesium/store.json` - Coins, Preise, Items und Bundles
- `magnesium/registry.json` - geteilte Capes (aktuell leer)
- `magnesium/capes/` - optionale Cape-Texturen (aktuell leer)

Store-URL:

`https://raw.githubusercontent.com/Magnuuuz/magnesium-capes/main/magnesium/store.json`

## Coins

```json
"coins": {
  "name": "Coins",
  "default": 1500,
  "players": { "Name": 2000 },
  "grants": { "Name": { "welcome": 500 } }
}
```

- `default` ist das Startguthaben; hier **1500**.
- `players` überschreibt den Startwert pro Spielername.
- `grants` sind einmalige Zusatzgutschriften pro Spieler und Grant-ID.

## Items

```json
{
  "id": "cape_m",
  "type": "CAPE",
  "name": "M Cape",
  "description": "The classic Magnesium cape",
  "url": "capes/m-cape.png",
  "price": 250
}
```

Typen: `CAPE`, `HAT`, `GLASSES`, `BANDANA`, `SWORD`, `EMOTE`.
`url` ist relativ zu `store.json` (oder absolut). `price` ist in Coins; `0` ist gratis.

## Bundles

```json
{
  "id": "starter",
  "name": "Starter",
  "price": 400,
  "items": ["cape_m", "cape_night", "hat_cap"]
}
```

Ein Bundle ist eine beliebige Liste von Item-IDs zu einem Gesamtpreis.

## Wichtig

- Nur der Besitzer ändert diese Dateien; Spieler können nichts hochladen.
- `id` nach dem ersten Verkauf nicht mehr ändern, sie ist der Besitz-Schlüssel.
- Nach Änderungen im Client **Store -> Refresh** drücken.
