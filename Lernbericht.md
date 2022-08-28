# Lern-Bericht
Joel Jütte

## Einleitung

Im Modul 133 geht es um Webapplikationen mit Session Handling.

## Was habe ich gelernt?

Von dem neu Gelernten, finde ich den "ProppertyActionListener", mit welchem man Daten im Hintergrund einfach weitergeben kann, besonders spannend. 

## Beschreibung

Der "ProppertyActionListener" ist ein "xhtml" Tag, welcher folgende Syntax hat:
```xhtml
<f:setPropertyActionListener target="" value=""/>
```
Mit dem Attribut "value" kann ein Wert gesetzt werden, welcher übergeben werden soll. Mit dem Attribut "target" kann der Ort bestimmt werden, wo das "value" gespeichert werden soll. Der "ProppertyActionListener" wird zusammen mit "commandLink" und "-Button" in einem "Form" verwendet.

In meinem Beispiel wird die Information des angeklickten Bildes in einer "Bean klasse" gespeichert. Somit kann ich auf einer anderen Seite diese Information verwenden, um einen Charakter zu gestalten.
Hier der Code der ersten Seite: 
```xhtml
<h1>Wilkommen zum Charakter Designer</h1>
<p>Klicken Sie jeweils auf das Bild mit dem Style, welcher Ihnen gefällt.</p>
<p>Hier geht es um die Hautfarbe</p>
  <h:form>
    <h:commandLink action = "page1">
      <h:graphicImage value="/9954_PokemonBilder/d.png" width="200"/>
      <f:setPropertyActionListener target="#{bean.hautfarbe}" value="d"/>
    </h:commandLink>
    <h:commandLink action = "page1">
      <h:graphicImage value="/9954_PokemonBilder/h.png" width="200"/>
      <f:setPropertyActionListener target="#{bean.hautfarbe}" value="h"/>
    </h:commandLink>
  </h:form>
```
Das sieht im Browser so aus:

![LernberichtScreenshot](https://user-images.githubusercontent.com/69578012/187091634-0dd799f6-b37d-44a0-8b2b-c27da5401557.png)

## Verifikation

Im Code kann man sehen, wie die Information der Bilder über die "ProppertyActionListener" in eine "Bean Klasse" weitergegeben werden. Ich habe gelernt, dass die "values" via "Setter" gespeichert und danach auf der zweiten Seite via "Getter" ausgelesen werden können.

# Reflektion zum Arbeitsprozess

Das Prinzip des "ProppertyActionListener" habe ich schnell begriffen und auch umsetzen können. 
Leider habe ich es nicht geschafft, den "ProppertyActionListener" bei "Radiobuttons" oder "Dropdownauswahlen" zu verwenden. Damit hätte ich mein Projekt noch etwas dynamischer gestalten können. 

**VBV**: Bei Gelegenheit werde ich mich bei unserem Lehrer darüber informieren, ob, und wenn ja wie, ich den "ProppertyChangeListener" auch für "Radiobuttons" und "Dropdownauswahlen" verwenden kann.
