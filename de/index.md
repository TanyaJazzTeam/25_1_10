---
layout: Post
title: Web-Vitals
description: Wichtige Metriken für eine gesunde Website
hero: image/admin/BHaoqqR73jDWe6FL2kfw.png
authors:
  - philippwalton
date: '2020-04-30'
updated: '2020-07-21'
tags:
  - Metriken
  - Leistung
  - Web-Vitals
---

Die Optimierung der Qualität der Benutzererfahrung ist der Schlüssel zum langfristigen Erfolg jeder Website im Web. Ganz gleich, ob Sie Geschäftsinhaber, Vermarkter oder Entwickler sind, Web Vitals kann Ihnen dabei helfen, die Erfahrung Ihrer Website zu quantifizieren und Verbesserungsmöglichkeiten zu identifizieren.

## Überblick

Web Vitals ist eine Initiative von Google, um eine einheitliche Anleitung für Qualitätssignale bereitzustellen, die für die Bereitstellung einer großartigen Benutzererfahrung im Web unerlässlich sind.

Google hat im Laufe der Jahre eine Reihe von Tools bereitgestellt, um die Leistung zu messen und zu melden. Einige Entwickler sind Experten im Umgang mit diesen Tools, während es für andere schwierig ist, mit der Fülle an Tools und Metriken Schritt zu halten.

Websitebesitzer sollten keine Performance-Gurus sein müssen, um die Qualität der Erfahrung zu verstehen, die sie ihren Benutzern bieten. Die Web Vitals-Initiative zielt darauf ab, die Landschaft zu vereinfachen und Websites dabei zu helfen, sich auf die Metriken zu konzentrieren, die am wichtigsten sind, die **Core Web Vitals** .

## Core Web Vitals

