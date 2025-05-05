[[_TOC_]]
# Beschrieb
Der PVA (Prozesswert Analog) vereint die Funktionalitäten von MWA (Messwert Analog) und IWA (Istwert Analog) in einem HMI-Element. Er ermöglicht die Visualisierung eines analogen Prozesswerts mit farbcodierter Darstellung sowie die Konfiguration von vier Grenzwerten (Alarm tief/hoch, Warnung tief/hoch) mit Hysterese-Funktion. Das Typical bietet die Verarbeitung analoger Eingangssignale mit unterschiedlichen Signaltypen, Signalfilterung, Offset-Korrektur, Ersatzwertvorgabe bei Signalausfall und eine Simulationsfunktion für Testzwecke. Zusätzlich verfügt es über integrierte Screens für Trend-Darstellung, Meldungsanzeige und Parametrierungsmöglichkeiten.

# Symbol
Das Symbol zeigt den aktuellen Messwert mit entsprechender Einheit an und wechselt die Hintergrundfarbe je nach Zustand. Zudem wird unten rechts der [Hint](Global/Hint.md) angezeigt.

|Symbol|Beschreibung|
|-|-|
|![Pva](../../.content/HmiGrafics/GraficsGeneral/symbols/PVA/Pva.png)|PVA-Typical Symbol ohne anstehende Meldung|
|![PvaWarnung](../../.content/HmiGrafics/GraficsGeneral/symbols/PVA/PvaWarnung.png)|PVA-Typical Symbol bei aktiver Warnung|
|![PvaAlarm](../../.content/HmiGrafics/GraficsGeneral/symbols/PVA/PvaAlarm.png)|PVA-Typical Symbol bei aktivem Alarm|

