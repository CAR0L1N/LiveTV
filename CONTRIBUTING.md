# Kodinerds IPTV Contributing

## Streams hinzufügen/ändern

Eine detaillierte Anleitung zum GitHub Workflow findet sich
[hier](https://git-scm.com/book/de/v2/GitHub-Mitwirken-an-einem-Projekt).
Es ist nicht erforderlich, das Repository auszuchecken.
Alle Änderungen können im Browser vorgenommen werden.

1. Repository forken
2. Im Fork einen neuen Branch anlegen
3. Änderungen in `iptv/source.yaml` einbauen (z.B. URL ändern) - siehe
   [Hinweis](###-Hinweis)
4. Pull Request erstellen (Title z.B. "Fix ..." oder "Add ...")

### Hinweis

Wenn Streams in mehreren Qualitäten verfügbar sind, bitte immer den
`master.m3u8`-Stream verwenden!

<details>
<summary>Klicke hier für Begründung</summary>
<br>

Viele Streams, die also `master.m3u8` verfübar sind, bieten direkte Links mit
verschiedenen Auflösungen an:

```text
https://mcdn.daserste.de/daserste/de/master.m3u8
> https://mcdn.daserste.de/daserste/de/master_640p_828.m3u8 (640x360)
> ...
> https://mcdn.daserste.de/daserste/de/master_1920p_5128.m3u8 (1920x1080)
```

Das initiale Laden der Direktlinks kann je nach Anwendung zwar zu schnelleren
initialen Ladezeiten führen, verhindert aber auch die Nutzung von niedrigeren
Auflösungen (z.B. bei langsameren Verbindungen).

Zudem werden Direktlinks deutlich häufiger vom Provider umbenannt/ersetzt, also
dies bei `master`-Links der Fall ist.
Die Nutzung von Direktlinks erfordert daher einen deutlich höheren Aufwand der Listenpflege.

</details>

## Links

- [GitHub - Mitwirken an einem Projekt](https://git-scm.com/book/de/v2/GitHub-Mitwirken-an-einem-Projekt)