Core Web Vitals sind die Teilmenge von Web Vitals, die für alle Webseiten gelten, von allen Websitebesitzern gemessen werden sollten und in allen Google-Tools angezeigt werden. Jeder der Core Web Vitals stellt eine bestimmte Facette der Benutzererfahrung [dar](/user-centric-performance-metrics/#how-metrics-are-measured) , ist vor Ort messbar und spiegelt die reale Erfahrung eines kritischen [benutzerzentrierten](/user-centric-performance-metrics/#how-metrics-are-measured) Ergebnisses wider.

Die Metriken, aus denen sich Core Web Vitals zusammensetzt, werden sich im Laufe der Zeit [weiterentwickeln](#evolving-web-vitals) . Das aktuelle Set für 2020 konzentriert sich auf drei Aspekte der Benutzererfahrung – *Laden* , *Interaktivität* und *visuelle Stabilität* – und umfasst die folgenden Metriken (und ihre jeweiligen Schwellenwerte):

<div class="w-stack w-stack--center w-stack--md">
<img src="lcp_ux.svg" width="400px" height="350px" alt="Größte Empfehlungen für Contentful Paint-Schwellenwerte"><img src="fid_ux.svg" width="400px" height="350px" alt="Empfehlungen für den Schwellenwert für die erste Eingangsverzögerung"><img src="cls_ux.svg" width="400px" height="350px" alt="Kumulierte Grenzwertempfehlungen für die Layout-Verschiebung">
</div>

- **[Largest Contentful Paint (LCP)](/lcp/)** : misst die *Ladeleistung* . Um eine gute Benutzererfahrung zu bieten, sollte LCP innerhalb von **2,5 Sekunden** nach dem ersten Laden der Seite erfolgen.
- **[First Input Delay (FID)](/fid/)** : Misst die *Interaktivität* . Um eine gute Benutzererfahrung zu bieten, sollten Seiten eine FID von weniger als **100 Millisekunden** haben .
- **[Cumulative Layout Shift (CLS)](/cls/)** : Misst die *visuelle Stabilität* . Um eine gute Benutzererfahrung zu bieten, sollten Seiten einen CLS von weniger als **0,1 beibehalten.**

Um sicherzustellen, dass Sie das empfohlene Ziel für die meisten Ihrer Benutzer erreichen, ist für jede der oben genannten Metriken das **75. Perzentil** der Seitenladevorgänge, segmentiert nach Mobil- und Desktop-Geräten, ein guter Schwellenwert.

Tools, die die Einhaltung von Core Web Vitals bewerten, sollten eine Seite als bestanden betrachten, wenn sie die empfohlenen Ziele im 75. Perzentil für alle der drei oben genannten Metriken erfüllt.

{% Aside %} Um mehr über die Forschung und Methodik hinter diesen Empfehlungen zu erfahren, siehe: [Definieren der Schwellenwerte für Core Web Vitals-Metriken](/defining-core-web-vitals-thresholds/) {% endAside %}

### Tools zum Messen und Berichten von Core Web Vitals

Google ist der Ansicht, dass die Core Web Vitals für alle Web-Erlebnisse von entscheidender Bedeutung sind. Aus diesem Grund verpflichtet es sich, diese Metriken [in all seinen beliebten Tools zu](/vitals-tools/) präsentieren . In den folgenden Abschnitten wird beschrieben, welche Tools die Core Web Vitals unterstützen.

#### Feldtools zur Messung von Core Web Vitals

Der[Chrome User Experience Report](https://developers.google.com/web/tools/chrome-user-experience-report) sammelt anonymisierte, echte Benutzermessdaten für jedes Core Web Vital. Diese Daten ermöglichen es Websitebesitzern, ihre Leistung schnell zu bewerten, ohne dass sie Analysen auf ihren Seiten manuell instrumentieren müssen, und unterstützen Tools wie [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) und den [Core Web Vitals-Bericht](https://support.google.com/webmasters/answer/9205520) der Search Console .

<div class="w-table-wrapper">
  <table>
    <tr>
      <td> </td>
      <td>LCP</td>
      <td>FID</td>
      <td>CLS</td>
    </tr>
    <tr>
      <td><a href="https://developers.google.com/web/tools/chrome-user-experience-report">Bericht zur Chrome-Benutzererfahrung</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
    <tr>
      <td><a href="https://developers.google.com/speed/pagespeed/insights/">PageSpeed-Einblicke</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
    <tr>
      <td><a href="https://support.google.com/webmasters/answer/9205520">Search Console (Core Web Vitals-Bericht)</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
  </table>
</div>

{% Aside %} Anleitungen zur Verwendung dieser Tools und dazu, welches Tool für Ihren Anwendungsfall geeignet ist, finden Sie unter: Erste Schritte [mit der Messung von Web Vitals](/vitals-measurement-getting-started/) {% endAside %}

Die vom Chrome User Experience Report bereitgestellten Daten bieten eine schnelle Möglichkeit, die Leistung von Websites zu bewerten, bieten jedoch nicht die detaillierte Telemetrie pro Seitenaufruf, die häufig erforderlich ist, um Regressionen genau zu diagnostizieren, zu überwachen und schnell darauf zu reagieren. Aus diesem Grund empfehlen wir dringend, dass Websites ihre eigene Überwachung von echten Benutzern einrichten.

#### Messen Sie Core Web Vitals in JavaScript

Jeder der Core Web Vitals kann in JavaScript unter Verwendung von Standard-Web-APIs gemessen werden.

Der einfachste Weg, alle Core Web Vitals zu messen, ist die Verwendung der [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) JavaScript-Bibliothek, einem kleinen, produktionsbereiten Wrapper um die zugrunde liegenden Web-APIs, der jede Metrik so misst, dass sie genau mit der von allen gemeldeten übereinstimmt Die oben aufgeführten Google-Tools.

Mit der [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek ist das Messen jeder Metrik so einfach wie das Aufrufen einer einzelnen Funktion (siehe die Dokumentation für die vollständige [Verwendung](https://github.com/GoogleChrome/web-vitals#usage) und [API](https://github.com/GoogleChrome/web-vitals#api) -Details):

```js
import {getCLS, getFID, getLCP} from 'web-vitals';

function sendToAnalytics(metric) {
  const body = JSON.stringify(metric);
  // Use `navigator.sendBeacon()` if available, falling back to `fetch()`.
  (navigator.sendBeacon && navigator.sendBeacon('/analytics', body)) ||
      fetch('/analytics', {body, method: 'POST', keepalive: true});
}

getCLS(sendToAnalytics);
getFID(sendToAnalytics);
getLCP(sendToAnalytics);
```

Sobald Sie Ihre Website so konfiguriert haben, dass sie die [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek verwendet, um Ihre Core Web Vitals-Daten zu messen und an einen Analyseendpunkt zu senden, besteht der nächste Schritt darin, diese Daten zu aggregieren und zu melden, um zu sehen, ob Ihre Seiten die empfohlenen Schwellenwerte für erfüllen mindestens 75 % der Seitenaufrufe.

Während einige Analyseanbieter integrierte Unterstützung für Core Web Vitals-Metriken haben, sollten selbst diejenigen, die dies nicht tun, grundlegende benutzerdefinierte Metrikfunktionen enthalten, mit denen Sie Core Web Vitals in ihrem Tool messen können.

Ein Beispiel hierfür ist der [Web Vitals Report](https://github.com/GoogleChromeLabs/web-vitals-report) , der es Websitebesitzern ermöglicht, ihre Core Web Vitals mit Google Analytics zu messen. Anleitungen zum Messen von Core Web Vitals mit anderen Analysetools finden Sie unter [Best Practices für das Messen von Web Vitals im Feld](/vitals-field-measurement-best-practices/) .

Mit der [Web Vitals Chrome-Erweiterung](https://github.com/GoogleChrome/web-vitals-extension) können Sie auch Berichte zu jedem der Core Web Vitals erstellen, ohne Code schreiben zu müssen. Diese Erweiterung verwendet die [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek, um jede dieser Metriken zu messen und sie den Benutzern anzuzeigen, während sie im Internet surfen.

Diese Erweiterung kann hilfreich sein, um die Leistung Ihrer eigenen Websites, der Websites Ihrer Mitbewerber und des gesamten Webs zu verstehen.

<div class="w-table-wrapper">
  <table>
    <thead>
      <tr>
        <th> </th>
        <th>LCP</th>
        <th>FID</th>
        <th>CLS</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a href="https://github.com/GoogleChrome/web-vitals">Web-Vitals</a></td>
        <td>✔</td>
        <td>✔</td>
        <td>✔</td>
      </tr>
      <tr>
        <td><a href="https://github.com/GoogleChrome/web-vitals-extension">Web Vitals-Erweiterung</a></td>
        <td>✔</td>
        <td>✔</td>
        <td>✔</td>
      </tr>
    </tbody>
  </table>
</div>

Alternativ können Entwickler, die diese Metriken lieber direkt über die zugrunde liegenden Web-APIs messen möchten, auf diese Metrikleitfäden für Implementierungsdetails verweisen:

- [Messen Sie LCP in JavaScript](/lcp/#measure-lcp-in-javascript)
- [FID in JavaScript messen](/fid/#measure-fid-in-javascript)
- [Messen Sie CLS in JavaScript](/cls/#measure-cls-in-javascript)

{% Aside %} Weitere Anleitungen zur Messung dieser Metriken mit beliebten Analysediensten (oder Ihren eigenen internen Analysetools) finden Sie unter: [Best Practices for Measuring Web Vitals in the field](/vitals-field-measurement-best-practices/) {% endAside %}

#### Lab-Tools zur Messung von Core Web Vitals

Während alle Core Web Vitals in erster Linie Feldmetriken sind, sind viele von ihnen auch im Labor messbar.

Labormessungen sind die beste Methode, um die Leistung von Funktionen während der Entwicklung zu testen – bevor sie für Benutzer freigegeben werden. Es ist auch der beste Weg, Leistungsregressionen zu erkennen, bevor sie auftreten.

Die folgenden Tools können verwendet werden, um die Core Web Vitals in einer Laborumgebung zu messen:

<div class="w-table-wrapper">
  <table>
    <thead>
      <tr>
        <th> </th>
        <th>LCP</th>
        <th>FID</th>
        <th>CLS</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a href="https://developers.google.com/web/tools/chrome-devtools">Chrome-Entwicklungstools</a></td>
        <td>✔</td>
        <td>✘ (stattdessen <a href="/tbt/">TBT</a> verwenden)</td>
        <td>✔</td>
      </tr>
      <tr>
        <td><a href="https://developers.google.com/web/tools/lighthouse">Leuchtturm</a></td>
        <td>✔</td>
        <td>✘ (stattdessen <a href="/tbt/">TBT</a> verwenden)</td>
        <td>✔</td>
      </tr>
    </tbody>
  </table>
</div>

{% Aside %} Tools wie Lighthouse, die Seiten in einer simulierten Umgebung ohne Benutzer laden, können FID nicht messen (es gibt keine Benutzereingabe). Die Metrik der Total Blocking Time (TBT) ist jedoch im Labor messbar und ein hervorragender Proxy für FID. Leistungsoptimierungen, die TBT im Labor verbessern, sollten FID im Feld verbessern (siehe Leistungsempfehlungen unten). {% endAside %}

Während Labormessungen ein wesentlicher Bestandteil der Bereitstellung großartiger Erfahrungen sind, sind sie kein Ersatz für Feldmessungen.

Die Leistung einer Website kann je nach den Gerätefunktionen eines Benutzers, seinen Netzwerkbedingungen, den möglicherweise auf dem Gerät ausgeführten anderen Prozessen und der Art und Weise, wie er mit der Seite interagiert, erheblich variieren. Tatsächlich kann die Punktzahl jeder der Core Web Vitals-Metriken durch die Benutzerinteraktion beeinflusst werden. Nur die Feldmessung kann das vollständige Bild genau erfassen.

### Empfehlungen zur Verbesserung Ihrer Punktzahl

Nachdem Sie die Core Web Vitals gemessen und verbesserungswürdige Bereiche identifiziert haben, besteht der nächste Schritt in der Optimierung. Die folgenden Leitfäden bieten spezifische Empfehlungen zur Optimierung Ihrer Seiten für die einzelnen Core Web Vitals:

- [LCP optimieren](/optimize-lcp/)
- [FID optimieren](/optimize-fid/)
- [CLS optimieren](/optimize-cls/)

## Andere Web-Vitals

Während die Core Web Vitals die kritischen Metriken für das Verständnis und die Bereitstellung einer großartigen Benutzererfahrung sind, gibt es auch andere wichtige Metriken.

Diese anderen Web Vitals dienen oft als Proxy- oder ergänzende Metriken für die Core Web Vitals, um einen größeren Teil der Erfahrung zu erfassen oder bei der Diagnose eines bestimmten Problems zu helfen.

Beispielsweise sind die Metriken [Time to First Byte (TTFB)](/time-to-first-byte/) und [First Contentful Paint (FCP)](/fcp/) beide wichtige Aspekte der *Ladeerfahrung* und beide nützlich bei der Diagnose von Problemen mit LCP (langsame [Serverantwortzeiten](/overloaded-server/) bzw. [Ressourcen, die das Rendern blockieren](/render-blocking-resources/) ). .

In ähnlicher Weise sind Metriken wie [Total Blocking Time (TBT)](/tbt/) und [Time to Interactive (TTI)](/tti/) Labormetriken, die für das Erkennen und Diagnostizieren potenzieller *Interaktivitätsprobleme* , die sich auf FID auswirken, von entscheidender Bedeutung sind. Sie sind jedoch nicht Teil des Core Web Vitals-Sets, da sie weder vor Ort messbar sind noch ein [benutzerzentriertes](/user-centric-performance-metrics/#how-metrics-are-measured) Ergebnis widerspiegeln.

## Sich entwickelnde Web-Vitals

Web Vitals und Core Web Vitals stellen die besten verfügbaren Signale dar, über die Entwickler heute verfügen, um die Qualität der Erfahrung im gesamten Web zu messen, aber diese Signale sind nicht perfekt und zukünftige Verbesserungen oder Ergänzungen sollten erwartet werden.

Die **Core Web Vitals** sind für alle Webseiten relevant und werden in allen relevanten Google-Tools angezeigt. Änderungen an diesen Metriken werden weitreichende Auswirkungen haben; Daher sollten Entwickler davon ausgehen, dass die Definitionen und Schwellenwerte der Core Web Vitals stabil sind und dass Aktualisierungen im Voraus angekündigt werden und eine vorhersehbare jährliche Kadenz haben.

Die anderen Web Vitals sind oft kontext- oder werkzeugspezifisch und möglicherweise experimenteller als die Core Web Vitals. Daher können sich ihre Definitionen und Schwellenwerte häufiger ändern.

Für alle Web Vitals werden Änderungen in diesem öffentlichen [CHANGELOG](http://bit.ly/chrome-speed-metrics-changelog) eindeutig dokumentiert.