# Container
Der Container zeigt den Screen an, der an der [Standardnavigation](Global/Navigator/Navigator.md) angewählt wurde. Folgende Screens stehen bei diesem Typical zur Verfühgung:
- [Main](#main)
- [Trend](Global/Screens/Trend.md)
- [Message](Global/Screens/Message.md)
- [Limit](Global/Screens/Limit.md)
- [Parameter](#parameter)
- [Message Group](Global/Screens/MessageGroup.md)

## Main
Der Main besteht aus der PVA Anzeige und den Symbolen, die die verschiedenen Alarme und Warnungen anzeigen.

<div style="position: relative; width: 100%; max-width: 600px;" id="picPvaSlider">
    <img src="../../.content/HmiGrafics/TypicalPVA/ScreenMainPva.png" style="width: 90%;" alt="picPvaSlider">
  
  <a href="#modus">
      <div style="position: absolute; left: 2.7%; top: 18.3%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">1</div>
  </a>
  <a href="Global/Screens/Trend.md">
    <div style="position: absolute; left: 16%; top: 0%; transform: translate(0%, 0%); width: 67.5%; height: 45%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">2</span>
    </div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 15%; top: 73%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">3</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 30%; top: 73%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">4</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 56%; top: 73%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">5</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 70.5%; top: 73%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">6</div>
  </a>
</div>

<table border="1">
    <tr>
        <th align="center">Ref.</th>
        <th>Funktion</th>
        <th colspan="2">Beschrieb</th>
        <th>Berechtigung</th>
    </tr>
    <tr>
        <td align="center">1</td>
        <td>Rückmeldung Prozesswert</td>
        <td colspan="2">Messwert / Istwert als Zahl mit <a href="#einheit">Einheit</a></td>
        <td>keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td align="center">2</td>
        <td>Slider Prozesswert</td>
        <td colspan="2">Messwert / Istwert als <a href="Global/Basic/PvaSlider.md">Slider</a> dargestellt</td>
        <td>keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td align="center" rowspan="2">3</td>
        <td rowspan="2">Rückmeldung Alarm tief</td>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/Al.png" width="80"></td>
        <td>Alarm tief nicht ausgelöst</td>
        <td rowspan="2">keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/AlActive.png" width="80"></td>
        <td>Alarm tief ausgelöst</td>
    </tr>
    <tr>
        <td align="center" rowspan="2">4</td>
        <td rowspan="2">Rückmeldung Warnung tief</td>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/Wl.png" width="80"></td>
        <td>Warnung tief nicht ausgelöst</td>
        <td rowspan="2">keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/WlActive.png" width="80"></td>
        <td>Warnung tief ausgelöst</td>
    </tr>
    <tr>
        <td align="center" rowspan="2">5</td>
        <td rowspan="2">Rückmeldung Warnung hoch</td>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/Wh.png" width="80"></td>
        <td>Warnung hoch nicht ausgelöst</td>
        <td rowspan="2">keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/WhActive.png" width="80"></td>
        <td>Warnung hoch ausgelöst</td>
    </tr>
    <tr>
        <td align="center" rowspan="2">6</td>
        <td rowspan="2">Rückmeldung Alarm hoch</td>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/Ah.png" width="80"></td>
        <td>Alarm hoch nicht ausgelöst</td>
        <td rowspan="2">keine Bedienbarkeit</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/TypicalPVA/AhActive.png" width="80"></td>
        <td>Alarm hoch ausgelöst</td>
    </tr>
</table>

## Trend
Standard [Trendscreen](Global/Screens/Trend.md)

## Message
Standard [Messagescreen](Global/Screens/Message.md)

Die Standard Meldungen die das Typical mit sich bringt findet man [[hier]](Global/Meldetexte.md#pva)

## Limit
Auf dem Screen Limit kann die Auslösung der verschiedenen Alarme konfiguriert werden. 
<div style="position: relative; width: 100%; max-width: 800px;" id="picLimit">
    <img src="../../.content/HmiGrafics/TypicalPVA/Limit.png" style="width: 90%;" alt="ScreenLimit">

  <a href="">
    <div style="position: absolute; left: 17.5%; top: 0%; transform: translate(0%, 0%); width: 14.2%; height: 95%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">1</span>
    </div>
  </a>
  <a href="">
    <div style="position: absolute; left: 32.4%; top: 0%; transform: translate(0%, 0%); width: 13.8%; height: 95%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">2</span>
    </div>
  </a>
  <a href="">
    <div style="position: absolute; left: 46.9%; top: 0%; transform: translate(0%, 0%); width: 13.9%; height: 95%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">3</span>
    </div>
  </a>
  <a href="">
    <div style="position: absolute; left: 61.5%; top: 0%; transform: translate(0%, 0%); width: 13.9%; height: 95%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">4</span>
    </div>
  </a>
    <a href="">
    <div style="position: absolute; left: 76.1%; top: 0%; transform: translate(0%, 0%); width: 13.3%; height: 95%; background-color: rgba(255, 119, 0, 0.5); border: 3px solid orange; border-radius: 0%; color: white; text-align: center; cursor: pointer; display: grid; place-items: center;">
        <span style="background-color: orange; border-radius: 50%; font-weight: bold; font-size: 150%; display: flex; justify-content: center; align-items: center; width: 1.5em; height: 1.5em;">5</span>
    </div>
  </a>
</div>

<table border="1">
    <tr>
        <th align="center">Ref.</th>
        <th>Funktion</th>
        <th colspan="3">Beschrieb</th>
        <th>Berechtigung</th>
    </tr>
    <tr>
        <td align="center" rowspan="4">1</td>
        <td rowspan="4">Befehl & Rückmeldung Schaltart</td>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAnalogDigital/Analog.png" width="100%"></td>
        <td colspan="2">analoge Schalthysterese, Umschaltung zu digitaler Schaltpunkt mit Klick auf rechtes Symbol möglich</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAnalogDigital/AnalogNoAuth.png" width="100%"></td>
        <td colspan="2">analoge Schalthysterese, Umschaltberechtigung zu digitaler Schaltpunkt fehlt</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAnalogDigital/Digital.png" width="100%"></td>
        <td colspan="2"><a href="#digitaler-schaltpunkt">digitaler Schaltpunkt</a>, Umschaltung zu analoge Schaltysterese mittels Klick auf linkes Symbol möglich</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAnalogDigital/DigitalNoAuth.png" width="100%"></td>
        <td colspan="2"><a href="#digitaler-schaltpunkt">digitaler Schaltpunkt</a>, Umschaltberechtigung zu analoge Schalthysterese fehlt</td>
    </tr>
    <tr>
        <td align="center">2</td>
        <td>Befehl & Rückmeldung Grenzwert</td>
        <td colspan="3">Grenzwert ab wann der Schaltpunkt auslöst (nur bei analoger Schalthysterese ersichtlich)</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center">3</td>
        <td>Befehl & Rückmeldung Hysterese</td>
        <td colspan="3"><a href = "#hysterese">Hysterese</a> ab wann der Schaltpunkt abfällt (nur bei analoger Schalthysterese ersichtlich)</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center">4</td>
        <td>Befehl & Rückmeldung Verzögerung</td>
        <td colspan="3">Schaltpunkt auslöseverzögerung (min. Überschreitungszeit des Grenzwert bis Schaltpunkt auslöst und nur bei analoger Schalthysterese ersichtlich)</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center" rowspan="4">5</td>
        <td rowspan="4">Befehl & Rückmeldung Status</td>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Aktiv.png" width="100%"></td>
        <td>Schaltpunkt aktiv, Deaktivierung mittels Klickauf auf Kreuz möglich</td>
        <td rowspan="2">Meldung wird abgegeben bei überschreitung des Schaltpunkts</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/AktivNoAuth.png" width="100%"></td>
        <td>Schaltpunkt aktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Inaktiv.png" width="100%"></td>
        <td>Schaltpunkt inaktiv, Aktivierung mittels Klick auf Hacken möglich</td>
        <td rowspan="2">keine Meldungen werden für diesen Schaltpunkt abgegeben</td>
    </tr>
    <tr>
        <td><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/InaktivNoAuth.png" width="100%"></td>
        <td>Schaltpunkt inaktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
</table>

### Digitaler Schaltpunkt
Ist ein digitaler Schaltpunkt eingestellt, bedeutet das, dass der Schaltpunkt von extern ausgelöst wird. Man hat also keine Einstellmöglichkeiten wie Hysterese oder Verzögerung. Dies wird vorallem bei Fail-Safe MWA benötigt. 

### Hysterese
Bei der Hysterese geht es um den Unterschied zwischen dem Punkt, an dem ein Signal einschaltet, und dem Punkt, an dem es wieder ausschaltet. Diese Differenz verhindert ein schnelles Hin- und Herschalten (Flattern) bei Grenzwerten.


>__Beispiel Schaltpunkt hoch__
>
>Bei Schaltpunkt hoch mit einem Grenzwert von beispielswiese 6.5 bar und einer Hysterese von 0.8 bar:
>- Wenn der Druck steigt und 6.5 bar erreicht, wird der Alarm aktiviert
Der Alarm bleibt aktiv, bis der Druck unter (6.5 - 0.8) = 5.7 bar fällt. Diese Differenz von 0.8 bar ist die Hysterese
>- die Hysterese wird absolut angegeben, bei hoch wird immer vom Grenzwert subtrahiert fürs Abfallen

>__Beispiel Schaltpunkt tief__
>
>Bei Schaltpunkt tief mit einem Grenzwert von beispielsweise 2.5 bar und einer Hysterese von 0.8 bar funktioniert es umgekehrt:
>- Wenn der Druck fällt und 2.5 bar erreicht, wird der Alarm aktiviert Der Alarm bleibt aktiv, bis der Druck über (2.5 + 0.8) = 3.3 bar steigt
>- die Hysterese wird absolut angegeben, bei den Schaltpunkten tief wird sie immer zum Grenzwert addiert

## Parameter

<div style="position: relative; width: 100%; max-width: 800px;" id="picParameter">
    <img src="../../.content/HmiGrafics/TypicalPVA/Parameter.png" style="width: 90%;" alt="ScreenParameter">
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 14%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">1</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 25.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">2</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 37%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">4</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 48.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">6</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 60%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">8</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 71.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">10</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 74.4%; top: 25.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">3</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 74.4%; top: 37%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">5</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 74.4%; top: 48.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">7</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 74.4%; top: 60%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">9</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 74.4%; top: 71.5%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">11</div>
  </a>
  <a href="#modus">
      <div style="position: absolute; left: 27.4%; top: 94%; transform: translate(-50%, -50%); width: 1.5em; height: 1.5em; background-color:rgba(255, 119, 0, 0.5); border-radius: 50%; color: white; cursor: pointer; font-weight: bold; display: flex; justify-content: center; align-items: center; font-size: 150%;">12</div>
  </a>
</div>
<table border="1">
    <tr>
        <th align="center">Ref.</th>
        <th>Funktion</th>
        <th colspan="3">Beschrieb</th>
        <th>Berechtigung</th>
    </tr>
    <tr>
        <td align="center" rowspan="5">1</td>
        <td rowspan="5">Auswahl Messsignal</td>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/TypicalPVA/Signal1.png" width="100%"></td>
        <td colspan="2">Skalierung des Signals auf den konfigurierten Minimal- und Maximalwert des Messbereichs für <b>unipolare Signale<b></td>
        <td rowspan="5">30 - Parametrieren</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/TypicalPVA/Signal2.png" width="100%"></td>
        <td colspan="2">Bidirektionale Skalierung, wobei der Nullpunkt in der Mitte liegt und die negativen/positiven Signalwerte auf entsprechende Messwertbereiche abgebildet werden für <b>bipolare Signale<b></td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/TypicalPVA/Signal3.png" width="100%"></td>
        <td colspan="2">Widerstandsmessung wobei der Widerstand für höhere Genauigkeit durch 10 geteilt wird</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/TypicalPVA/Signal4.png" width="100%"></td>
        <td colspan="2">Widerstandsmessung wobei der Widerstand für höhere Genauigkeit durch 100 geteilt wird</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/TypicalPVA/Signal5.png" width="100%"></td>
        <td colspan="2">Temperaturabhängiger Widerstand wird mittels charakteristischer Kennlinie auf entsprechende Temperaturwerte umgerechnet</td>
    </tr>
    <tr>
        <td align="center">2</td>
        <td>Befehl & Rückmeldung Messwert Minimum</td>
        <td colspan="3">Minimaler Signalwert entspricht diesem Wert</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center">3</td>
        <td>Befehl & Rückmeldung Messwert Maximum</td>
        <td colspan="3">Maximaler Signalwert entspricht diesem Wert</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center">4</td>
        <td>Befehl & Rückmeldung Korrektur</td>
        <td colspan="3">Absolute Korrektur (Offset) zum Messwert</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center">5</td>
        <td>Befehl & Rückmeldung <p id="einheit">Einheit</p></td>
        <td colspan="3">Einheit der Prozesswerte im Faceplate</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center" rowspan="4">6</td>
        <td rowspan="4">Befehl & Rückmeldung Simulation Aktiv / Inaktiv</td>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Aktiv.png" width="100%"></td>
        <td>Simulation aktiv, Deaktivierung mittels Klick auf Kreuz möglich</td>
        <td rowspan="2">Echter Messwert wird vom Simulationswert überschrieben</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/AktivNoAuth.png" width="100%"></td>
        <td>Simulation aktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Inaktiv.png" width="100%"></td>
        <td>Simulation inaktiv, Aktivierung mittels Klick auf Haken möglich</td>
        <td rowspan="2">Keine Überschreibung des Messwerts durch den Simulationswert</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/InaktivNoAuth.png" width="100%"></td>
        <td>Simulation inaktiv, Umschaltberechtigung zur Aktivierung fehlt</td>
    </tr>
    <tr>
        <td align="center">7</td>
        <td>Befehl & Rückmeldung Simulationswert</td>
        <td colspan="3">Simulationswert der den Messwert ersetzt (nur wenn die Simulation aktiviert ist)</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center" rowspan="4">8</td>
        <td rowspan="4">Befehl & Rückmeldung Ersatzwert Aktiv / Inaktiv</td>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Aktiv.png" width="100%"></td>
        <td>Ersatzwert aktiv, Deaktivierung mittels Klick auf Kreuz möglich</td>
        <td rowspan="2">Ersetzt den Messwert mit dem Ersatzwert wenn das Messsignal ausfällt</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/AktivNoAuth.png" width="100%"></td>
        <td>Ersatzwert aktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Inaktiv.png" width="100%"></td>
        <td>Ersatzwert inaktiv, Aktivierung mittels Klick auf Haken möglich</td>
        <td rowspan="2">Kein Ersetzen des Messwerts wenn das Messsignal ausfällt</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/InaktivNoAuth.png" width="100%"></td>
        <td>Ersatzwert inaktiv, Umschaltberechtigung zur Aktivierung fehlt</td>
    </tr>
    <tr>
        <td align="center">9</td>
        <td>Befehl & Rückmeldung  Ersatzwert</td>
        <td colspan="3">Ersatzwert der den Messwert ersetzt wenn das Messsignal ausfällt (nur wenn der Ersatzwert aktiviert ist)</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center" rowspan="4">10</td>
        <td rowspan="4">Befehl & Rückmeldung  Tiefpassfilter Aktiv / Inaktiv</td>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Aktiv.png" width="100%"></td>
        <td>Tiefpassfilter aktiv, Deaktivierung mittels Klick auf Kreuz möglich</td>
        <td rowspan="2">Glättet Messwerte durch Dämpfung hochfrequenter Signalanteile</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/AktivNoAuth.png" width="100%"></td>
        <td>Tiefpassfilter aktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Inaktiv.png" width="100%"></td>
        <td>Tiefpassfilter inaktiv, Aktivierung mittels Klick auf Haken möglich</td>
        <td rowspan="2">Keine Glättung der Messwerte</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/InaktivNoAuth.png" width="100%"></td>
        <td>Tiefpassfilter inaktiv, Umschaltberechtigung zur Aktivierung fehlt</td>
    </tr>
    <tr>
        <td align="center">11</td>
        <td>Befehl & Rückmeldung Verzögerung</td>
        <td colspan="3">Zeitkonstante für den Tiefpassfilter in Sekunden</td>
        <td>30 - Parametrieren</td>
    </tr>
    <tr>
        <td align="center" rowspan="4">12</td>
        <td rowspan="4">Befehl & Rückmeldung Meldesperre Aktiv / Inaktiv</td>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Aktiv.png" width="100%"></td>
        <td>Meldesperre aktiv, Deaktivierung mittels Klick auf Kreuz möglich</td>
        <td rowspan="2">Alarme und Warnungen werden unterdrückt</td>
        <td rowspan="4">30 - Parametrieren</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/AktivNoAuth.png" width="100%"></td>
        <td>Meldesperre aktiv, Umschaltberechtigung zur Deaktivierung fehlt</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/Inaktiv.png" width="100%"></td>
        <td>Meldesperre inaktiv, Aktivierung mittels Klick auf Haken möglich</td>
        <td rowspan="2">Alarme und Warnungen werden ausgegeben</td>
    </tr>
    <tr>
        <td style="padding: 8px; text-align: center;"><img src="../../.content/HmiGrafics/GraficsGeneral/switch/swAktivInaktiv/InaktivNoAuth.png" width="100%"></td>
        <td>Meldesperre inaktiv, Umschaltberechtigung zur Aktivierung fehlt</td>
    </tr>
</table>

## Message Group
Standard [Message Group](Global/Screens/MessageGroup.md)

# Programmierung Übersicht

# Historie
|Datum      |Autor |Kommentar        |
|:----------|:-----|:----------------|
|22.04.2025 |leke  |Erstdokumentation|
||||