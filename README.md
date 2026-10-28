# Tabula Pyrenaei · Tiles de relieve

Teselas ráster de relieve sombreado del Pirineo y su entorno, preparadas para
los mapas de [tabulapyrenaei.eu](https://tabulapyrenaei.eu).

## Contenido

- Esquema XYZ (`{z}/{x}/{y}.png`) en EPSG:3857 (Web Mercator), teselas de 256 px
  en formato PNG.
- Niveles de zoom 7 a 12.
- Cobertura aproximada: de 41° a 44° N y de 3° O a 4° E.
- Relieve sombreado elaborado a partir del modelo digital de elevaciones
  Copernicus GLO-30 (30 m). Sobre él se dibujan, como manchas de color, el mar
  según una línea de costa aproximada de hace unos 2000 años y una red fluvial
  adaptada a una reconstrucción de sus cursos en la Antigüedad.

## Uso en Leaflet

```js
L.tileLayer('https://pyrenaeus.github.io/tabula-pyrenaei-tiles/{z}/{x}/{y}.png', {
  minZoom: 7,
  maxNativeZoom: 12,
  maxZoom: 18,
  bounds: [[40.9998611, -3.0001389], [44.0001389, 4.0001389]],
  attribution: '<a href="https://github.com/pyrenaeus/tabula-pyrenaei-tiles#readme">Créditos</a> · © <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);
```

Si se reutilizan estas teselas, deben mostrarse junto al mapa los créditos
indicados en este documento. Se recomienda enlazar a una página que los
reproduzca completos.

## Créditos

### Relieve

Produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus
Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European
Union and ESA; all rights reserved.

The organisations in charge of the Copernicus programme by law or by
delegation do not incur any liability for any use of the Copernicus
WorldDEM-30.

Licencia: «Licence for the use of the Copernicus WorldDEM-30» (documentación
de Copernicus Data Space).

### Hidrografía

Los cursos fluviales dibujados sobre el relieve proceden de las fuentes
siguientes. Han sido adaptados y modificados por Tabula Pyrenaei para
ajustarlos a una reconstrucción de su trazado en la Antigüedad.

- **Francia:** Sandre / Agences de l'Eau, «Masses d'eau cours d'eau –
  Métropole – Version État des Lieux 2013» (masas de agua derivadas del tema
  hidrográfico BD CARTHAGE®). Ficha actualizada el 12-05-2021. Licence
  Ouverte (Etalab).
- **País Vasco:** Eusko Jaurlaritza / Gobierno Vasco (capa
  CT_0202LRiosCAPV_ETRS89).
- **Cataluña (cuencas internas):** Agència Catalana de l'Aigua,
  «Rius_CARACT. Caracterització de masses d'aigua superficials i anàlisi del
  risc d'incompliment dels objectius de la DMA (2000/60/CE) a les conques
  internes de Catalunya», v.3 (2009). Red fluvial extraída de la base
  topográfica 1:50.000 del Institut Cartogràfic de Catalunya (ICC, 2002). Los
  metadatos del conjunto no declaran condiciones de uso.
- **Cuenca del Ebro:** Confederación Hidrográfica del Ebro, «Red hidrográfica»
  (digitalizada a partir de las hojas 1:50.000 del Servicio Geográfico del
  Ejército). Licencia indicada por la CHE: compatible con CC BY 4.0, con
  remisión a las condiciones de licencia de uso del IGN.

Las modificaciones son responsabilidad de Tabula Pyrenaei. Esta reutilización
no tiene carácter oficial ni implica reconocimiento o aval por parte de los
productores de los datos originales.

### Costa y mar

La línea de costa y las zonas de mar dibujadas corresponden a una aproximación
a la situación de en torno al siglo I y se han elaborado a partir de:

- **Costa vasca:** Eusko Jaurlaritza / Gobierno Vasco (capas
  CT_0203GMasaAguaCosterasCAPV_ETRS89 y
  CT_0208GMasaAguaTransicionCAPV_ETRS89).
- **Resto de la costa:** © [OpenStreetMap](https://www.openstreetmap.org/copyright)
  contributors. Datos disponibles bajo la Open Database Licence (ODbL).

Estos datos han sido modificados por Tabula Pyrenaei para ajustarlos a esa
reconstrucción; las teselas son una obra producida a partir de ellos.

## Licencia

La aportación de Tabula Pyrenaei (el tratamiento cartográfico y las teselas) se
distribuye bajo la licencia [Creative Commons Atribución 4.0 Internacional
(CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.es). Los datos de
terceros citados en el apartado de créditos conservan sus propias condiciones.
