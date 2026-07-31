FROM rocker/shiny:latest

# Instalamos las librerías del sistema
RUN apt-get update && apt-get install -y \
    libcurl4-gnutls-dev \
    libssl-dev \
    libxml2-dev \
    libudunits2-dev \
    libgdal-dev \
    libgeos-dev \
    libproj-dev \
    && rm -rf /var/lib/apt/lists/*

# Instalamos los paquetes de R
RUN R -e "install.packages(c('shiny', 'dplyr', 'ggplot2', 'leaflet', 'readxl', 'bslib', 'sf', 'tidyr'), repos='https://cloud.r-project.org/')"

WORKDIR /app
COPY . .

EXPOSE 10000

# El comando "." le dice a Shiny que busque app.R O la pareja ui.R/server.R en la carpeta actual
CMD ["R", "-e", "shiny::runApp('.', host = '0.0.0.0', port = as.numeric(Sys.getenv('PORT', 10000)))"]
<?xml version="1.0" encoding="UTF-8"?>
<kml xmlns="http://www.opengis.net/kml/2.2">
  <Document>
    <name>LA PLATA</name>
    <Style id="poly-006064-1200-77-normal">
      <LineStyle>
        <color>ff646000</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d646000</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-006064-1200-77-highlight">
      <LineStyle>
        <color>ff646000</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d646000</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-006064-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-006064-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-006064-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-0097A7-1200-77-normal">
      <LineStyle>
        <color>ffa79700</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4da79700</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-0097A7-1200-77-highlight">
      <LineStyle>
        <color>ffa79700</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4da79700</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-0097A7-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-0097A7-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-0097A7-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-0288D1-1200-77-normal">
      <LineStyle>
        <color>ffd18802</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4dd18802</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-0288D1-1200-77-highlight">
      <LineStyle>
        <color>ffd18802</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4dd18802</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-0288D1-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-0288D1-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-0288D1-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-0F9D58-1200-77-normal">
      <LineStyle>
        <color>ff589d0f</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d589d0f</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-0F9D58-1200-77-highlight">
      <LineStyle>
        <color>ff589d0f</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d589d0f</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-0F9D58-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-0F9D58-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-0F9D58-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-1A237E-1200-77-normal">
      <LineStyle>
        <color>ff7e231a</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d7e231a</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-1A237E-1200-77-highlight">
      <LineStyle>
        <color>ff7e231a</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d7e231a</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-1A237E-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-1A237E-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-1A237E-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-558B2F-1200-77-normal">
      <LineStyle>
        <color>ff2f8b55</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d2f8b55</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-558B2F-1200-77-highlight">
      <LineStyle>
        <color>ff2f8b55</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d2f8b55</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-558B2F-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-558B2F-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-558B2F-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-817717-1200-77-normal">
      <LineStyle>
        <color>ff177781</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d177781</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-817717-1200-77-highlight">
      <LineStyle>
        <color>ff177781</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d177781</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-817717-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-817717-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-817717-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-880E4F-1200-77-normal">
      <LineStyle>
        <color>ff4f0e88</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d4f0e88</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-880E4F-1200-77-highlight">
      <LineStyle>
        <color>ff4f0e88</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d4f0e88</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-880E4F-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-880E4F-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-880E4F-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-9C27B0-1200-77-normal">
      <LineStyle>
        <color>ffb0279c</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4db0279c</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-9C27B0-1200-77-highlight">
      <LineStyle>
        <color>ffb0279c</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4db0279c</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-9C27B0-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-9C27B0-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-9C27B0-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-A1C2FA-1200-77-normal">
      <LineStyle>
        <color>fffac2a1</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4dfac2a1</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-A1C2FA-1200-77-highlight">
      <LineStyle>
        <color>fffac2a1</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4dfac2a1</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-A1C2FA-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-A1C2FA-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-A1C2FA-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-A52714-1200-77-normal">
      <LineStyle>
        <color>ff1427a5</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d1427a5</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-A52714-1200-77-highlight">
      <LineStyle>
        <color>ff1427a5</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d1427a5</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-A52714-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-A52714-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-A52714-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-AFB42B-1200-77-normal">
      <LineStyle>
        <color>ff2bb4af</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d2bb4af</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-AFB42B-1200-77-highlight">
      <LineStyle>
        <color>ff2bb4af</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d2bb4af</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-AFB42B-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-AFB42B-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-AFB42B-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-C2185B-1200-77-normal">
      <LineStyle>
        <color>ff5b18c2</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d5b18c2</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-C2185B-1200-77-highlight">
      <LineStyle>
        <color>ff5b18c2</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d5b18c2</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-C2185B-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-C2185B-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-C2185B-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-E65100-1200-77-normal">
      <LineStyle>
        <color>ff0051e6</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d0051e6</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-E65100-1200-77-highlight">
      <LineStyle>
        <color>ff0051e6</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d0051e6</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-E65100-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-E65100-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-E65100-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-EDA29B-3001-120-normal">
      <LineStyle>
        <color>ff9ba2ed</color>
        <width>3.001</width>
      </LineStyle>
      <PolyStyle>
        <color>789ba2ed</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-EDA29B-3001-120-highlight">
      <LineStyle>
        <color>ff9ba2ed</color>
        <width>4.5015</width>
      </LineStyle>
      <PolyStyle>
        <color>789ba2ed</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-EDA29B-3001-120">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-EDA29B-3001-120-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-EDA29B-3001-120-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-F48FB1-1200-77-normal">
      <LineStyle>
        <color>ffb18ff4</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4db18ff4</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-F48FB1-1200-77-highlight">
      <LineStyle>
        <color>ffb18ff4</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4db18ff4</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-F48FB1-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-F48FB1-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-F48FB1-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-F57C00-1200-77-normal">
      <LineStyle>
        <color>ff007cf5</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d007cf5</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-F57C00-1200-77-highlight">
      <LineStyle>
        <color>ff007cf5</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d007cf5</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-F57C00-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-F57C00-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-F57C00-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-FF5252-1200-77-normal">
      <LineStyle>
        <color>ff5252ff</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d5252ff</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-FF5252-1200-77-highlight">
      <LineStyle>
        <color>ff5252ff</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d5252ff</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-FF5252-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-FF5252-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-FF5252-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Style id="poly-FFEA00-1200-77-normal">
      <LineStyle>
        <color>ff00eaff</color>
        <width>1.2</width>
      </LineStyle>
      <PolyStyle>
        <color>4d00eaff</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <Style id="poly-FFEA00-1200-77-highlight">
      <LineStyle>
        <color>ff00eaff</color>
        <width>1.8</width>
      </LineStyle>
      <PolyStyle>
        <color>4d00eaff</color>
        <fill>1</fill>
        <outline>1</outline>
      </PolyStyle>
    </Style>
    <StyleMap id="poly-FFEA00-1200-77">
      <Pair>
        <key>normal</key>
        <styleUrl>#poly-FFEA00-1200-77-normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#poly-FFEA00-1200-77-highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Placemark>
      <name>HERNANDEZ
</name>
      <description><![CDATA[Descripción: <br>nombre: HERNANDEZ<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-FFEA00-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>HERNANDEZ</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0072391,-34.9128742,0
              -57.9948864,-34.9016413,0
              -58.0049782,-34.8941507,0
              -58.011161,-34.8997583,0
              -58.0213779,-34.8921995,0
              -58.0256186,-34.8972705,0
              -58.029863,-34.902329,0
              -58.044467,-34.918063,0
              -58.0339592,-34.9254542,0
              -58.023286,-34.912726,0
              -58.010551,-34.915888,0
              -58.0072391,-34.9128742,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>ABASTO</name>
      <description><![CDATA[Descripción: <br>nombre: ABASTO<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-0F9D58-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>ABASTO</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.1616496,-34.9720405,0
              -58.12041,-35.004402,0
              -58.1783113,-35.0563772,0
              -58.145315,-35.0816998,0
              -58.1310006,-35.0691029,0
              -58.1238982,-35.0643718,0
              -58.0926781,-35.0356395,0
              -58.0933884,-35.0251738,0
              -58.0490651,-34.9847295,0
              -58.0608601,-34.9758074,0
              -58.0754525,-34.9648888,0
              -58.0827911,-34.9602288,0
              -58.0946786,-34.9527369,0
              -58.1131931,-34.940892,0
              -58.1176992,-34.9380073,0
              -58.1205057,-34.9362055,0
              -58.1616496,-34.9720405,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>SAN LORENZO
</name>
      <description><![CDATA[Descripción: <br>nombre: SAN LORENZO<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-AFB42B-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>SAN LORENZO</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.93358,-34.937005,0
              -57.9521755,-34.9539424,0
              -57.9530118,-34.9539169,0
              -57.959174,-34.959577,0
              -57.9158124,-34.9915988,0
              -57.9076826,-34.9841841,0
              -57.8985175,-34.9910806,0
              -57.8908234,-34.9842401,0
              -57.8953302,-34.9809396,0
              -57.8969395,-34.9869873,0
              -57.9009092,-34.986038,0
              -57.8985703,-34.978654,0
              -57.908285,-34.971487,0
              -57.8983236,-34.9624668,0
              -57.9158447,-34.9494266,0
              -57.9165206,-34.950007,0
              -57.93358,-34.937005,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>VILLA ELVIRA</name>
      <description><![CDATA[Descripción: <br>nombre: VILLA ELVIRA<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-F48FB1-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>VILLA ELVIRA</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9335156,-34.9370402,0
              -57.9165421,-34.9499894,0
              -57.9158662,-34.949409,0
              -57.8983451,-34.9624492,0
              -57.908263,-34.9714715,0
              -57.8985703,-34.978654,0
              -57.9009092,-34.986038,0
              -57.8969395,-34.9869873,0
              -57.8953517,-34.980922,0
              -57.8908234,-34.9842401,0
              -57.8756533,-34.9706231,0
              -57.860204,-34.957013,0
              -57.8555363,-34.9604734,0
              -57.84334,-34.948085,0
              -57.8616775,-34.9379114,0
              -57.8620745,-34.9377784,0
              -57.8624893,-34.9377305,0
              -57.8714571,-34.9378418,0
              -57.8717575,-34.9378242,0
              -57.8720579,-34.9377495,0
              -57.884199,-34.9332462,0
              -57.8844619,-34.9331803,0
              -57.8913164,-34.9319448,0
              -57.8920615,-34.9317624,0
              -57.8960255,-34.9304234,0
              -57.9048025,-34.9239774,0
              -57.9049998,-34.9235747,0
              -57.9125205,-34.9179984,0
              -57.9147145,-34.919947,0
              -57.9164935,-34.9215698,0
              -57.9249609,-34.9292789,0
              -57.9292702,-34.9331684,0
              -57.9313929,-34.9351043,0
              -57.9324381,-34.9360854,0
              -57.9335156,-34.9370402,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>MELCHOR ROMERO</name>
      <description><![CDATA[Descripción: <br>nombre: MELCHOR ROMERO<br><br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-1A237E-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>MELCHOR ROMERO
</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.1204899,-34.9362284,0
              -58.1190816,-34.9371254,0
              -58.1128536,-34.9410626,0
              -58.1072746,-34.9447212,0
              -58.0947952,-34.9526552,0
              -58.0890767,-34.9562605,0
              -58.0812509,-34.9612542,0
              -58.0754525,-34.9648888,0
              -58.0694822,-34.9693726,0
              -58.0591811,-34.9770082,0
              -58.0575476,-34.9783137,0
              -58.0490651,-34.9847295,0
              -58.0427674,-34.9790291,0
              -58.0495984,-34.9739559,0
              -58.0475901,-34.9721421,0
              -58.0407183,-34.9771136,0
              -58.0366298,-34.9733866,0
              -58.0377563,-34.9725778,0
              -58.0356856,-34.9706876,0
              -58.0345363,-34.9715415,0
              -58.0241984,-34.9622704,0
              -58.0149776,-34.9537898,0
              -58.0056773,-34.9453686,0
              -58.044467,-34.918063,0
              -58.0496245,-34.92347,0
              -58.0551713,-34.9282025,0
              -58.0797669,-34.9223232,0
              -58.0802711,-34.9234141,0
              -58.0896044,-34.931378,0
              -58.1081613,-34.9169451,0
              -58.108208,-34.9169765,0
              -58.1082551,-34.9170089,0
              -58.1083175,-34.9170584,0
              -58.1083745,-34.9171277,0
              -58.108518,-34.9172805,0
              -58.1086132,-34.917485,0
              -58.1086771,-34.9175893,0
              -58.1087776,-34.9177716,0
              -58.1088549,-34.9178834,0
              -58.1090333,-34.9182122,0
              -58.1091817,-34.9183816,0
              -58.109259,-34.9184818,0
              -58.1093303,-34.9185583,0
              -58.1094212,-34.9186452,0
              -58.1094891,-34.9187102,0
              -58.1095427,-34.9187718,0
              -58.1096077,-34.9188582,0
              -58.1096537,-34.9189075,0
              -58.1096661,-34.9189279,0
              -58.1097374,-34.9190317,0
              -58.1097645,-34.919129,0
              -58.1097632,-34.9191897,0
              -58.1097364,-34.9193524,0
              -58.1097095,-34.9195746,0
              -58.1097636,-34.9196815,0
              -58.1098226,-34.9198091,0
              -58.1098403,-34.9200395,0
              -58.1098994,-34.9201627,0
              -58.1099259,-34.9205734,0
              -58.1099353,-34.9207405,0
              -58.1099369,-34.9209357,0
              -58.109961,-34.9210204,0
              -58.110079,-34.9212139,0
              -58.1101917,-34.9213525,0
              -58.1103714,-34.9215075,0
              -58.1105672,-34.9216493,0
              -58.1106919,-34.9217098,0
              -58.1107576,-34.9217813,0
              -58.1107821,-34.921868,0
              -58.1108234,-34.9220711,0
              -58.1109162,-34.9221957,0
              -58.110932,-34.922384,0
              -58.1109293,-34.9225225,0
              -58.1109189,-34.9226091,0
              -58.1108997,-34.9227468,0
              -58.1107862,-34.9231185,0
              -58.1107874,-34.9231611,0
              -58.1108261,-34.923257,0
              -58.1109132,-34.9235693,0
              -58.1113158,-34.9241706,0
              -58.1115412,-34.9244701,0
              -58.1115371,-34.9248886,0
              -58.1115344,-34.9249985,0
              -58.1115304,-34.9252459,0
              -58.1115214,-34.9255504,0
              -58.1115337,-34.925618,0
              -58.1115496,-34.9257376,0
              -58.1115909,-34.925857,0
              -58.1116472,-34.9259647,0
              -58.1117223,-34.9260703,0
              -58.1117357,-34.9261605,0
              -58.1117528,-34.9263119,0
              -58.1117817,-34.9264181,0
              -58.1118326,-34.926574,0
              -58.1118247,-34.9267458,0
              -58.1117817,-34.9269789,0
              -58.1118166,-34.9271438,0
              -58.1119427,-34.9274451,0
              -58.11217,-34.9279625,0
              -58.1122987,-34.9282242,0
              -58.1123684,-34.9283693,0
              -58.1124535,-34.9285582,0
              -58.1125267,-34.9288113,0
              -58.1125539,-34.9289854,0
              -58.112556,-34.9291365,0
              -58.1125279,-34.9293113,0
              -58.1204899,-34.9362284,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>EL PELIGRO</name>
      <description><![CDATA[Descripción: <br>nombre: EL PELIGRO<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-C2185B-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>EL PELIGRO</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.162488,-34.901981,0
              -58.2080577,-34.941959,0
              -58.2038907,-34.945232,0
              -58.2480007,-34.983892,0
              -58.2470647,-34.987017,0
              -58.2623491,-34.9963292,0
              -58.2697437,-35.001406,0
              -58.2776977,-35.009498,0
              -58.2829443,-35.0130786,0
              -58.2886237,-35.017114,0
              -58.2469807,-35.048242,0
              -58.1837899,-34.9915144,0
              -58.1522271,-34.9638063,0
              -58.120514,-34.936301,0
              -58.1223113,-34.935126,0
              -58.1238693,-34.9341861,0
              -58.1248345,-34.9335738,0
              -58.1255719,-34.9331225,0
              -58.1259936,-34.9329184,0
              -58.1263617,-34.9327143,0
              -58.1272427,-34.9322336,0
              -58.1313377,-34.9298248,0
              -58.1351903,-34.9274147,0
              -58.137465,-34.9259881,0
              -58.1384205,-34.9253176,0
              -58.1393756,-34.9244471,0
              -58.1407275,-34.9232024,0
              -58.1419293,-34.9220984,0
              -58.1444775,-34.9198068,0
              -58.1502633,-34.914183,0
              -58.1559841,-34.9085061,0
              -58.1579528,-34.9066126,0
              -58.159664,-34.904939,0
              -58.1612799,-34.903339,0
              -58.162488,-34.901981,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>ARTURO SEGUI</name>
      <description><![CDATA[Descripción: <br>nombre: ARTURO SEGUI<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-A52714-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>ARTURO SEGUI</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.1079143,-34.91666,0
              -58.1078618,-34.9165296,0
              -58.107753,-34.9163355,0
              -58.1076604,-34.9162228,0
              -58.1075736,-34.9161681,0
              -58.1074774,-34.916121,0
              -58.107401,-34.9160429,0
              -58.1073246,-34.9159747,0
              -58.1072871,-34.9159451,0
              -58.1072329,-34.9158833,0
              -58.1071934,-34.9158437,0
              -58.1071719,-34.9158134,0
              -58.1071451,-34.9157821,0
              -58.1071303,-34.9157354,0
              -58.1071253,-34.9157029,0
              -58.1071484,-34.9156342,0
              -58.1071611,-34.9155598,0
              -58.1071611,-34.9155086,0
              -58.1071406,-34.9154432,0
              -58.1071249,-34.9153984,0
              -58.1071048,-34.9153518,0
              -58.1070809,-34.9153127,0
              -58.1070615,-34.9152842,0
              -58.1070478,-34.9152489,0
              -58.1070314,-34.915213,0
              -58.1070167,-34.9151919,0
              -58.107003,-34.9151592,0
              -58.1069869,-34.915119,0
              -58.1069638,-34.9150658,0
              -58.1069474,-34.9150256,0
              -58.1069133,-34.9149857,0
              -58.1068827,-34.914911,0
              -58.1068616,-34.914874,0
              -58.1068421,-34.9148586,0
              -58.1068132,-34.9148346,0
              -58.1067741,-34.9148138,0
              -58.1067362,-34.9147967,0
              -58.1067113,-34.914785,0
              -58.1066959,-34.914781,0
              -58.1066268,-34.9147535,0
              -58.1065175,-34.9147233,0
              -58.106429,-34.9146854,0
              -58.1063485,-34.9146546,0
              -58.1062882,-34.9146216,0
              -58.1062513,-34.914582,0
              -58.1062204,-34.9145424,0
              -58.1062098,-34.914522,0
              -58.1062011,-34.9145034,0
              -58.1061916,-34.9144874,0
              -58.1061581,-34.9144198,0
              -58.106136,-34.9143686,0
              -58.1061213,-34.9142867,0
              -58.1061272,-34.9141503,0
              -58.1060998,-34.914086,0
              -58.1060676,-34.9140535,0
              -58.1060026,-34.9140228,0
              -58.1059295,-34.9139953,0
              -58.1058436,-34.9139634,0
              -58.1057577,-34.9139276,0
              -58.1056994,-34.913854,0
              -58.1056776,-34.9138144,0
              -58.105672,-34.9137528,0
              -58.1056612,-34.9136736,0
              -58.1056545,-34.9136021,0
              -58.1056344,-34.9135097,0
              -58.1055942,-34.9134416,0
              -58.1055405,-34.9134042,0
              -58.1054547,-34.9133624,0
              -58.1053621,-34.9133338,0
              -58.1052422,-34.9132948,0
              -58.1051321,-34.9132783,0
              -58.1050316,-34.913275,0
              -58.1048881,-34.9133058,0
              -58.104766,-34.9133212,0
              -58.1047097,-34.9133278,0
              -58.1045797,-34.9133366,0
              -58.1044381,-34.9133107,0
              -58.1041854,-34.913242,0
              -58.1040365,-34.9132073,0
              -58.1039479,-34.9131672,0
              -58.1038534,-34.9130599,0
              -58.1038339,-34.9130209,0
              -58.1038246,-34.9129505,0
              -58.1038112,-34.9128724,0
              -58.1037971,-34.9127432,0
              -58.1037509,-34.9126723,0
              -58.1036731,-34.912603,0
              -58.1035644,-34.9125018,0
              -58.1034947,-34.9124678,0
              -58.1033609,-34.9123734,0
              -58.1032262,-34.9122876,0
              -58.1031152,-34.9122298,0
              -58.1030344,-34.9121996,0
              -58.1029522,-34.9121474,0
              -58.1029031,-34.9120927,0
              -58.1028768,-34.912027,0
              -58.1028687,-34.9119808,0
              -58.1028741,-34.9119258,0
              -58.1029626,-34.9117388,0
              -58.1029653,-34.9116343,0
              -58.1029398,-34.9114441,0
              -58.102913,-34.9112417,0
              -58.1028298,-34.9109096,0
              -58.1028091,-34.9108134,0
              -58.1027749,-34.9107457,0
              -58.1026851,-34.9106215,0
              -58.1026267,-34.9105726,0
              -58.1025899,-34.9105192,0
              -58.1025597,-34.9104758,0
              -58.1025455,-34.9104235,0
              -58.1025375,-34.9102442,0
              -58.1025375,-34.9100892,0
              -58.1025462,-34.9097938,0
              -58.1025462,-34.9095518,0
              -58.1024979,-34.9094199,0
              -58.1023799,-34.9093187,0
              -58.1022592,-34.9092923,0
              -58.1020929,-34.9092659,0
              -58.1019024,-34.9092659,0
              -58.1017523,-34.9092725,0
              -58.1015162,-34.9093165,0
              -58.1013071,-34.9093935,0
              -58.1008819,-34.9095584,0
              -58.1003924,-34.9097278,0
              -58.1001779,-34.9097784,0
              -58.099974,-34.909741,0
              -58.0997648,-34.9097058,0
              -58.0996628,-34.9096355,0
              -58.0996414,-34.9094023,0
              -58.0994643,-34.9091603,0
              -58.0991693,-34.90898,0
              -58.0989333,-34.9087248,0
              -58.0985256,-34.9085577,0
              -58.098134,-34.9084477,0
              -58.0980312,-34.9084134,0
              -58.097975,-34.9082862,0
              -58.097967,-34.9082268,0
              -58.0979562,-34.9081333,0
              -58.0979187,-34.9080123,0
              -58.097865,-34.9078991,0
              -58.0978811,-34.9077341,0
              -58.0979213,-34.9075031,0
              -58.0979643,-34.9072721,0
              -58.0979723,-34.906973,0
              -58.0979616,-34.9068696,0
              -58.0978569,-34.9067509,0
              -58.0977407,-34.9064357,0
              -58.0977943,-34.9062663,0
              -58.0979177,-34.9061146,0
              -58.0980304,-34.9059122,0
              -58.0981403,-34.905778,0
              -58.0981919,-34.9056702,0
              -58.0981953,-34.9055184,0
              -58.0982101,-34.9053293,0
              -58.0982047,-34.9050654,0
              -58.0981711,-34.904885,0
              -58.0981296,-34.9047265,0
              -58.0981041,-34.9046122,0
              -58.0980625,-34.9045209,0
              -58.0979271,-34.9043614,0
              -58.0976321,-34.9040931,0
              -58.0974966,-34.9040051,0
              -58.0973772,-34.9038951,0
              -58.0972713,-34.9038005,0
              -58.097217,-34.9037488,0
              -58.0971466,-34.9037125,0
              -58.0970245,-34.9036751,0
              -58.096954,-34.9036596,0
              -58.096889,-34.9036287,0
              -58.0968474,-34.9035946,0
              -58.0968058,-34.9035451,0
              -58.0967428,-34.9034703,0
              -58.0966891,-34.9033752,0
              -58.0966167,-34.9032558,0
              -58.0965604,-34.9031502,0
              -58.0964719,-34.9030314,0
              -58.09637,-34.902928,0
              -58.0963431,-34.9028796,0
              -58.0963511,-34.9028137,0
              -58.0964128,-34.9027147,0
              -58.0965657,-34.9024991,0
              -58.0966783,-34.9024221,0
              -58.0968775,-34.9023359,0
              -58.0969955,-34.9022259,0
              -58.0970465,-34.9021159,0
              -58.0970385,-34.9019421,0
              -58.0969661,-34.9017639,0
              -58.0968762,-34.9016166,0
              -58.0968013,-34.9015127,0
              -58.0967638,-34.9014709,0
              -58.096753,-34.9013939,0
              -58.0968495,-34.9012466,0
              -58.0969488,-34.9011168,0
              -58.0969749,-34.9010475,0
              -58.0969743,-34.9009452,0
              -58.0969669,-34.9008743,0
              -58.0969246,-34.9008033,0
              -58.0968201,-34.9007384,0
              -58.0967048,-34.9006768,0
              -58.096575,-34.9006511,0
              -58.0964559,-34.9006078,0
              -58.0963767,-34.9005187,0
              -58.0963519,-34.9004549,0
              -58.0963405,-34.900412,0
              -58.0962869,-34.900203,0
              -58.0962037,-34.9000446,0
              -58.0961712,-34.9000018,0
              -58.096132,-34.8999575,0
              -58.0960807,-34.8999128,0
              -58.0960381,-34.899875,0
              -58.0959838,-34.8997982,0
              -58.0959679,-34.8997485,0
              -58.095972,-34.8996922,0
              -58.095986,-34.8996625,0
              -58.0959912,-34.8996042,0
              -58.0959395,-34.8994597,0
              -58.0958846,-34.8992137,0
              -58.0959221,-34.8990509,0
              -58.0959382,-34.8988837,0
              -58.0958873,-34.8987231,0
              -58.095831,-34.8985977,0
              -58.0957909,-34.8984746,0
              -58.0957185,-34.8984086,0
              -58.0956595,-34.8982766,0
              -58.0955848,-34.8980826,0
              -58.0954772,-34.8978542,0
              -58.0953698,-34.8977267,0
              -58.0952142,-34.8976607,0
              -58.0950748,-34.8975507,0
              -58.095005,-34.8974231,0
              -58.0949138,-34.8973175,0
              -58.0948119,-34.8971503,0
              -58.0946724,-34.8970403,0
              -58.094651,-34.8968555,0
              -58.0945866,-34.8966971,0
              -58.0945132,-34.8966208,0
              -58.094481,-34.896458,0
              -58.0944732,-34.8961902,0
              -58.094481,-34.8960268,0
              -58.094481,-34.8959388,0
              -58.1107153,-34.8921097,0
              -58.1015942,-34.8842613,0
              -58.1202447,-34.8707665,0
              -58.1159612,-34.867219,0
              -58.1197458,-34.8644153,0
              -58.1477743,-34.8872854,0
              -58.1465783,-34.8881934,0
              -58.1625122,-34.9021356,0
              -58.1506317,-34.9138015,0
              -58.1446539,-34.9196284,0
              -58.1384178,-34.9253143,0
              -58.1374623,-34.9259848,0
              -58.1362814,-34.9267168,0
              -58.1351876,-34.9274114,0
              -58.1340912,-34.928128,0
              -58.1318909,-34.9294898,0
              -58.1307776,-34.9301766,0
              -58.1296248,-34.9308448,0
              -58.1250132,-34.9334911,0
              -58.1204872,-34.9362251,0
              -58.1199879,-34.9358005,0
              -58.1198455,-34.9356608,0
              -58.1194563,-34.9353231,0
              -58.1190672,-34.9350031,0
              -58.1189034,-34.9348502,0
              -58.1183933,-34.9344211,0
              -58.117894,-34.9339921,0
              -58.1176108,-34.9337468,0
              -58.1173545,-34.9335059,0
              -58.1164175,-34.9326831,0
              -58.1125252,-34.929308,0
              -58.1125366,-34.9292305,0
              -58.1125533,-34.9291332,0
              -58.1125512,-34.9289821,0
              -58.1125317,-34.9288942,0
              -58.1125162,-34.9287897,0
              -58.1124944,-34.9287019,0
              -58.1124689,-34.9286164,0
              -58.1124508,-34.9285549,0
              -58.1124213,-34.9284927,0
              -58.1123864,-34.9284114,0
              -58.112304,-34.9282498,0
              -58.1122161,-34.9280585,0
              -58.1119532,-34.9274724,0
              -58.1118339,-34.9272113,0
              -58.111801,-34.9270796,0
              -58.1117829,-34.9269952,0
              -58.1117822,-34.9269072,0
              -58.1118235,-34.9267049,0
              -58.1118299,-34.9265707,0
              -58.1117802,-34.9264311,0
              -58.1117501,-34.9263086,0
              -58.1117387,-34.9261816,0
              -58.1117293,-34.9261156,0
              -58.1117071,-34.9260496,0
              -58.1116558,-34.9259847,0
              -58.1116233,-34.9259276,0
              -58.1115697,-34.9257994,0
              -58.1115469,-34.9257343,0
              -58.1115248,-34.9255775,0
              -58.1115187,-34.9255471,0
              -58.1115267,-34.9252651,0
              -58.1115281,-34.9250603,0
              -58.1115361,-34.9248995,0
              -58.1115395,-34.9246037,0
              -58.1115385,-34.9244668,0
              -58.1114516,-34.9243563,0
              -58.1111384,-34.9239311,0
              -58.1109105,-34.923566,0
              -58.1108234,-34.9232537,0
              -58.1107932,-34.9231833,0
              -58.1107835,-34.9231152,0
              -58.1107979,-34.9230624,0
              -58.1108421,-34.9229183,0
              -58.110897,-34.9227435,0
              -58.1109266,-34.9225192,0
              -58.1109293,-34.9223807,0
              -58.1109159,-34.9222366,0
              -58.1108207,-34.9220678,0
              -58.1107811,-34.9218514,0
              -58.1107549,-34.921778,0
              -58.1106892,-34.9217065,0
              -58.1105645,-34.921646,0
              -58.1103687,-34.9215042,0
              -58.110189,-34.9213492,0
              -58.1100763,-34.9212106,0
              -58.1099583,-34.9210171,0
              -58.1099342,-34.9209324,0
              -58.1099302,-34.9208483,0
              -58.1099315,-34.9206806,0
              -58.1099073,-34.9203529,0
              -58.1098967,-34.9201594,0
              -58.1098376,-34.9200362,0
              -58.1098108,-34.9198833,0
              -58.1097626,-34.919769,0
              -58.109725,-34.9196866,0
              -58.1097116,-34.9196172,0
              -58.1097249,-34.9193743,0
              -58.1097631,-34.9191697,0
              -58.1097618,-34.9191257,0
              -58.1097347,-34.9190284,0
              -58.1096896,-34.9189594,0
              -58.1096526,-34.9189063,0
              -58.109605,-34.9188549,0
              -58.1095547,-34.9187864,0
              -58.1094976,-34.9187169,0
              -58.1094631,-34.9186821,0
              -58.1094185,-34.9186419,0
              -58.1093276,-34.918555,0
              -58.1092563,-34.9184785,0
              -58.1091721,-34.9183716,0
              -58.109092,-34.9182768,0
              -58.1090306,-34.9182089,0
              -58.1089585,-34.9180794,0
              -58.1088522,-34.9178801,0
              -58.1087749,-34.9177683,0
              -58.1087084,-34.9176478,0
              -58.1086105,-34.9174817,0
              -58.1085153,-34.9172772,0
              -58.1083718,-34.9171244,0
              -58.1083148,-34.9170551,0
              -58.1082524,-34.9170056,0
              -58.1081586,-34.9169418,0
              -58.1081023,-34.9169077,0
              -58.1080406,-34.9168417,0
              -58.1079781,-34.9167541,0
              -58.1079143,-34.91666,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>ETCHEVERRY</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-1A237E-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <MultiGeometry>
        <Polygon>
          <outerBoundaryIs>
            <LinearRing>
              <tessellate>1</tessellate>
              <coordinates>
                -58.028098,-35.0406417,0
                -58.028095,-35.0406399,0
                -58.0281021,-35.0406454,0
                -58.028098,-35.0406417,0
              </coordinates>
            </LinearRing>
          </outerBoundaryIs>
        </Polygon>
        <Polygon>
          <outerBoundaryIs>
            <LinearRing>
              <tessellate>1</tessellate>
              <coordinates>
                -58.027805,-35.0403884,0
                -58.0278032,-35.0403859,0
                -58.0277993,-35.0403829,0
                -58.027805,-35.0403884,0
              </coordinates>
            </LinearRing>
          </outerBoundaryIs>
        </Polygon>
        <Polygon>
          <outerBoundaryIs>
            <LinearRing>
              <tessellate>1</tessellate>
              <coordinates>
                -58.028029,-35.0405844,0
                -58.0214308,-35.0349149,0
                -58.0325075,-35.026497,0
                -58.0327114,-35.0263871,0
                -58.0393762,-35.0213249,0
                -58.0460984,-35.0161747,0
                -58.0529271,-35.0110944,0
                -58.0665336,-35.0009679,0
                -58.066665,-35.0007943,0
                -58.0933884,-35.0251738,0
                -58.0926781,-35.0356395,0
                -58.1032239,-35.0452992,0
                -58.1238982,-35.0643718,0
                -58.1310006,-35.0691029,0
                -58.145315,-35.0816998,0
                -58.1100759,-35.1085248,0
                -58.1099766,-35.1085402,0
                -58.1098559,-35.1084612,0
                -58.1017909,-35.1011359,0
                -58.1016863,-35.101114,0
                -58.0933523,-35.1074881,0
                -58.0930492,-35.1077821,0
                -58.0928025,-35.1080937,0
                -58.0850401,-35.1136405,0
                -58.084769,-35.11405,0
                -58.079007,-35.1183521,0
                -58.076681,-35.120035,0
                -58.0697505,-35.1249878,0
                -58.0678086,-35.126383,0
                -58.0630397,-35.1298264,0
                -58.0631362,-35.1299229,0
                -58.062632,-35.1303484,0
                -58.0318405,-35.153141,0
                -58.0316312,-35.1532594,0
                -58.0307515,-35.1539655,0
                -58.0295928,-35.1552199,0
                -58.028992,-35.1558997,0
                -58.0278493,-35.157176,0
                -58.0249901,-35.1604346,0
                -58.0187004,-35.1675969,0
                -58.0186253,-35.1676583,0
                -58.0666249,-35.2095809,0
                -58.0700383,-35.212509,0
                -58.077353,-35.218791,0
                -58.0739194,-35.2212572,0
                -58.0625683,-35.2292853,0
                -58.053645,-35.235506,0
                -58.0416829,-35.22407,0
                -58.0341173,-35.2169064,0
                -58.0239893,-35.2070888,0
                -58.018954,-35.202274,0
                -58.0095062,-35.1940792,0
                -58.000549,-35.18613,0
                -57.9938099,-35.1801768,0
                -57.9849727,-35.1724542,0
                -57.9818506,-35.169753,0
                -57.9769464,-35.1655428,0
                -57.9743285,-35.1634027,0
                -57.9705949,-35.1600872,0
                -57.9697216,-35.1594341,0
                -57.9690725,-35.159092,0
                -57.968679,-35.158918,0
                -57.968651,-35.158641,0
                -57.968478,-35.158322,0
                -57.9677904,-35.1577982,0
                -57.9655374,-35.1559123,0
                -57.9139837,-35.1132691,0
                -57.9130181,-35.1125319,0
                -57.912476,-35.112106,0
                -57.9122651,-35.1119482,0
                -57.9165942,-35.1112746,0
                -57.9181765,-35.1109251,0
                -57.919067,-35.1107013,0
                -57.9200755,-35.1103283,0
                -57.9208051,-35.1099553,0
                -57.9218887,-35.1092707,0
                -57.922527,-35.1087397,0
                -57.9239593,-35.1076733,0
                -57.9249678,-35.1068219,0
                -57.9336046,-35.0999667,0
                -57.9349226,-35.098681,0
                -57.9359257,-35.0975354,0
                -57.9385788,-35.0944489,0
                -57.9392976,-35.0936588,0
                -57.9443469,-35.0889507,0
                -57.9480001,-35.0855669,0
                -57.9495129,-35.0840919,0
                -57.949533,-35.0840902,0
                -57.9497891,-35.0843207,0
                -57.9595289,-35.093026,0
                -57.9607949,-35.0941716,0
                -57.9630373,-35.0961818,0
                -57.9641316,-35.0971913,0
                -57.9644857,-35.0974546,0
                -57.9650758,-35.0980427,0
                -57.9661379,-35.0990171,0
                -57.966331,-35.099061,0
                -57.9667387,-35.0987713,0
                -57.968055,-35.0977528,0
                -57.9695249,-35.0966467,0
                -57.9709733,-35.0955582,0
                -57.9737889,-35.0934675,0
                -57.9798008,-35.0889534,0
                -57.983513,-35.0861441,0
                -57.9890786,-35.0820267,0
                -57.9923002,-35.0796476,0
                -57.9940812,-35.0783108,0
                -57.9954486,-35.0773117,0
                -57.9969667,-35.0761791,0
                -57.9986458,-35.0749147,0
                -58.0032778,-35.0714794,0
                -58.006475,-35.0690383,0
                -58.0093504,-35.0669484,0
                -58.0112386,-35.065719,0
                -58.018993,-35.0608088,0
                -58.024572,-35.0572081,0
                -58.031302,-35.0528903,0
                -58.0320315,-35.0535314,0
                -58.0357032,-35.0507655,0
                -58.0380977,-35.0489408,0
                -58.0364562,-35.0475852,0
                -58.0363906,-35.0475294,0
                -58.0363061,-35.0474588,0
                -58.0362043,-35.0473792,0
                -58.028029,-35.0405844,0
              </coordinates>
            </LinearRing>
          </outerBoundaryIs>
        </Polygon>
      </MultiGeometry>
    </Placemark>
    <Placemark>
      <name>CASCO URBANO</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-0288D1-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9530118,-34.9539169,0
              -57.9521755,-34.9539424,0
              -57.912499,-34.918016,0
              -57.9547751,-34.8866077,0
              -57.9741662,-34.9049041,0
              -57.993704,-34.9229764,0
              -57.9937048,-34.9232149,0
              -57.97356,-34.938694,0
              -57.9720299,-34.93968,0
              -57.971148,-34.93995,0
              -57.967415,-34.94267,0
              -57.967232,-34.943032,0
              -57.96722,-34.943414,0
              -57.9530118,-34.9539169,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>TOLOSA</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-EDA29B-3001-120</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.993704,-34.92295,0
              -57.9742258,-34.9049133,0
              -57.9643874,-34.8956922,0
              -57.9590231,-34.8907012,0
              -57.9568669,-34.8886765,0
              -57.9547751,-34.8865813,0
              -57.9679499,-34.8771158,0
              -58.0072391,-34.9128467,0
              -58.0004304,-34.9179073,0
              -57.993704,-34.92295,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>RINGUELET</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-880E4F-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9948864,-34.9016413,0
              -57.9679499,-34.8771422,0
              -57.9696781,-34.8759387,0
              -57.9716522,-34.8748825,0
              -57.9738409,-34.8740375,0
              -57.9749781,-34.873703,0
              -57.9761154,-34.8734037,0
              -57.9763087,-34.8733343,0
              -57.9802352,-34.8766957,0
              -57.9834753,-34.8795298,0
              -57.9842371,-34.8804187,0
              -57.9847199,-34.8802603,0
              -57.9854995,-34.8800778,0
              -57.9866367,-34.8798314,0
              -57.98801,-34.8796553,0
              -57.98904,-34.8796729,0
              -57.9906064,-34.8797697,0
              -57.992087,-34.8800426,0
              -57.9941147,-34.8806587,0
              -57.995075,-34.881091,0
              -57.996239,-34.8817038,0
              -57.9974514,-34.8820598,0
              -57.998138,-34.882293,0
              -57.998535,-34.8825175,0
              -57.9991251,-34.8829839,0
              -57.999522,-34.8833448,0
              -58.0001872,-34.884084,0
              -58.0011501,-34.8849817,0
              -58.002347,-34.88599,0
              -57.9989142,-34.8885502,0
              -58.0049782,-34.8941507,0
              -57.9948864,-34.9016413,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>GONNET
</name>
      <description><![CDATA[Descripción: <br>nombre: GONNET<br><br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-817717-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>GONNET
</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0213994,-34.8921995,0
              -58.0111825,-34.8997583,0
              -57.9989357,-34.8885502,0
              -58.0023685,-34.88599,0
              -58.0087698,-34.8810771,0
              -58.0094564,-34.8808306,0
              -58.0107332,-34.8803818,0
              -58.0117953,-34.8798185,0
              -58.012364,-34.8795192,0
              -58.0288306,-34.8723576,0
              -58.0302674,-34.8717353,0
              -58.030305,-34.8718233,0
              -58.0303103,-34.8719245,0
              -58.0302567,-34.8721182,0
              -58.0301762,-34.8723559,0
              -58.0300689,-34.8725539,0
              -58.0300099,-34.8727211,0
              -58.0299938,-34.8728972,0
              -58.030028,-34.8731997,0
              -58.0300824,-34.8734142,0
              -58.0300468,-34.87362,0
              -58.0299674,-34.8738814,0
              -58.0298869,-34.8740971,0
              -58.0298655,-34.8742335,0
              -58.0299888,-34.8744448,0
              -58.0301927,-34.8746956,0
              -58.0303912,-34.8749377,0
              -58.0306396,-34.875246,0
              -58.0308918,-34.8754286,0
              -58.0310312,-34.8755893,0
              -58.0311439,-34.8757763,0
              -58.0312838,-34.8759191,0
              -58.0314845,-34.8759787,0
              -58.0318259,-34.8759798,0
              -58.0320156,-34.8759897,0
              -58.0322309,-34.8760833,0
              -58.0323284,-34.8762148,0
              -58.0323941,-34.8763831,0
              -58.0325202,-34.8767198,0
              -58.032606,-34.876931,0
              -58.0327401,-34.8771115,0
              -58.0332175,-34.8774635,0
              -58.0336291,-34.8777506,0
              -58.0337755,-34.8778467,0
              -58.033933,-34.877863,0
              -58.0340931,-34.8778452,0
              -58.0342058,-34.87781,0
              -58.034433,-34.877756,0
              -58.0345644,-34.877756,0
              -58.0346958,-34.877855,0
              -58.0348004,-34.8779805,0
              -58.0350492,-34.8782925,0
              -58.0352906,-34.8784905,0
              -58.0355695,-34.8785962,0
              -58.0358462,-34.8786477,0
              -58.0359551,-34.8786815,0
              -58.0361891,-34.8787546,0
              -58.0363826,-34.8788149,0
              -58.0366076,-34.8789174,0
              -58.0366761,-34.8789497,0
              -58.0369298,-34.8790613,0
              -58.0371728,-34.8792304,0
              -58.0374681,-34.8794397,0
              -58.0376357,-34.8796345,0
              -58.0376594,-34.8797391,0
              -58.0376532,-34.8801416,0
              -58.0376512,-34.8803408,0
              -58.0377961,-34.8805608,0
              -58.0380536,-34.880706,0
              -58.0382924,-34.8807952,0
              -58.0383694,-34.8808083,0
              -58.0387502,-34.8808523,0
              -58.0388009,-34.8808571,0
              -58.0390683,-34.8808005,0
              -58.039176,-34.8807725,0
              -58.0393142,-34.8807412,0
              -58.0395787,-34.8808219,0
              -58.0398512,-34.8809893,0
              -58.0400228,-34.8812264,0
              -58.0401903,-34.88146,0
              -58.0403119,-34.8816021,0
              -58.0406183,-34.8819618,0
              -58.0410915,-34.8829254,0
              -58.0412769,-34.8832005,0
              -58.0414462,-34.8834492,0
              -58.041731,-34.8838108,0
              -58.0421221,-34.8842677,0
              -58.042599,-34.8846034,0
              -58.0430215,-34.8848047,0
              -58.043313,-34.884941,0
              -58.0439407,-34.8851038,0
              -58.0443056,-34.8852624,0
              -58.0445202,-34.885478,0
              -58.0446053,-34.8856639,0
              -58.0445722,-34.8859062,0
              -58.0445088,-34.886088,0
              -58.0445116,-34.8862051,0
              -58.0445467,-34.8862957,0
              -58.0445783,-34.8863505,0
              -58.0446208,-34.886379,0
              -58.044829,-34.8864372,0
              -58.0449923,-34.886467,0
              -58.0452499,-34.8865123,0
              -58.0453894,-34.8865313,0
              -58.0455502,-34.8865957,0
              -58.0457165,-34.8868025,0
              -58.0458038,-34.8869812,0
              -58.0459126,-34.8871071,0
              -58.0461033,-34.8872177,0
              -58.0463648,-34.8873625,0
              -58.0466492,-34.8874945,0
              -58.0469764,-34.8875693,0
              -58.0471481,-34.8877057,0
              -58.0474055,-34.8879477,0
              -58.0474538,-34.8881589,0
              -58.0474794,-34.8882777,0
              -58.047576,-34.8884449,0
              -58.0476243,-34.8886561,0
              -58.0475814,-34.8888629,0
              -58.0476806,-34.8890917,0
              -58.0478362,-34.8893051,0
              -58.0478925,-34.8893756,0
              -58.0351552,-34.8923976,0
              -58.0363836,-34.8960254,0
              -58.0290558,-34.8977941,0
              -58.0286857,-34.8965424,0
              -58.0256401,-34.8972705,0
              -58.0213994,-34.8921995,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>GORINA</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-E65100-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0351337,-34.892402,0
              -58.047871,-34.88938,0
              -58.0481558,-34.8897555,0
              -58.048298,-34.8899161,0
              -58.0484643,-34.8899821,0
              -58.0487995,-34.8901559,0
              -58.0489956,-34.8902921,0
              -58.0491297,-34.8904571,0
              -58.0492397,-34.8906419,0
              -58.0493282,-34.8907717,0
              -58.0494462,-34.8908993,0
              -58.0497198,-34.8910907,0
              -58.0498485,-34.8912073,0
              -58.0499102,-34.8913481,0
              -58.0500577,-34.8916429,0
              -58.0501275,-34.8918409,0
              -58.050225,-34.8920606,0
              -58.0502625,-34.892175,0
              -58.0502807,-34.8924474,0
              -58.0502217,-34.8928038,0
              -58.0502056,-34.8929974,0
              -58.0503182,-34.893191,0
              -58.050565,-34.8932526,0
              -58.0508654,-34.893279,0
              -58.0510639,-34.893301,0
              -58.0512141,-34.893389,0
              -58.0514608,-34.8937806,0
              -58.0515842,-34.89395,0
              -58.0515923,-34.8941282,0
              -58.0516379,-34.894269,0
              -58.0517908,-34.8944427,0
              -58.052,-34.8945417,0
              -58.0521931,-34.8945615,0
              -58.0524197,-34.8945945,0
              -58.0525806,-34.8947452,0
              -58.0526746,-34.8949025,0
              -58.0526732,-34.8949828,0
              -58.0526544,-34.8950939,0
              -58.0524734,-34.8954239,0
              -58.0523782,-34.8956351,0
              -58.0523881,-34.8957614,0
              -58.0524734,-34.8959717,0
              -58.0525478,-34.8961396,0
              -58.0526444,-34.8962364,0
              -58.052808,-34.8963926,0
              -58.0529911,-34.8965477,0
              -58.0530856,-34.8966588,0
              -58.0532284,-34.8968199,0
              -58.0532747,-34.8969052,0
              -58.0533058,-34.8969487,0
              -58.0535805,-34.8971097,0
              -58.0539132,-34.8973082,0
              -58.0541029,-34.8973555,0
              -58.0544221,-34.8975359,0
              -58.0546415,-34.8976323,0
              -58.0548722,-34.8976631,0
              -58.0551129,-34.8976488,0
              -58.055348,-34.8976521,0
              -58.0555897,-34.8976606,0
              -58.0558566,-34.8977456,0
              -58.0560014,-34.8977962,0
              -58.0561658,-34.8978706,0
              -58.0563094,-34.8979526,0
              -58.0563984,-34.898058,0
              -58.0564688,-34.8981999,0
              -58.0565003,-34.8983374,0
              -58.0565177,-34.8984702,0
              -58.0565184,-34.8985783,0
              -58.0565184,-34.8986894,0
              -58.0565177,-34.8987693,0
              -58.0565418,-34.8988347,0
              -58.0565968,-34.8989024,0
              -58.0566663,-34.8989483,0
              -58.0567652,-34.8989811,0
              -58.0568366,-34.8989883,0
              -58.0568859,-34.8989901,0
              -58.0570351,-34.8989553,0
              -58.0571649,-34.8989101,0
              -58.0573067,-34.8988959,0
              -58.057409,-34.8989099,0
              -58.0574857,-34.8989421,0
              -58.0576252,-34.8990081,0
              -58.0578328,-34.8990465,0
              -58.0579709,-34.8990872,0
              -58.0581305,-34.8992445,0
              -58.0582539,-34.899349,0
              -58.0587635,-34.8995877,0
              -58.0589674,-34.8996823,0
              -58.0590854,-34.8996757,0
              -58.0591605,-34.8996361,0
              -58.0593724,-34.8995437,0
              -58.0595092,-34.8994623,0
              -58.0596567,-34.8993787,0
              -58.059815,-34.8993413,0
              -58.0601824,-34.8993193,0
              -58.0604667,-34.8993083,0
              -58.0606089,-34.8992907,0
              -58.060862,-34.8993234,0
              -58.0610193,-34.8994029,0
              -58.0613143,-34.8994843,0
              -58.0615048,-34.8995877,0
              -58.0618159,-34.8997681,0
              -58.062017,-34.8999287,0
              -58.0621357,-34.9000194,0
              -58.0624891,-34.9003307,0
              -58.062581,-34.9004162,0
              -58.0626742,-34.900505,0
              -58.063157,-34.9012133,0
              -58.0632214,-34.9013475,0
              -58.0632884,-34.9015565,0
              -58.0633555,-34.9018557,0
              -58.0632992,-34.902366,0
              -58.0632133,-34.9027224,0
              -58.0630846,-34.9028764,0
              -58.0630604,-34.9030369,0
              -58.0631633,-34.9032942,0
              -58.063257,-34.9035094,0
              -58.0632867,-34.9036748,0
              -58.0632706,-34.9037891,0
              -58.0631446,-34.9040399,0
              -58.0631124,-34.9044887,0
              -58.0630909,-34.905087,0
              -58.0630909,-34.9053421,0
              -58.0630158,-34.9055841,0
              -58.0628388,-34.9057601,0
              -58.0625223,-34.9058173,0
              -58.0621361,-34.9058877,0
              -58.0619858,-34.9060152,0
              -58.0619,-34.9061912,0
              -58.0618356,-34.9063936,0
              -58.0618196,-34.9065915,0
              -58.0618303,-34.9068115,0
              -58.0618249,-34.9069567,0
              -58.0617176,-34.9070711,0
              -58.0616425,-34.9072162,0
              -58.0616586,-34.907379,0
              -58.0616425,-34.9075066,0
              -58.0615513,-34.9076034,0
              -58.0614279,-34.9076738,0
              -58.061326,-34.9077573,0
              -58.0611436,-34.9078805,0
              -58.0608931,-34.9081673,0
              -58.0606705,-34.9084114,0
              -58.0604774,-34.908682,0
              -58.0604593,-34.9088019,0
              -58.0604888,-34.9089624,0
              -58.0605948,-34.9092407,0
              -58.0606999,-34.9093748,0
              -58.0609354,-34.90958,0
              -58.0610836,-34.9098059,0
              -58.0611151,-34.9099275,0
              -58.061103,-34.9100086,0
              -58.0610775,-34.9100677,0
              -58.0609599,-34.9102075,0
              -58.0608677,-34.9102823,0
              -58.0608221,-34.9103406,0
              -58.0607785,-34.9103978,0
              -58.0607095,-34.9105199,0
              -58.0606679,-34.9106358,0
              -58.0606417,-34.9107161,0
              -58.0605954,-34.9109167,0
              -58.0606132,-34.9111274,0
              -58.060635,-34.9112897,0
              -58.0606324,-34.911425,0
              -58.0606069,-34.9115394,0
              -58.0605566,-34.9116056,0
              -58.0605103,-34.9116541,0
              -58.0604526,-34.9117095,0
              -58.060413,-34.9118097,0
              -58.060472,-34.9120385,0
              -58.0605578,-34.9122804,0
              -58.0606384,-34.9126017,0
              -58.0605753,-34.912759,0
              -58.0604894,-34.912882,0
              -58.060358,-34.9129628,0
              -58.0603218,-34.9130282,0
              -58.0602447,-34.9130926,0
              -58.0601623,-34.9131219,0
              -58.0599766,-34.9131279,0
              -58.059756,-34.9131164,0
              -58.0596151,-34.9131725,0
              -58.0594823,-34.9132834,0
              -58.0593414,-34.9134153,0
              -58.0592266,-34.913539,0
              -58.0590769,-34.9136561,0
              -58.0588838,-34.9137529,0
              -58.058797,-34.9138356,0
              -58.0587175,-34.9140377,0
              -58.0586277,-34.9143534,0
              -58.0585635,-34.9145619,0
              -58.0585479,-34.9146947,0
              -58.0585435,-34.9147979,0
              -58.0585429,-34.9148232,0
              -58.0586147,-34.9151201,0
              -58.0586303,-34.9151676,0
              -58.0586402,-34.9151954,0
              -58.0586382,-34.9152532,0
              -58.0586108,-34.9153174,0
              -58.0585673,-34.9153639,0
              -58.0583061,-34.9154954,0
              -58.0582072,-34.9155509,0
              -58.0580154,-34.9156532,0
              -58.0578883,-34.9157633,0
              -58.0576647,-34.9159732,0
              -58.0573697,-34.9163119,0
              -58.0570945,-34.9166927,0
              -58.0569635,-34.9168992,0
              -58.0569958,-34.9171492,0
              -58.0571046,-34.9173729,0
              -58.0572875,-34.9175578,0
              -58.0575053,-34.9177185,0
              -58.0576565,-34.9177709,0
              -58.0577143,-34.9178365,0
              -58.057752,-34.9180154,0
              -58.0577332,-34.9182078,0
              -58.0576948,-34.9183999,0
              -58.0576377,-34.9185027,0
              -58.0575894,-34.9185847,0
              -58.0574955,-34.9187398,0
              -58.0574306,-34.9188387,0
              -58.0573491,-34.9190898,0
              -58.0573698,-34.9192739,0
              -58.0574792,-34.9195566,0
              -58.057586,-34.9197569,0
              -58.0576375,-34.9198893,0
              -58.0577414,-34.9200449,0
              -58.0577474,-34.920091,0
              -58.0577688,-34.9202296,0
              -58.0579056,-34.9204231,0
              -58.0581216,-34.9206958,0
              -58.0584179,-34.9208839,0
              -58.0584964,-34.9209741,0
              -58.0586385,-34.9212242,0
              -58.0586888,-34.9212967,0
              -58.0587954,-34.921448,0
              -58.0588773,-34.9215513,0
              -58.058892,-34.9215672,0
              -58.0589376,-34.9216107,0
              -58.0590469,-34.9216283,0
              -58.0591535,-34.9216063,0
              -58.0593164,-34.9215172,0
              -58.059416,-34.9214513,0
              -58.0594975,-34.9214128,0
              -58.0595753,-34.9214068,0
              -58.059633,-34.9214282,0
              -58.0597349,-34.9214985,0
              -58.0600085,-34.9217823,0
              -58.0601614,-34.9220253,0
              -58.0602035,-34.9221042,0
              -58.0602844,-34.9221842,0
              -58.0603189,-34.9222397,0
              -58.0603914,-34.9226411,0
              -58.0604296,-34.9227301,0
              -58.0604993,-34.9228324,0
              -58.0605711,-34.9229512,0
              -58.0606348,-34.9230633,0
              -58.0607099,-34.9231788,0
              -58.0608044,-34.9233393,0
              -58.0608292,-34.9234185,0
              -58.0608292,-34.9234998,0
              -58.060791,-34.9235856,0
              -58.0607327,-34.9236868,0
              -58.0606804,-34.9237368,0
              -58.0606093,-34.9237758,0
              -58.0605329,-34.9238017,0
              -58.0604484,-34.9238077,0
              -58.0602251,-34.92383,0
              -58.0601064,-34.9238776,0
              -58.0600091,-34.9239743,0
              -58.0599307,-34.9241992,0
              -58.0598959,-34.9243707,0
              -58.0598824,-34.9247896,0
              -58.059916,-34.9249312,0
              -58.0599522,-34.9250014,0
              -58.060032,-34.925064,0
              -58.0601218,-34.9250937,0
              -58.0602285,-34.9251283,0
              -58.0603411,-34.925202,0
              -58.0604296,-34.9252855,0
              -58.0605194,-34.9256759,0
              -58.0606321,-34.9258425,0
              -58.0607903,-34.926025,0
              -58.0608493,-34.9261938,0
              -58.0608554,-34.9262845,0
              -58.0607864,-34.9264797,0
              -58.0607357,-34.9267095,0
              -58.0606931,-34.9268821,0
              -58.0551713,-34.9282069,0
              -58.0496245,-34.9234744,0
              -58.029863,-34.9023334,0
              -58.0256186,-34.8972749,0
              -58.0286642,-34.8965468,0
              -58.0290343,-34.8977985,0
              -58.0363621,-34.8960298,0
              -58.0351337,-34.892402,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>VILLA CASTELLS</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-FF5252-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9906064,-34.8797697,0
              -57.9998483,-34.8730397,0
              -57.9999774,-34.8729238,0
              -58.0000015,-34.8728754,0
              -57.9999747,-34.8728182,0
              -57.9998889,-34.8727544,0
              -57.9992532,-34.8722196,0
              -57.999221,-34.8721558,0
              -57.9992183,-34.8721228,0
              -57.9992532,-34.8720964,0
              -58.0030029,-34.870435,0
              -58.0222478,-34.8619808,0
              -58.0235674,-34.8639967,0
              -58.0251875,-34.8665232,0
              -58.026432,-34.8684774,0
              -58.0268934,-34.8692256,0
              -58.0272631,-34.8697136,0
              -58.0274669,-34.8699689,0
              -58.0275693,-34.8700178,0
              -58.0278911,-34.8701587,0
              -58.0282667,-34.8702467,0
              -58.0285823,-34.8703212,0
              -58.0292681,-34.8705278,0
              -58.0295201,-34.8706298,0
              -58.0297198,-34.8707913,0
              -58.0300798,-34.871391,0
              -58.0302459,-34.8717353,0
              -58.0137398,-34.8789079,0
              -58.0123425,-34.8795192,0
              -58.0108859,-34.8803161,0
              -58.0087483,-34.8810771,0
              -58.002347,-34.88599,0
              -58.0001872,-34.884084,0
              -57.999522,-34.8833448,0
              -57.998535,-34.8825175,0
              -57.998138,-34.882293,0
              -57.996239,-34.8817038,0
              -57.995075,-34.881091,0
              -57.9941147,-34.8806587,0
              -57.992087,-34.8800426,0
              -57.9906064,-34.8797697,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>CITY BELL</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-9C27B0-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0222478,-34.8619808,0
              -58.0574145,-34.846635,0
              -58.0574844,-34.8467774,0
              -58.0587397,-34.8487496,0
              -58.059952,-34.850537,0
              -58.0602632,-34.8511973,0
              -58.0604992,-34.8518665,0
              -58.0604134,-34.8541116,0
              -58.0603919,-34.8551505,0
              -58.0606829,-34.8558829,0
              -58.0612516,-34.8566753,0
              -58.0619167,-34.8571331,0
              -58.0625712,-34.8575116,0
              -58.063054,-34.8578374,0
              -58.0633759,-34.8581807,0
              -58.0633946,-34.8583584,0
              -58.0632873,-34.8586049,0
              -58.06318,-34.8588646,0
              -58.0632069,-34.8591771,0
              -58.0633302,-34.8594237,0
              -58.0639418,-34.8599078,0
              -58.0642207,-34.8602072,0
              -58.0644246,-34.8603216,0
              -58.0647357,-34.8603656,0
              -58.0649074,-34.8605857,0
              -58.0652078,-34.8607266,0
              -58.0656584,-34.8608762,0
              -58.0649238,-34.8612643,0
              -58.0639582,-34.8615988,0
              -58.0624991,-34.8617925,0
              -58.0603748,-34.8618629,0
              -58.0597954,-34.8618629,0
              -58.063995,-34.8739077,0
              -58.0840682,-34.8691886,0
              -58.0885656,-34.8731139,0
              -58.0854052,-34.8741852,0
              -58.0825942,-34.8748718,0
              -58.0885247,-34.8918462,0
              -58.0892114,-34.8937118,0
              -58.0895118,-34.8952078,0
              -58.0900393,-34.897185,0
              -58.0914628,-34.8968156,0
              -58.0933082,-34.8963757,0
              -58.0937676,-34.896261,0
              -58.0940914,-34.8961601,0
              -58.0942308,-34.8960677,0
              -58.094381,-34.8959929,0
              -58.0944951,-34.8959421,0
              -58.0944956,-34.8959794,0
              -58.0944936,-34.8960454,0
              -58.0944876,-34.8961973,0
              -58.0944978,-34.8964657,0
              -58.0945088,-34.8965435,0
              -58.094536,-34.8966258,0
              -58.0946201,-34.8967488,0
              -58.0946516,-34.8968555,0
              -58.0946892,-34.897048,0
              -58.0947092,-34.8970967,0
              -58.0947641,-34.8971894,0
              -58.0948292,-34.8972463,0
              -58.0949668,-34.897334,0
              -58.095015,-34.8974113,0
              -58.0950498,-34.8974996,0
              -58.0950799,-34.8975475,0
              -58.0951678,-34.897614,0
              -58.0953306,-34.897719,0
              -58.0954183,-34.8977778,0
              -58.0954778,-34.8978542,0
              -58.0955855,-34.8980826,0
              -58.0956675,-34.8982865,0
              -58.0957192,-34.8984086,0
              -58.0957916,-34.8984746,0
              -58.0958337,-34.8986016,0
              -58.0958879,-34.8987231,0
              -58.0959389,-34.8988837,0
              -58.0959228,-34.8990509,0
              -58.0958852,-34.8992137,0
              -58.0959402,-34.8994597,0
              -58.0959918,-34.8996042,0
              -58.0959866,-34.8996625,0
              -58.0959726,-34.8996922,0
              -58.09597,-34.8997202,0
              -58.0959685,-34.8997485,0
              -58.0959845,-34.8997982,0
              -58.0960388,-34.899875,0
              -58.0960854,-34.8999166,0
              -58.0961326,-34.8999575,0
              -58.0961719,-34.9000018,0
              -58.096247,-34.9001206,0
              -58.0963114,-34.9002856,0
              -58.0963534,-34.900445,0
              -58.0963774,-34.9005187,0
              -58.0964565,-34.9006078,0
              -58.0965646,-34.9006485,0
              -58.0967055,-34.9006768,0
              -58.0967216,-34.9006845,0
              -58.0968369,-34.9007461,0
              -58.0969253,-34.9008033,0
              -58.0969676,-34.9008743,0
              -58.0969796,-34.9009521,0
              -58.0969756,-34.9010475,0
              -58.0969488,-34.9011168,0
              -58.0968495,-34.9012466,0
              -58.096753,-34.9013939,0
              -58.0967638,-34.9014709,0
              -58.0968013,-34.9015127,0
              -58.0968762,-34.9016166,0
              -58.0969661,-34.9017639,0
              -58.096983,-34.9018006,0
              -58.0970051,-34.9018573,0
              -58.0970385,-34.9019421,0
              -58.0970465,-34.9021159,0
              -58.0969955,-34.9022259,0
              -58.0968775,-34.9023359,0
              -58.0966783,-34.9024221,0
              -58.0965657,-34.9024991,0
              -58.0964252,-34.9026998,0
              -58.0963511,-34.9028137,0
              -58.0963431,-34.9028796,0
              -58.0964016,-34.9029528,0
              -58.0965063,-34.9030694,0
              -58.0965604,-34.9031502,0
              -58.0966167,-34.9032558,0
              -58.0966799,-34.9033603,0
              -58.0967428,-34.9034703,0
              -58.0967596,-34.9034906,0
              -58.0967918,-34.9035302,0
              -58.0968058,-34.9035451,0
              -58.0968474,-34.9035946,0
              -58.096889,-34.9036287,0
              -58.0969233,-34.9036474,0
              -58.0969904,-34.9036693,0
              -58.0970789,-34.9036935,0
              -58.0971466,-34.9037125,0
              -58.097217,-34.9037488,0
              -58.0972533,-34.9037815,0
              -58.0974966,-34.9040051,0
              -58.0975554,-34.9040441,0
              -58.0976321,-34.9040931,0
              -58.0978547,-34.9042952,0
              -58.0979271,-34.9043614,0
              -58.0979976,-34.9044439,0
              -58.0980116,-34.90446,0
              -58.0980625,-34.9045209,0
              -58.0981041,-34.9046122,0
              -58.0981243,-34.9047004,0
              -58.0981726,-34.9048897,0
              -58.0982047,-34.9050654,0
              -58.0982088,-34.9052283,0
              -58.0982108,-34.9053653,0
              -58.0981953,-34.9055184,0
              -58.0981919,-34.9056702,0
              -58.0981403,-34.905778,0
              -58.0980304,-34.9059122,0
              -58.0979788,-34.9060131,0
              -58.0979177,-34.9061146,0
              -58.0977943,-34.9062663,0
              -58.0977407,-34.9064357,0
              -58.0977883,-34.9065656,0
              -58.0978373,-34.9066956,0
              -58.0978569,-34.9067509,0
              -58.0979178,-34.9068195,0
              -58.0979616,-34.9068696,0
              -58.0979723,-34.906973,0
              -58.0979643,-34.9072721,0
              -58.0979131,-34.9075539,0
              -58.0978811,-34.9077341,0
              -58.097865,-34.9078991,0
              -58.0979187,-34.9080123,0
              -58.0979562,-34.9081333,0
              -58.097975,-34.9082862,0
              -58.0979937,-34.9083298,0
              -58.0980312,-34.9084134,0
              -58.0981508,-34.9084554,0
              -58.0984389,-34.9085366,0
              -58.0987071,-34.9086377,0
              -58.0989003,-34.9087169,0
              -58.0989861,-34.9088137,0
              -58.099206,-34.9089589,0
              -58.0993294,-34.9090865,0
              -58.0994811,-34.909168,0
              -58.0996137,-34.9093548,0
              -58.0996674,-34.9094428,0
              -58.0996674,-34.9096144,0
              -58.0997816,-34.9097135,0
              -58.1000536,-34.9097551,0
              -58.1001947,-34.9097861,0
              -58.1004881,-34.9096979,0
              -58.1007832,-34.9096012,0
              -58.1011158,-34.9094912,0
              -58.1013239,-34.9094012,0
              -58.1017691,-34.9092802,0
              -58.1019633,-34.90928,0
              -58.1021378,-34.9092727,0
              -58.1023967,-34.9093264,0
              -58.1025147,-34.9094276,0
              -58.102563,-34.9095595,0
              -58.102567,-34.9098292,0
              -58.1025543,-34.9100969,0
              -58.1025623,-34.9104312,0
              -58.1026067,-34.9105269,0
              -58.1027019,-34.9106292,0
              -58.1027977,-34.9107794,0
              -58.1028379,-34.910852,0
              -58.1028969,-34.9111885,0
              -58.1029318,-34.9112919,0
              -58.1029794,-34.9117465,0
              -58.1028909,-34.9119335,0
              -58.1028807,-34.9120673,0
              -58.1030512,-34.9122073,0
              -58.1032026,-34.9122785,0
              -58.103444,-34.9124236,0
              -58.1036899,-34.9126107,0
              -58.103841,-34.9127799,0
              -58.1038507,-34.9130286,0
              -58.1039647,-34.9131749,0
              -58.1042486,-34.913277,0
              -58.1045115,-34.9133254,0
              -58.1047828,-34.9133289,0
              -58.1050484,-34.9132827,0
              -58.105259,-34.9133025,0
              -58.1055573,-34.9134119,0
              -58.1056512,-34.9135174,0
              -58.105678,-34.9136813,0
              -58.1057162,-34.9138617,0
              -58.1057745,-34.9139353,0
              -58.1060194,-34.9140305,0
              -58.1061369,-34.9141304,0
              -58.1061369,-34.9142316,0
              -58.1061528,-34.9143763,0
              -58.1062372,-34.9145501,0
              -58.1063653,-34.9146623,0
              -58.1065343,-34.914731,0
              -58.1068784,-34.9148817,0
              -58.1070482,-34.9152207,0
              -58.1071779,-34.9155163,0
              -58.1071471,-34.9157431,0
              -58.1073414,-34.9159824,0
              -58.1075904,-34.9161758,0
              -58.1078083,-34.9164254,0
              -58.1079311,-34.9166677,0
              -58.1081191,-34.9169154,0
              -58.1081781,-34.9169528,0
              -58.0896212,-34.9313857,0
              -58.0802879,-34.9234218,0
              -58.0797837,-34.9223309,0
              -58.0606931,-34.9268821,0
              -58.0607333,-34.926719,0
              -58.0607864,-34.9264797,0
              -58.0608271,-34.9263656,0
              -58.0608554,-34.9262845,0
              -58.0608493,-34.9261938,0
              -58.0607903,-34.926025,0
              -58.0606321,-34.9258425,0
              -58.0605194,-34.9256759,0
              -58.0604296,-34.9252855,0
              -58.0603411,-34.925202,0
              -58.0602285,-34.9251283,0
              -58.060032,-34.925064,0
              -58.0599522,-34.9250014,0
              -58.059916,-34.9249312,0
              -58.0598824,-34.9247896,0
              -58.0598959,-34.9243707,0
              -58.0599307,-34.9241992,0
              -58.0600091,-34.9239743,0
              -58.0601064,-34.9238776,0
              -58.0602251,-34.92383,0
              -58.0605329,-34.9238017,0
              -58.0606093,-34.9237758,0
              -58.0606804,-34.9237368,0
              -58.0607327,-34.9236868,0
              -58.060791,-34.9235856,0
              -58.0608292,-34.9234998,0
              -58.0608292,-34.9234185,0
              -58.0608044,-34.9233393,0
              -58.060723,-34.9232013,0
              -58.0606348,-34.9230633,0
              -58.0606087,-34.9230193,0
              -58.0605259,-34.9228725,0
              -58.0604296,-34.9227301,0
              -58.0603914,-34.9226411,0
              -58.0603753,-34.9225536,0
              -58.0603189,-34.9222397,0
              -58.0602844,-34.9221842,0
              -58.0602035,-34.9221042,0
              -58.0601797,-34.9220564,0
              -58.0601544,-34.9220116,0
              -58.0601237,-34.9219636,0
              -58.0600085,-34.9217823,0
              -58.0599132,-34.9216827,0
              -58.0597349,-34.9214985,0
              -58.059633,-34.9214282,0
              -58.0595753,-34.9214068,0
              -58.0594975,-34.9214128,0
              -58.059416,-34.9214513,0
              -58.0592756,-34.9215458,0
              -58.0591535,-34.9216063,0
              -58.0590469,-34.9216283,0
              -58.0589376,-34.9216107,0
              -58.0588773,-34.9215513,0
              -58.0587954,-34.921448,0
              -58.0586385,-34.9212242,0
              -58.0584964,-34.9209741,0
              -58.0584179,-34.9208839,0
              -58.0581987,-34.9207409,0
              -58.0581216,-34.9206958,0
              -58.0580793,-34.9206441,0
              -58.0579492,-34.9204682,0
              -58.0577856,-34.9202329,0
              -58.0577554,-34.9201631,0
              -58.0577524,-34.9200996,0
              -58.0577414,-34.9200449,0
              -58.0576375,-34.9198893,0
              -58.057586,-34.9197569,0
              -58.0574728,-34.9195387,0
              -58.0573698,-34.9192739,0
              -58.0573491,-34.9190898,0
              -58.0574306,-34.9188387,0
              -58.0575707,-34.9186237,0
              -58.0576948,-34.9183999,0
              -58.0577332,-34.9182078,0
              -58.057752,-34.9180154,0
              -58.0577143,-34.9178365,0
              -58.0576565,-34.9177709,0
              -58.0575053,-34.9177185,0
              -58.0572875,-34.9175578,0
              -58.0571046,-34.9173729,0
              -58.0569958,-34.9171492,0
              -58.0569683,-34.9170088,0
              -58.0569635,-34.9168992,0
              -58.0570008,-34.9168113,0
              -58.0570891,-34.9166751,0
              -58.0573034,-34.916379,0
              -58.0574377,-34.9162147,0
              -58.0577759,-34.91588,0
              -58.0578883,-34.9157633,0
              -58.0580154,-34.9156532,0
              -58.0583235,-34.9154867,0
              -58.0585673,-34.9153639,0
              -58.0586108,-34.9153174,0
              -58.0586382,-34.9152532,0
              -58.0586402,-34.9151954,0
              -58.0586127,-34.9151102,0
              -58.0585429,-34.9148232,0
              -58.0585479,-34.9146947,0
              -58.0585635,-34.9145619,0
              -58.0586378,-34.9143226,0
              -58.0587044,-34.9140791,0
              -58.058797,-34.9138356,0
              -58.0588838,-34.9137529,0
              -58.0589637,-34.91371,0
              -58.0590769,-34.9136561,0
              -58.0592266,-34.913539,0
              -58.0593046,-34.9134531,0
              -58.0594657,-34.9133001,0
              -58.0596151,-34.9131725,0
              -58.059756,-34.9131164,0
              -58.0599337,-34.9131252,0
              -58.0601623,-34.9131219,0
              -58.0602447,-34.9130926,0
              -58.0603218,-34.9130282,0
              -58.060358,-34.9129628,0
              -58.0604894,-34.912882,0
              -58.0605753,-34.912759,0
              -58.0606384,-34.9126017,0
              -58.0606212,-34.9124438,0
              -58.0605746,-34.9122837,0
              -58.0604821,-34.9120516,0
              -58.0604204,-34.9118114,0
              -58.0604526,-34.9117095,0
              -58.0605103,-34.9116541,0
              -58.0605566,-34.9116056,0
              -58.0606069,-34.9115394,0
              -58.0606223,-34.9114877,0
              -58.0606324,-34.911425,0
              -58.060635,-34.9112897,0
              -58.0606122,-34.9111237,0
              -58.0605954,-34.9109167,0
              -58.0606417,-34.9107161,0
              -58.0607095,-34.9105199,0
              -58.0607785,-34.9103978,0
              -58.0608677,-34.9102823,0
              -58.0609599,-34.9102075,0
              -58.0610775,-34.9100677,0
              -58.061103,-34.9100086,0
              -58.0611151,-34.9099275,0
              -58.0610836,-34.9098059,0
              -58.0609354,-34.90958,0
              -58.0606999,-34.9093748,0
              -58.0605948,-34.9092407,0
              -58.0604888,-34.9089624,0
              -58.0604593,-34.9088019,0
              -58.0604774,-34.908682,0
              -58.0605636,-34.9085341,0
              -58.0606685,-34.908396,0
              -58.0609117,-34.9081366,0
              -58.0610049,-34.9080091,0
              -58.0611651,-34.907864,0
              -58.0613428,-34.907765,0
              -58.0614447,-34.9076815,0
              -58.0615681,-34.9076111,0
              -58.0616593,-34.9075143,0
              -58.0616754,-34.9073867,0
              -58.0616702,-34.9073331,0
              -58.0616593,-34.9072195,0
              -58.0617344,-34.9070788,0
              -58.0618417,-34.9069644,0
              -58.0618471,-34.9068192,0
              -58.0618364,-34.9065992,0
              -58.0618524,-34.9063969,0
              -58.0619168,-34.9061945,0
              -58.0620026,-34.9060229,0
              -58.0621529,-34.9058954,0
              -58.0628388,-34.9057601,0
              -58.0630158,-34.9055841,0
              -58.0630909,-34.9053421,0
              -58.0630909,-34.905087,0
              -58.063105,-34.9046426,0
              -58.0631292,-34.9042483,0
              -58.0631446,-34.9040399,0
              -58.0632706,-34.9037891,0
              -58.0632867,-34.9036748,0
              -58.063257,-34.9035094,0
              -58.0630604,-34.9030369,0
              -58.0630846,-34.9028764,0
              -58.0632133,-34.9027224,0
              -58.0632992,-34.902366,0
              -58.0633211,-34.9021686,0
              -58.0633555,-34.9018557,0
              -58.0632884,-34.9015565,0
              -58.0632214,-34.9013475,0
              -58.063157,-34.9012133,0
              -58.0629052,-34.9008464,0
              -58.0626742,-34.900505,0
              -58.0625535,-34.9003903,0
              -58.0621403,-34.9000237,0
              -58.06183,-34.8997714,0
              -58.0613284,-34.8994876,0
              -58.0610361,-34.8994062,0
              -58.0608761,-34.8993223,0
              -58.060718,-34.8993061,0
              -58.060623,-34.899294,0
              -58.0602486,-34.8993171,0
              -58.0597739,-34.8993545,0
              -58.0595754,-34.8994205,0
              -58.0593179,-34.8995877,0
              -58.0590448,-34.8996877,0
              -58.0585868,-34.8995207,0
              -58.0582075,-34.8993149,0
              -58.057985,-34.8990905,0
              -58.057642,-34.8990114,0
              -58.0574998,-34.8989454,0
              -58.057409,-34.8989099,0
              -58.0573022,-34.8988954,0
              -58.0571649,-34.8989101,0
              -58.0570242,-34.8989573,0
              -58.0568859,-34.8989901,0
              -58.0567652,-34.8989811,0
              -58.0566663,-34.8989483,0
              -58.0565968,-34.8989024,0
              -58.0565418,-34.8988347,0
              -58.0565177,-34.8987693,0
              -58.0565177,-34.8984702,0
              -58.0565003,-34.8983374,0
              -58.0564688,-34.8981999,0
              -58.0563984,-34.898058,0
              -58.0563094,-34.8979526,0
              -58.0561658,-34.8978706,0
              -58.0560182,-34.8977995,0
              -58.0555897,-34.8976606,0
              -58.0552937,-34.8976509,0
              -58.0551129,-34.8976488,0
              -58.0548722,-34.8976631,0
              -58.0546583,-34.8976356,0
              -58.0544221,-34.8975359,0
              -58.0542633,-34.897445,0
              -58.0541029,-34.8973555,0
              -58.0539132,-34.8973082,0
              -58.0533058,-34.8969487,0
              -58.0532284,-34.8968199,0
              -58.0529911,-34.8965477,0
              -58.052808,-34.8963926,0
              -58.0525478,-34.8961396,0
              -58.0524998,-34.8960327,0
              -58.0523881,-34.8957614,0
              -58.0523782,-34.8956351,0
              -58.0524734,-34.8954239,0
              -58.0526544,-34.8950939,0
              -58.0526732,-34.8949828,0
              -58.0526746,-34.8949025,0
              -58.0525806,-34.8947452,0
              -58.0524197,-34.8945945,0
              -58.0522099,-34.8945648,0
              -58.052,-34.8945417,0
              -58.0517908,-34.8944427,0
              -58.0516379,-34.894269,0
              -58.0515923,-34.8941282,0
              -58.0515842,-34.89395,0
              -58.0514608,-34.8937806,0
              -58.0512141,-34.893389,0
              -58.0510639,-34.893301,0
              -58.0509854,-34.8932913,0
              -58.0507618,-34.8932654,0
              -58.050565,-34.8932526,0
              -58.0503182,-34.893191,0
              -58.0502056,-34.8929974,0
              -58.0502217,-34.8928038,0
              -58.0502807,-34.8924474,0
              -58.0502625,-34.892175,0
              -58.050225,-34.8920606,0
              -58.0501275,-34.8918409,0
              -58.0500577,-34.8916429,0
              -58.0499102,-34.8913481,0
              -58.0498485,-34.8912073,0
              -58.0497198,-34.8910907,0
              -58.0494462,-34.8908993,0
              -58.0493282,-34.8907717,0
              -58.0492397,-34.8906419,0
              -58.0491297,-34.8904571,0
              -58.0489956,-34.8902921,0
              -58.0487995,-34.8901559,0
              -58.0486688,-34.8900846,0
              -58.0484643,-34.8899821,0
              -58.048298,-34.8899161,0
              -58.0481558,-34.8897555,0
              -58.047871,-34.8893756,0
              -58.0478033,-34.8892854,0
              -58.0476591,-34.8890917,0
              -58.0476249,-34.889012,0
              -58.0475599,-34.8888629,0
              -58.0476028,-34.8886561,0
              -58.0475545,-34.8884449,0
              -58.0475165,-34.8883733,0
              -58.0474579,-34.8882777,0
              -58.047384,-34.8879477,0
              -58.0473433,-34.8879047,0
              -58.0471266,-34.8877057,0
              -58.0469549,-34.8875693,0
              -58.0466277,-34.8874945,0
              -58.0464916,-34.8874428,0
              -58.0462076,-34.8872908,0
              -58.0458911,-34.8871071,0
              -58.0457823,-34.8869812,0
              -58.045695,-34.8868025,0
              -58.0455287,-34.8865957,0
              -58.0453679,-34.8865313,0
              -58.0452072,-34.8865098,0
              -58.0448075,-34.8864372,0
              -58.0445993,-34.886379,0
              -58.0445568,-34.8863505,0
              -58.0445252,-34.8862957,0
              -58.0444901,-34.8862051,0
              -58.0444873,-34.886088,0
              -58.0445507,-34.8859062,0
              -58.0445838,-34.8856639,0
              -58.0444987,-34.885478,0
              -58.0442841,-34.8852624,0
              -58.0439192,-34.8851038,0
              -58.0432915,-34.884941,0
              -58.0428785,-34.8847474,0
              -58.0425943,-34.8846111,0
              -58.0421006,-34.8842677,0
              -58.041709,-34.8838145,0
              -58.0414247,-34.8834492,0
              -58.04107,-34.8829254,0
              -58.040791,-34.8823578,0
              -58.0405968,-34.8819618,0
              -58.0401688,-34.88146,0
              -58.0398297,-34.8809893,0
              -58.0395572,-34.8808219,0
              -58.0392927,-34.8807412,0
              -58.0389671,-34.8808175,0
              -58.0387794,-34.8808571,0
              -58.0382709,-34.8807952,0
              -58.0380321,-34.880706,0
              -58.0377746,-34.8805608,0
              -58.0376297,-34.8803408,0
              -58.0376379,-34.8797391,0
              -58.0376142,-34.8796345,0
              -58.0374634,-34.8794474,0
              -58.0369083,-34.8790613,0
              -58.0363611,-34.8788149,0
              -58.0358247,-34.8786477,0
              -58.035548,-34.8785962,0
              -58.0354063,-34.878542,0
              -58.0352691,-34.8784905,0
              -58.0350277,-34.8782925,0
              -58.0346743,-34.877855,0
              -58.0345429,-34.877756,0
              -58.0344115,-34.877756,0
              -58.0341843,-34.87781,0
              -58.0340716,-34.8778452,0
              -58.0339115,-34.877863,0
              -58.033754,-34.8778467,0
              -58.0334388,-34.87763,0
              -58.0332128,-34.8774712,0
              -58.0327186,-34.8771115,0
              -58.0325845,-34.876931,0
              -58.0324451,-34.8765903,0
              -58.0323069,-34.8762148,0
              -58.0322094,-34.8760833,0
              -58.0319941,-34.8759897,0
              -58.0318044,-34.8759798,0
              -58.031463,-34.8759787,0
              -58.0312623,-34.8759191,0
              -58.0311224,-34.8757763,0
              -58.0310097,-34.8755893,0
              -58.0308703,-34.8754286,0
              -58.0306181,-34.875246,0
              -58.030188,-34.8747033,0
              -58.0299673,-34.8744448,0
              -58.029844,-34.8742335,0
              -58.0298654,-34.8740971,0
              -58.0299459,-34.8738814,0
              -58.0300253,-34.87362,0
              -58.0300609,-34.8734142,0
              -58.0300065,-34.8731997,0
              -58.0299723,-34.8728972,0
              -58.0299884,-34.8727211,0
              -58.0300474,-34.8725539,0
              -58.0301547,-34.8723559,0
              -58.0302352,-34.8721182,0
              -58.0302888,-34.8719245,0
              -58.0302835,-34.8718233,0
              -58.0300798,-34.871391,0
              -58.0299089,-34.8710939,0
              -58.0297198,-34.8707913,0
              -58.0295201,-34.8706298,0
              -58.0292681,-34.8705278,0
              -58.0285823,-34.8703212,0
              -58.0278911,-34.8701587,0
              -58.0274669,-34.8699689,0
              -58.0273388,-34.8698523,0
              -58.0272631,-34.8697136,0
              -58.0268934,-34.8692256,0
              -58.0260755,-34.8679215,0
              -58.0246279,-34.8656519,0
              -58.0222478,-34.8619808,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>EL RINCON</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-0288D1-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0885515,-34.8731106,0
              -58.1015942,-34.8842613,0
              -58.1107153,-34.8921097,0
              -58.094481,-34.8959388,0
              -58.0942167,-34.8960644,0
              -58.0940773,-34.8961568,0
              -58.0937535,-34.8962577,0
              -58.091715,-34.8967549,0
              -58.0900252,-34.8971817,0
              -58.0894132,-34.8948676,0
              -58.0891973,-34.8937085,0
              -58.0825801,-34.8748685,0
              -58.0853911,-34.8741819,0
              -58.0885515,-34.8731106,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>VILLA ELISA</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-006064-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0574145,-34.846635,0
              -58.0841926,-34.8351751,0
              -58.1197458,-34.8644153,0
              -58.1159612,-34.867219,0
              -58.1202447,-34.8707665,0
              -58.1015942,-34.8842613,0
              -58.0840682,-34.8691886,0
              -58.063995,-34.8739077,0
              -58.0597954,-34.8618629,0
              -58.0624991,-34.8617925,0
              -58.0639582,-34.8615988,0
              -58.0649238,-34.8612643,0
              -58.0656584,-34.8608762,0
              -58.0652078,-34.8607266,0
              -58.0649074,-34.8605857,0
              -58.0647357,-34.8603656,0
              -58.0644246,-34.8603216,0
              -58.0642207,-34.8602072,0
              -58.0639418,-34.8599078,0
              -58.0633302,-34.8594237,0
              -58.0632069,-34.8591771,0
              -58.06318,-34.8588646,0
              -58.0633946,-34.8583584,0
              -58.0633759,-34.8581807,0
              -58.063054,-34.8578374,0
              -58.0624864,-34.8574485,0
              -58.0619167,-34.8571331,0
              -58.0612516,-34.8566753,0
              -58.0606829,-34.8558829,0
              -58.0603919,-34.8551505,0
              -58.0604992,-34.8518665,0
              -58.0602496,-34.8510931,0
              -58.059952,-34.850537,0
              -58.0587397,-34.8487496,0
              -58.0574145,-34.846635,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>SAN CARLOS</name>
      <description><![CDATA[Descripción: <br>nombre: SAN CARLOS<br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-558B2F-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>SAN CARLOS</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9936546,-34.9343563,0
              -57.9870233,-34.9283492,0
              -57.9937048,-34.9232149,0
              -57.993704,-34.9229764,0
              -57.9940981,-34.9226516,0
              -57.9953773,-34.9216978,0
              -57.9970505,-34.9204543,0
              -58.000421,-34.9179475,0
              -58.0072391,-34.9128742,0
              -58.010551,-34.915888,0
              -58.023286,-34.912726,0
              -58.0339592,-34.9254542,0
              -58.0056773,-34.9453686,0
              -57.9993323,-34.9395824,0
              -57.9936546,-34.9343563,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>LISANDRO OLMOS</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-558B2F-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0241984,-34.9622704,0
              -58.0345363,-34.9715415,0
              -58.0356856,-34.9706876,0
              -58.0377563,-34.9725778,0
              -58.0366298,-34.9733866,0
              -58.0407183,-34.9771136,0
              -58.0435586,-34.9750578,0
              -58.0475901,-34.9721421,0
              -58.0495984,-34.9739559,0
              -58.0427674,-34.9790291,0
              -58.066665,-35.0007943,0
              -58.0665336,-35.0009679,0
              -58.0214308,-35.0349149,0
              -58.0234347,-35.0366254,0
              -58.0255407,-35.0384809,0
              -58.0297099,-35.0419808,0
              -58.0380977,-35.0489408,0
              -58.0320315,-35.0535314,0
              -58.031302,-35.0528903,0
              -58.0199183,-35.0601972,0
              -58.0093504,-35.0669484,0
              -58.006475,-35.0690383,0
              -58.0019438,-35.0724698,0
              -57.9904882,-35.0809625,0
              -57.9847268,-35.0852557,0
              -57.9797271,-35.0889957,0
              -57.966331,-35.099061,0
              -57.9661379,-35.0990171,0
              -57.9495129,-35.0840919,0
              -57.9677575,-35.0663085,0
              -57.9789128,-35.0513732,0
              -57.9931816,-35.0275276,0
              -57.9944691,-35.0256298,0
              -57.9955342,-35.024587,0
              -58.0355195,-34.9947963,0
              -58.010625,-34.972293,0
              -58.0241984,-34.9622704,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>MALVINAS ARGENTINAS</name>
      <description><![CDATA[Descripción: <br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-0097A7-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -58.0241984,-34.9622704,0
              -58.010625,-34.9722754,0
              -57.97356,-34.9386764,0
              -57.9870233,-34.9283492,0
              -58.0056773,-34.9453686,0
              -58.0097463,-34.9490447,0
              -58.0144541,-34.9533054,0
              -58.0241984,-34.9622704,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>ARANA</name>
      <description><![CDATA[Descripción: ARANA<br>nombre: <br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-A1C2FA-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value>ARANA</value>
        </Data>
        <Data name="nombre">
          <value/>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.7541626,-34.9723163,0
              -57.7574344,-34.9672077,0
              -57.7586468,-34.9661835,0
              -57.7675839,-34.9596067,0
              -57.76855,-34.9589696,0
              -57.769204,-34.9586922,0
              -57.7698262,-34.9584987,0
              -57.7703939,-34.9584068,0
              -57.7711181,-34.9583717,0
              -57.7716545,-34.9584068,0
              -57.7723304,-34.9585563,0
              -57.7739773,-34.9591367,0
              -57.7840308,-34.9626801,0
              -57.8034211,-34.9642845,0
              -57.842145,-34.948755,0
              -57.84334,-34.948085,0
              -57.8555363,-34.9604734,0
              -57.860204,-34.957013,0
              -57.8985175,-34.9910806,0
              -57.9076826,-34.9841841,0
              -57.9233939,-34.9985687,0
              -57.9152005,-35.0046162,0
              -57.9228192,-35.0118594,0
              -57.9154485,-35.0175315,0
              -57.9173299,-35.0192102,0
              -57.9175816,-35.0194387,0
              -57.9177921,-35.0201977,0
              -57.917894,-35.0205227,0
              -57.9184144,-35.0223854,0
              -57.9194404,-35.0259703,0
              -57.919415,-35.0263448,0
              -57.9176975,-35.0283775,0
              -57.9171507,-35.0279386,0
              -57.9166412,-35.0274637,0
              -57.9165154,-35.0272481,0
              -57.9164135,-35.026945,0
              -57.9161158,-35.0265013,0
              -57.9155522,-35.0260756,0
              -57.9150533,-35.0259658,0
              -57.9147439,-35.0259464,0
              -57.9143058,-35.0260457,0
              -57.9138686,-35.0259886,0
              -57.9136888,-35.0258876,0
              -57.9134581,-35.02587,0
              -57.9132166,-35.0257295,0
              -57.9131142,-35.0256893,0
              -57.913025,-35.0256582,0
              -57.9129807,-35.025637,0
              -57.9129338,-35.0256069,0
              -57.9128861,-35.0255742,0
              -57.9127687,-35.0255305,0
              -57.9124416,-35.0254176,0
              -57.9121932,-35.0253306,0
              -57.9116351,-35.0251471,0
              -57.9113304,-35.0251097,0
              -57.91121,-35.0251108,0
              -57.9111111,-35.0251207,0
              -57.9109874,-35.0251537,0
              -57.9109417,-35.0251559,0
              -57.910912,-35.0251515,0
              -57.9105781,-35.0250537,0
              -57.9101865,-35.0249483,0
              -57.90999,-35.0249368,0
              -57.9097999,-35.0249096,0
              -57.9095843,-35.0248407,0
              -57.909072,-35.0246814,0
              -57.9088887,-35.0246235,0
              -57.9087827,-35.0246069,0
              -57.9086839,-35.0246057,0
              -57.9085544,-35.0246309,0
              -57.9081775,-35.0247583,0
              -57.9076465,-35.0249428,0
              -57.9073829,-35.0250082,0
              -57.9072361,-35.0250032,0
              -57.9071522,-35.0249972,0
              -57.907055,-35.024967,0
              -57.90688,-35.0248744,0
              -57.9067938,-35.0248067,0
              -57.9067693,-35.024739,0
              -57.9067546,-35.0245452,0
              -57.906658,-35.0243344,0
              -57.9065239,-35.0241587,0
              -57.9063174,-35.0240093,0
              -57.9060559,-35.0239038,0
              -57.9058433,-35.0238764,0
              -57.9056619,-35.0238627,0
              -57.9055886,-35.0238426,0
              -57.9055422,-35.0238116,0
              -57.9054497,-35.0237304,0
              -57.9053196,-35.0235898,0
              -57.9050916,-35.0232317,0
              -57.9049066,-35.0230225,0
              -57.9048288,-35.0229725,0
              -57.9045753,-35.0228363,0
              -57.904407,-35.0227759,0
              -57.9042333,-35.0227441,0
              -57.9039128,-35.0227513,0
              -57.9033837,-35.0228114,0
              -57.9028881,-35.0229232,0
              -57.9023558,-35.0233591,0
              -57.9019969,-35.0236916,0
              -57.9018427,-35.0237663,0
              -57.9014846,-35.0238366,0
              -57.9005462,-35.0238513,0
              -57.9003062,-35.0238769,0
              -57.9000984,-35.0239465,0
              -57.8999691,-35.0239728,0
              -57.8997887,-35.0240116,0
              -57.8993786,-35.0240207,0
              -57.8990957,-35.023925,0
              -57.8989329,-35.0238171,0
              -57.8988453,-35.0236806,0
              -57.8987702,-35.0233665,0
              -57.898679,-35.0231293,0
              -57.8986463,-35.0227764,0
              -57.8987502,-35.0224836,0
              -57.8988292,-35.0221936,0
              -57.8988972,-35.0219789,0
              -57.8988828,-35.0218026,0
              -57.8988675,-35.0216079,0
              -57.8987173,-35.0213531,0
              -57.8984788,-35.0211354,0
              -57.8981908,-35.0209284,0
              -57.8980711,-35.0206785,0
              -57.8979853,-35.0204149,0
              -57.8980175,-35.0202392,0
              -57.8982213,-35.0200547,0
              -57.8982428,-35.0197999,0
              -57.8981248,-35.0194396,0
              -57.8980751,-35.019165,0
              -57.897942,-35.0190041,0
              -57.873978,-34.9970206,0
              -57.8733658,-34.9974836,0
              -57.8430402,-34.9697688,0
              -57.8131593,-34.9919591,0
              -57.812948,-34.9920571,0
              -57.8127709,-34.992101,0
              -57.8125885,-34.9920439,0
              -57.8110704,-34.990664,0
              -57.8109545,-34.9906253,0
              -57.8108284,-34.9906517,0
              -57.8107539,-34.9906947,0
              -57.796214,-35.001547,0
              -57.7893701,-35.0042382,0
              -57.7541626,-34.9723163,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>PARQUE SICARDI - VILLA GARIBALDI</name>
      <description><![CDATA[Descripción: <br>nombre: PARQUE SICARDI - VILLA GARIBALDI<br><br>FRACCION: <br>CLAVEF: ]]></description>
      <styleUrl>#poly-FF5252-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value/>
        </Data>
        <Data name="nombre">
          <value>PARQUE SICARDI - VILLA GARIBALDI
</value>
        </Data>
        <Data name="FRACCION">
          <value/>
        </Data>
        <Data name="CLAVEF">
          <value/>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.7893701,-35.0042382,0
              -57.796214,-35.001547,0
              -57.8107539,-34.9906947,0
              -57.8108284,-34.9906517,0
              -57.8109545,-34.9906253,0
              -57.8110704,-34.990664,0
              -57.8125885,-34.9920439,0
              -57.8127709,-34.992101,0
              -57.812948,-34.9920571,0
              -57.8131593,-34.9919591,0
              -57.8430402,-34.9697688,0
              -57.8733658,-34.9974836,0
              -57.873978,-34.9970206,0
              -57.897942,-35.0190041,0
              -57.8973738,-35.0188509,0
              -57.8970961,-35.0188378,0
              -57.8967622,-35.0188773,0
              -57.8965691,-35.0190091,0
              -57.8960751,-35.0191974,0
              -57.8958165,-35.0192755,0
              -57.8954625,-35.0193062,0
              -57.8952919,-35.0193468,0
              -57.895072,-35.0193424,0
              -57.8946375,-35.0193775,0
              -57.8943263,-35.0193248,0
              -57.8941244,-35.0192508,0
              -57.8939252,-35.0190256,0
              -57.8938582,-35.0189706,0
              -57.8936302,-35.0188564,0
              -57.893429,-35.0186697,0
              -57.8932976,-35.0185796,0
              -57.8930925,-35.018534,0
              -57.8928577,-35.0185533,0
              -57.892627,-35.0187268,0
              -57.8924473,-35.0189443,0
              -57.8923427,-35.0190849,0
              -57.8922503,-35.0191798,0
              -57.891994,-35.0192145,0
              -57.8918212,-35.0191474,0
              -57.8914688,-35.0190091,0
              -57.8911585,-35.0189146,0
              -57.8908412,-35.0189037,0
              -57.8907965,-35.0189426,0
              -57.8906947,-35.019036,0
              -57.8904989,-35.0190251,0
              -57.8900885,-35.0188054,0
              -57.8899034,-35.0186912,0
              -57.8898015,-35.0185704,0
              -57.8896942,-35.0185001,0
              -57.8894422,-35.0184565,0
              -57.8888922,-35.0184813,0
              -57.8886107,-35.0185049,0
              -57.8882753,-35.0184505,0
              -57.8878677,-35.0184104,0
              -57.8873662,-35.0184126,0
              -57.8869556,-35.0183539,0
              -57.8865374,-35.0182435,0
              -57.8864113,-35.0181776,0
              -57.8862046,-35.0182177,0
              -57.8861753,-35.018305,0
              -57.8861672,-35.0184609,0
              -57.8860867,-35.018551,0
              -57.8860168,-35.0185779,0
              -57.8857434,-35.0186213,0
              -57.8852097,-35.0187509,0
              -57.8850246,-35.0187157,0
              -57.8849361,-35.0187289,0
              -57.8848503,-35.0187663,0
              -57.8847991,-35.0187603,0
              -57.8846518,-35.0187223,0
              -57.8845713,-35.0187443,0
              -57.8844504,-35.0188547,0
              -57.88437,-35.0189821,0
              -57.8842226,-35.0191331,0
              -57.8840331,-35.0192488,0
              -57.8837908,-35.0192298,0
              -57.8837103,-35.0191375,0
              -57.8836433,-35.0190936,0
              -57.8834376,-35.0191258,0
              -57.8831605,-35.0193308,0
              -57.8828305,-35.0194209,0
              -57.8825918,-35.0195417,0
              -57.8825382,-35.0196251,0
              -57.8824121,-35.0196998,0
              -57.8822431,-35.0197086,0
              -57.8818659,-35.0197892,0
              -57.8813527,-35.0200535,0
              -57.8811792,-35.0201143,0
              -57.8809432,-35.0202504,0
              -57.8805968,-35.0206133,0
              -57.8805069,-35.0206682,0
              -57.8803701,-35.0207231,0
              -57.8801381,-35.0208461,0
              -57.8799338,-35.0210033,0
              -57.8798632,-35.0210636,0
              -57.8798323,-35.0211372,0
              -57.8795239,-35.0214524,0
              -57.8794166,-35.0215303,0
              -57.8793992,-35.0215798,0
              -57.8794139,-35.0216413,0
              -57.8794886,-35.0217242,0
              -57.8795861,-35.0218501,0
              -57.8795901,-35.0219413,0
              -57.8795606,-35.0220237,0
              -57.8795204,-35.0221005,0
              -57.8794426,-35.0221708,0
              -57.8793434,-35.0221994,0
              -57.8792683,-35.0222499,0
              -57.8792012,-35.0223378,0
              -57.8791771,-35.0224454,0
              -57.8790778,-35.0227046,0
              -57.8790805,-35.0227837,0
              -57.8791663,-35.0231461,0
              -57.8792656,-35.0233361,0
              -57.8794834,-35.0235539,0
              -57.87958,-35.0236791,0
              -57.8796149,-35.0237889,0
              -57.8796417,-35.0239844,0
              -57.8796149,-35.0240723,0
              -57.8793617,-35.0244319,0
              -57.8792973,-35.0245461,0
              -57.8792156,-35.024659,0
              -57.8791927,-35.0246976,0
              -57.8791498,-35.0248382,0
              -57.8791418,-35.025098,0
              -57.8791042,-35.0254862,0
              -57.8790975,-35.0257146,0
              -57.8790184,-35.0258897,0
              -57.8789567,-35.0259782,0
              -57.878899,-35.0260275,0
              -57.8788293,-35.0260901,0
              -57.8787059,-35.0262539,0
              -57.8784525,-35.0264396,0
              -57.8782016,-35.0265702,0
              -57.8777926,-35.0266942,0
              -57.877098,-35.0270265,0
              -57.8765897,-35.0272967,0
              -57.876445,-35.027456,0
              -57.8764275,-35.0277993,0
              -57.8763991,-35.0279637,0
              -57.8762772,-35.0281429,0
              -57.8757729,-35.0285272,0
              -57.8750098,-35.0287391,0
              -57.8745445,-35.0286958,0
              -57.8742763,-35.0284761,0
              -57.8740394,-35.0283467,0
              -57.8737811,-35.0283052,0
              -57.8733214,-35.0283268,0
              -57.8728605,-35.0284834,0
              -57.8723894,-35.0287875,0
              -57.8723593,-35.0289732,0
              -57.8722057,-35.0291017,0
              -57.8717767,-35.0293196,0
              -57.8712378,-35.0293992,0
              -57.8709588,-35.0296666,0
              -57.8707684,-35.0297957,0
              -57.8704197,-35.0298682,0
              -57.869996,-35.0299363,0
              -57.8692685,-35.0301226,0
              -57.8687186,-35.0300315,0
              -57.8681848,-35.0298788,0
              -57.8674408,-35.0294859,0
              -57.8665895,-35.0288821,0
              -57.8664553,-35.0289765,0
              -57.8497383,-35.040522,0
              -57.8622753,-35.0519431,0
              -57.8512981,-35.0594561,0
              -57.7893701,-35.0042382,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
    <Placemark>
      <name>LOS HORNOS</name>
      <description><![CDATA[Descripción: LOS HORNOS<br>nombre: LOS HORNOS<br>FRACCION: LOS HORNOS<br>CLAVEF: LOS HORNOS]]></description>
      <styleUrl>#poly-F57C00-1200-77</styleUrl>
      <ExtendedData>
        <Data name="Descripción">
          <value>LOS HORNOS</value>
        </Data>
        <Data name="nombre">
          <value>LOS HORNOS</value>
        </Data>
        <Data name="FRACCION">
          <value>LOS HORNOS</value>
        </Data>
        <Data name="CLAVEF">
          <value>LOS HORNOS</value>
        </Data>
      </ExtendedData>
      <Polygon>
        <outerBoundaryIs>
          <LinearRing>
            <tessellate>1</tessellate>
            <coordinates>
              -57.9122651,-35.1119482,0
              -57.8512981,-35.0594561,0
              -57.8622753,-35.0519431,0
              -57.8497383,-35.040522,0
              -57.8665895,-35.0288821,0
              -57.8674408,-35.0294859,0
              -57.8681848,-35.0298788,0
              -57.8687186,-35.0300315,0
              -57.8692685,-35.0301226,0
              -57.869996,-35.0299363,0
              -57.8704197,-35.0298682,0
              -57.8707684,-35.0297957,0
              -57.8709588,-35.0296666,0
              -57.8712378,-35.0293992,0
              -57.8717767,-35.0293196,0
              -57.8722057,-35.0291017,0
              -57.8723593,-35.0289732,0
              -57.8723894,-35.0287875,0
              -57.8728605,-35.0284834,0
              -57.8733214,-35.0283268,0
              -57.8737811,-35.0283052,0
              -57.8740394,-35.0283467,0
              -57.8742763,-35.0284761,0
              -57.8745445,-35.0286958,0
              -57.8750098,-35.0287391,0
              -57.8757729,-35.0285272,0
              -57.8762772,-35.0281429,0
              -57.8764275,-35.0277993,0
              -57.876445,-35.027456,0
              -57.877098,-35.0270265,0
              -57.8777926,-35.0266942,0
              -57.8782016,-35.0265702,0
              -57.8784925,-35.0264349,0
              -57.8787059,-35.0262539,0
              -57.8788293,-35.0260901,0
              -57.8789567,-35.0259782,0
              -57.8790975,-35.0257146,0
              -57.8791498,-35.0248382,0
              -57.8792156,-35.024659,0
              -57.8794642,-35.0242865,0
              -57.8796149,-35.0240723,0
              -57.8796417,-35.0239844,0
              -57.87958,-35.0236791,0
              -57.8793804,-35.0234639,0
              -57.8792656,-35.0233361,0
              -57.8791663,-35.0231461,0
              -57.8790805,-35.0227837,0
              -57.8790778,-35.0227046,0
              -57.8791953,-35.0224074,0
              -57.8792012,-35.0223378,0
              -57.8792683,-35.0222499,0
              -57.8793434,-35.0221994,0
              -57.8794426,-35.0221708,0
              -57.8795204,-35.0221005,0
              -57.8795901,-35.0219413,0
              -57.8795861,-35.0218501,0
              -57.8795011,-35.0217396,0
              -57.8794139,-35.0216413,0
              -57.8793992,-35.0215798,0
              -57.8794166,-35.0215303,0
              -57.8794953,-35.0214726,0
              -57.8796107,-35.0213715,0
              -57.8797422,-35.0212233,0
              -57.8798253,-35.0211211,0
              -57.8798632,-35.0210636,0
              -57.8801381,-35.0208461,0
              -57.8803081,-35.0207598,0
              -57.8805069,-35.0206682,0
              -57.8805968,-35.0206133,0
              -57.8808365,-35.0203336,0
              -57.8810591,-35.0201733,0
              -57.8812362,-35.0201008,0
              -57.8814025,-35.0200437,0
              -57.8816975,-35.0198548,0
              -57.8820757,-35.0197406,0
              -57.8823761,-35.019701,0
              -57.8825382,-35.0196251,0
              -57.8826282,-35.0195297,0
              -57.8828305,-35.0194209,0
              -57.8831605,-35.0193308,0
              -57.8834376,-35.0191258,0
              -57.8836433,-35.0190936,0
              -57.8837908,-35.0192298,0
              -57.883905,-35.0192353,0
              -57.8840766,-35.0192441,0
              -57.884259,-35.0190992,0
              -57.88437,-35.0189821,0
              -57.8844504,-35.0188547,0
              -57.8845713,-35.0187443,0
              -57.8846518,-35.0187223,0
              -57.8847991,-35.0187603,0
              -57.8849361,-35.0187289,0
              -57.8850637,-35.0187169,0
              -57.8852097,-35.0187509,0
              -57.8856109,-35.0186686,0
              -57.8860168,-35.0185779,0
              -57.8861419,-35.018528,0
              -57.8862009,-35.0184182,0
              -57.8861741,-35.0182512,0
              -57.886276,-35.0182029,0
              -57.8864113,-35.0181776,0
              -57.8865764,-35.0182776,0
              -57.8868232,-35.0183347,0
              -57.8871504,-35.0183787,0
              -57.887703,-35.0184094,0
              -57.8882126,-35.0184621,0
              -57.8886107,-35.0185049,0
              -57.889264,-35.0184709,0
              -57.8894422,-35.0184565,0
              -57.8896942,-35.0185001,0
              -57.889838,-35.0186027,0
              -57.8899614,-35.0187345,0
              -57.8902001,-35.0188575,0
              -57.8904989,-35.0190251,0
              -57.8906947,-35.019036,0
              -57.8908412,-35.0189037,0
              -57.8911585,-35.0189146,0
              -57.8914688,-35.0190091,0
              -57.891994,-35.0192145,0
              -57.8922503,-35.0191798,0
              -57.8923427,-35.0190849,0
              -57.892627,-35.0187268,0
              -57.8928577,-35.0185533,0
              -57.8930925,-35.018534,0
              -57.8932976,-35.0185796,0
              -57.893429,-35.0186697,0
              -57.8935019,-35.0187411,0
              -57.8936302,-35.0188564,0
              -57.8938582,-35.0189706,0
              -57.8939252,-35.0190256,0
              -57.8940377,-35.019153,0
              -57.8941244,-35.0192508,0
              -57.8943263,-35.0193248,0
              -57.8944031,-35.019343,0
              -57.8946375,-35.0193775,0
              -57.895072,-35.0193424,0
              -57.8952919,-35.0193468,0
              -57.8954625,-35.0193062,0
              -57.8958165,-35.0192755,0
              -57.8960751,-35.0191974,0
              -57.8965691,-35.0190091,0
              -57.8967622,-35.0188773,0
              -57.8970961,-35.0188378,0
              -57.8973738,-35.0188509,0
              -57.897942,-35.0190041,0
              -57.8980751,-35.019165,0
              -57.8981248,-35.0194396,0
              -57.8981889,-35.0196353,0
              -57.8982428,-35.0197999,0
              -57.8982213,-35.0200547,0
              -57.8980175,-35.0202392,0
              -57.8979853,-35.0204149,0
              -57.8980711,-35.0206785,0
              -57.8981908,-35.0209284,0
              -57.8984788,-35.0211354,0
              -57.8987173,-35.0213531,0
              -57.8988675,-35.0216079,0
              -57.8988972,-35.0219789,0
              -57.8987468,-35.0224997,0
              -57.8986463,-35.0227764,0
              -57.8986556,-35.022873,0
              -57.898679,-35.0231293,0
              -57.8987702,-35.0233665,0
              -57.8988453,-35.0236806,0
              -57.8989329,-35.0238171,0
              -57.8990957,-35.023925,0
              -57.8993786,-35.0240207,0
              -57.8995756,-35.0240153,0
              -57.8997887,-35.0240116,0
              -57.9000984,-35.0239465,0
              -57.9003062,-35.0238769,0
              -57.9005462,-35.0238513,0
              -57.9014846,-35.0238366,0
              -57.9018427,-35.0237663,0
              -57.9019969,-35.0236916,0
              -57.9023983,-35.0233294,0
              -57.9028881,-35.0229232,0
              -57.9033837,-35.0228114,0
              -57.9039128,-35.0227513,0
              -57.9042253,-35.022754,0
              -57.904407,-35.0227759,0
              -57.9045753,-35.0228363,0
              -57.9048288,-35.0229725,0
              -57.9049066,-35.0230225,0
              -57.9049602,-35.0230834,0
              -57.9050916,-35.0232317,0
              -57.9053196,-35.0235898,0
              -57.9054497,-35.0237304,0
              -57.9055422,-35.0238116,0
              -57.9055886,-35.0238426,0
              -57.9056619,-35.0238627,0
              -57.9058165,-35.023872,0
              -57.9060559,-35.0239038,0
              -57.9063174,-35.0240093,0
              -57.9065239,-35.0241587,0
              -57.906658,-35.0243344,0
              -57.9067546,-35.0245452,0
              -57.9067693,-35.024739,0
              -57.9067938,-35.0248067,0
              -57.90688,-35.0248744,0
              -57.907055,-35.024967,0
              -57.9071522,-35.0249972,0
              -57.9072361,-35.0250032,0
              -57.9073829,-35.0250082,0
              -57.9076465,-35.0249428,0
              -57.9085369,-35.0246353,0
              -57.9086839,-35.0246057,0
              -57.9087827,-35.0246069,0
              -57.9088887,-35.0246235,0
              -57.9090324,-35.0246642,0
              -57.9096259,-35.0248561,0
              -57.9097999,-35.0249096,0
              -57.90999,-35.0249368,0
              -57.9101865,-35.0249483,0
              -57.9105781,-35.0250537,0
              -57.910912,-35.0251515,0
              -57.9109417,-35.0251559,0
              -57.9109874,-35.0251537,0
              -57.9111111,-35.0251207,0
              -57.91121,-35.0251108,0
              -57.9113304,-35.0251097,0
              -57.9116351,-35.0251471,0
              -57.9124215,-35.025411,0
              -57.9126518,-35.0254904,0
              -57.9128861,-35.0255742,0
              -57.9129338,-35.0256069,0
              -57.9129857,-35.0256403,0
              -57.913025,-35.0256582,0
              -57.9131235,-35.0256944,0
              -57.9132166,-35.0257295,0
              -57.9134581,-35.02587,0
              -57.9136888,-35.0258876,0
              -57.9138686,-35.0259886,0
              -57.9143058,-35.0260457,0
              -57.9147439,-35.0259464,0
              -57.9150533,-35.0259658,0
              -57.9155522,-35.0260756,0
              -57.9161158,-35.0265013,0
              -57.9164135,-35.026945,0
              -57.9165154,-35.0272481,0
              -57.9166412,-35.0274637,0
              -57.9171586,-35.0279535,0
              -57.9176975,-35.0283775,0
              -57.919415,-35.0263448,0
              -57.9194404,-35.0259703,0
              -57.9175816,-35.0194387,0
              -57.9154485,-35.0175315,0
              -57.9228192,-35.0118594,0
              -57.9152005,-35.0046162,0
              -57.9233939,-34.9985687,0
              -57.9158124,-34.9915988,0
              -57.959174,-34.959577,0
              -57.9530118,-34.9539169,0
              -57.96722,-34.943414,0
              -57.967232,-34.943032,0
              -57.967415,-34.94267,0
              -57.9710717,-34.9400098,0
              -57.9720299,-34.93968,0
              -57.97356,-34.938694,0
              -58.0355195,-34.9947963,0
              -57.9955342,-35.024587,0
              -57.9944691,-35.0256298,0
              -57.9797396,-35.0501198,0
              -57.9677575,-35.0663085,0
              -57.9495129,-35.0840919,0
              -57.9392976,-35.0936588,0
              -57.9336046,-35.0999667,0
              -57.9218887,-35.1092707,0
              -57.919067,-35.1107013,0
              -57.9165942,-35.1112746,0
              -57.9122651,-35.1119482,0
            </coordinates>
          </LinearRing>
        </outerBoundaryIs>
      </Polygon>
    </Placemark>
  </Document>
</kml>

library(shiny)
library(sf)
library(readxl)
library(dplyr)
library(tidyr)
library(stringr)
library(leaflet)
library(leaflet.extras)
library(htmltools)
library(plotly)

# ==============================================================================
# CARGA DE DATOS BASE
# ==============================================================================

capa_laplata <- st_read("LA PLATA.kml", quiet = TRUE) %>% 
  mutate(
    Name = as.character(Name),
    barrio_normalizado = str_trim(toupper(Name))
  ) %>% 
  st_transform(crs = 4326)

reclamos_raw <- read_excel("Reclamos.xlsx")

# Aseguramos la columna DELEGACION
if ("DELEGACION" %in% names(reclamos_raw)) {
  reclamos_raw <- reclamos_raw %>% mutate(DELEGACION = str_trim(as.character(DELEGACION)))
} else {
  reclamos_raw$DELEGACION <- "SIN ESPECIFICAR"
}

# Aseguramos la columna AREA ASIGNADA
if ("AREA ASIGNADA" %in% names(reclamos_raw)) {
  reclamos_raw <- reclamos_raw %>% mutate(`AREA ASIGNADA` = str_trim(as.character(`AREA ASIGNADA`)))
} else {
  reclamos_raw$`AREA ASIGNADA` <- "SIN ESPECIFICAR"
}

# Aseguramos la columna SUBTIPO | CARATULA
if (!("SUBTIPO | CARATULA" %in% names(reclamos_raw))) {
  reclamos_raw$`SUBTIPO | CARATULA` <- "SIN ESPECIFICAR"
}

# ==============================================================================
# LÓGICA DEL SERVIDOR (SERVER FUNCTION)
# ==============================================================================

server <- function(input, output, session) {
  
  # ----------------------------------------------------------------------------
  # FILTROS DINÁMICOS
  # ----------------------------------------------------------------------------
  observe({
    delegaciones <- c("Todos", sort(unique(na.omit(reclamos_raw$DELEGACION))))
    areas <- c("Todos", sort(unique(na.omit(reclamos_raw$`AREA ASIGNADA`))))
    
    updateSelectInput(session, "filtro_delegacion", choices = delegaciones, selected = "Todos")
    updateSelectInput(session, "filtro_area", choices = areas, selected = "Todos")
  })
  
  # Actualización en cascada para Subtipos según Delegación y Área seleccionadas
  observe({
    datos_temp <- reclamos_raw
    if (!is.null(input$filtro_delegacion) && input$filtro_delegacion != "Todos") {
      datos_temp <- datos_temp %>% filter(DELEGACION == input$filtro_delegacion)
    }
    if (!is.null(input$filtro_area) && input$filtro_area != "Todos") {
      datos_temp <- datos_temp %>% filter(`AREA ASIGNADA` == input$filtro_area)
    }
    
    subtipos <- c("Todos", sort(unique(na.omit(datos_temp$`SUBTIPO | CARATULA`))))
    updateSelectInput(session, "filtro_subtipo", choices = subtipos, selected = "Todos")
  })
  
  # Filtrado reactivo general
  reclamos_filtrados <- reactive({
    datos <- reclamos_raw
    if (!is.null(input$filtro_delegacion) && input$filtro_delegacion != "Todos") {
      datos <- datos %>% filter(DELEGACION == input$filtro_delegacion)
    }
    if (!is.null(input$filtro_area) && input$filtro_area != "Todos") {
      datos <- datos %>% filter(`AREA ASIGNADA` == input$filtro_area)
    }
    if (!is.null(input$filtro_subtipo) && input$filtro_subtipo != "Todos") {
      datos <- datos %>% filter(`SUBTIPO | CARATULA` == input$filtro_subtipo)
    }
    datos
  })
  
  puntos_reclamos_sf <- reactive({
    reclamos_filtrados() %>% 
      filter(!is.na(COORDENADAS)) %>% 
      separate(COORDENADAS, into = c("lat", "lng"), sep = ",", remove = FALSE, convert = TRUE) %>% 
      filter(!is.na(lat), !is.na(lng)) %>% 
      st_as_sf(coords = c("lng", "lat"), crs = 4326, remove = FALSE)
  })
  
  # ----------------------------------------------------------------------------
  # GRÁFICO BARRAS: ÁREA OPERATIVA
  # ----------------------------------------------------------------------------
  output$grafico_area_operativa <- renderPlotly({
    datos_grafico <- reclamos_filtrados() %>% 
      count(`AREA ASIGNADA`, name = "total") %>% 
      filter(!is.na(`AREA ASIGNADA`)) %>% 
      arrange(total)
    
    if(nrow(datos_grafico) == 0) return(NULL)
    
    plot_ly(
      data = datos_grafico,
      x = ~total,
      y = ~reorder(`AREA ASIGNADA`, total),
      type = 'bar',
      orientation = 'h',
      marker = list(
        color = '#0284c7',
        line = list(color = '#38bdf8', width = 1)
      ),
      hoverinfo = "text",
      text = ~paste0("<b>", `AREA ASIGNADA`, "</b><br>Reclamos: ", format(total, big.mark = "."))
    ) %>% 
      layout(
        paper_bgcolor = 'rgba(0,0,0,0)',
        plot_bgcolor = 'rgba(0,0,0,0)',
        margin = list(l = 10, r = 10, t = 10, b = 20),
        xaxis = list(
          title = "",
          tickfont = list(color = '#94a3b8', size = 10),
          gridcolor = '#1e293b',
          zerolinecolor = '#334155'
        ),
        yaxis = list(
          title = "",
          tickfont = list(color = '#f1f5f9', size = 10),
          autorange = "reversed"
        )
      ) %>% 
      config(displayModeBar = FALSE)
  })
  
  # ----------------------------------------------------------------------------
  # MAPA Y PROCESAMIENTO GEOGRÁFICO
  # ----------------------------------------------------------------------------
  datos_procesados <- reactive({
    datos <- reclamos_filtrados() %>% 
      select(delegacion = `DELEGACION`, subtipo_caratula = `SUBTIPO | CARATULA`) %>% 
      filter(!is.na(delegacion), !is.na(subtipo_caratula)) %>% 
      mutate(delegacion = str_trim(toupper(as.character(delegacion))))
    
    if (nrow(datos) == 0) {
      empty_map <- capa_laplata %>% mutate(total_reclamos = 0, html_final = "<div>Sin datos</div>")
      return(list(mapa_data = empty_map, html_tabla_flotante = "<div style='color:white; padding:10px;'>Sin datos.</div>"))
    }
    
    ranking_general_subtipo <- datos %>% 
      count(subtipo_caratula) %>% 
      arrange(desc(n)) %>% 
      mutate(ranking_num = row_number(), pct_general = (n / sum(n)) * 100, subtipo_con_ranking = paste0(ranking_num, ". ", subtipo_caratula))
    
    desviaciones_subtipo <- datos %>% 
      count(delegacion, subtipo_caratula) %>% 
      group_by(delegacion) %>% 
      mutate(total_delegacion = sum(n), pct_local = (n / total_delegacion) * 100) %>% 
      ungroup() %>% 
      left_join(ranking_general_subtipo %>% select(subtipo_caratula, pct_general, subtipo_con_ranking), by = "subtipo_caratula") %>% 
      mutate(desviacion = pct_local - pct_general) %>% 
      arrange(delegacion, desc(abs(desviacion)))
    
    popups_subtipo_html <- desviaciones_subtipo %>% 
      mutate(
        estado = if_else(desviacion > 0, "▲ Encima", "▼ Debajo"),
        color_estado = if_else(desviacion > 0, "#60a5fa", "#f87171"),
        fila_html = sprintf("<tr><td style='padding:4px; font-size:11px; border-bottom:1px solid #334155; color:#cbd5e1;'>%s</td><td style='padding:4px; text-align:right; font-size:11px; color:%s; font-weight:bold; border-bottom:1px solid #334155;'>%s (%+.1f%%)</td></tr>", subtipo_con_ranking, color_estado, estado, desviacion)
      ) %>% 
      group_by(delegacion) %>% 
      summarise(total_reclamos = first(total_delegacion), tabla_completa = paste(head(fila_html, 15), collapse = "")) %>% 
      mutate(html_final = sprintf("<div style='min-width:300px; max-height:260px; overflow-y:auto; font-family:Arial; color:#f8fafc; background-color:#1e293b; padding:10px; border-radius:6px;'><h4 style='margin:0; color:#007a87; font-size:14px;'>Delegación: %s</h4><p style='margin:0 0 6px 0; font-size:11px; color:#94a3b8;'>Total: <strong>%s</strong></p><table style='width:100%%;'>%s</table></div>", delegacion, format(total_reclamos, big.mark = "."), tabla_completa))
    
    filas_tabla_general <- ranking_general_subtipo %>% 
      mutate(fila = sprintf("<tr><td style='padding:4px; font-size:11px; color:#cbd5e1;'>%s</td><td style='padding:4px; text-align:right; font-size:11px; color:#fff;'>%s</td><td style='padding:4px; text-align:right; font-size:11px; color:#007a87;'>%.1f%%</td></tr>", subtipo_con_ranking, format(n, big.mark = "."), pct_general)) %>% 
      pull(fila) %>% paste(collapse = "")
    
    html_tabla_flotante <- sprintf("<div style='background: rgba(30, 41, 59, 0.92); padding: 10px; border-radius: 8px; border: 1px solid #475569; max-height: 240px; width: 300px; overflow-y: auto; color: #f8fafc;'><h5 style='margin:0 0 6px 0; color:#007a87;'>Promedio General Ciudad</h5><table style='width:100%%;'>%s</table></div>", filas_tabla_general)
    
    mapa_unido <- capa_laplata %>% 
      left_join(popups_subtipo_html, by = c("barrio_normalizado" = "delegacion")) %>% 
      mutate(total_reclamos = ifelse(is.na(total_reclamos), 0, total_reclamos), html_final = ifelse(is.na(html_final), sprintf("<div style='color:#fff;'><strong>%s</strong><br>Sin datos.</div>", Name), html_final))
    
    list(mapa_data = mapa_unido, html_tabla_flotante = html_tabla_flotante)
  })
  
  output$mapa_interactivo <- renderLeaflet({
    leaflet() %>%
      addProviderTiles(providers$CartoDB.DarkMatter, group = "Oscuro (Default)") %>% 
      addProviderTiles(providers$CartoDB.Positron, group = "Claro / Simple") %>% 
      addProviderTiles(providers$Esri.WorldImagery, group = "Satélite") %>% 
      addProviderTiles(providers$OpenStreetMap.Mapnik, group = "Calles (OSM)") %>% 
      setView(lng = -57.9545, lat = -34.9214, zoom = 12)
  })
  
  observe({
    res <- datos_procesados()
    mapa_data <- res$mapa_data
    html_tabla_flotante <- res$html_tabla_flotante
    puntos <- puntos_reclamos_sf()
    paleta <- colorNumeric(palette = "YlOrRd", domain = mapa_data$total_reclamos)
    
    proxy <- leafletProxy("mapa_interactivo") %>%
      clearGroup("barrio_destacado") %>% 
      clearShapes() %>% clearMarkers() %>% clearMarkerClusters() %>% clearControls()
    
    proxy %>% 
      addPolygons(
        data = mapa_data, layerId = ~Name, group = "Delegaciones / Barrios",
        fillColor = ~paleta(total_reclamos), 
        fillOpacity = 0.2, # Reducido a 0.2 para dar ese efecto traslúcido de fondo
        color = "#475569", 
        weight = 1.2, 
        dashArray = "3",
        highlightOptions = highlightOptions(weight = 3, color = "#38bdf8", fillOpacity = 0.5, bringToFront = TRUE),
        label = ~paste0("Delegación: ", Name, " | Reclamos: ", format(total_reclamos, big.mark = ".")),
        popup = ~html_final
      ) %>% 
      addLegend(pal = paleta, values = mapa_data$total_reclamos, opacity = 0.8, title = "Cant. Reclamos", position = "bottomright") %>% 
      addControl(html = html_tabla_flotante, position = "topright", className = "info legend")
    
    if (nrow(puntos) > 0) {
      proxy %>% 
        addCircleMarkers(data = puntos, group = "Puntos de Reclamo", radius = 4, color = "#38bdf8", stroke = FALSE, fillOpacity = 0.7, clusterOptions = markerClusterOptions(), popup = ~paste0("<strong>Subtipo: </strong>", `SUBTIPO | CARATULA`, "<br><strong>Delegación: </strong>", DELEGACION)) %>% 
        addHeatmap(data = puntos, group = "Mapa de Calor", lng = ~lng, lat = ~lat, blur = 12, max = 0.35, radius = 8, minOpacity = 0.3)
    }
    
    proxy %>% 
      addLayersControl(
        baseGroups = c("Oscuro (Default)", "Claro / Simple", "Satélite", "Calles (OSM)"),
        overlayGroups = c("Delegaciones / Barrios", "Puntos de Reclamo", "Mapa de Calor"),
        options = layersControlOptions(collapsed = TRUE), position = "bottomleft"
      ) %>% 
      hideGroup(c("Puntos de Reclamo", "Mapa de Calor"))
  })
  
  # ----------------------------------------------------------------------------
  # RESALTAR DELEGACIÓN EN AZUL SEGÚN EL FILTRO DE SELECCIÓN
  # ----------------------------------------------------------------------------
  observeEvent(input$filtro_delegacion, {
    proxy <- leafletProxy("mapa_interactivo", session)
    proxy %>% clearGroup("barrio_destacado")
    
    if (!is.null(input$filtro_delegacion) && input$filtro_delegacion != "Todos") {
      barrio_sel <- capa_laplata %>% 
        filter(barrio_normalizado == str_trim(toupper(input$filtro_delegacion)))
      
      if (nrow(barrio_sel) > 0) {
        proxy %>% addPolygons(
          data = barrio_sel, 
          group = "barrio_destacado", 
          fillColor = "#0284c7",   # Azul principal idéntico al de las barras
          fillOpacity = 0.75,     # Opaco y destacado
          color = "#38bdf8",       # Borde celeste brillante de acento
          weight = 3, 
          opacity = 1, 
          options = pathOptions(pane = "markerPane")
        )
      }
    }
  }, ignoreInit = TRUE)
  
  # INTERACCIONES Y SELECCIÓN
  capas_visibles <- reactiveValues(poligonos = TRUE, puntos = FALSE, calor = FALSE)
  
  observeEvent(input$btn_capa_poligonos, {
    capas_visibles$poligonos <- !capas_visibles$poligonos
    if (capas_visibles$poligonos) leafletProxy("mapa_interactivo") %>% showGroup("Delegaciones / Barrios")
    else leafletProxy("mapa_interactivo") %>% hideGroup("Delegaciones / Barrios")
  })
  
  observeEvent(input$btn_capa_puntos, {
    capas_visibles$puntos <- !capas_visibles$puntos
    if (capas_visibles$puntos) leafletProxy("mapa_interactivo") %>% showGroup("Puntos de Reclamo")
    else leafletProxy("mapa_interactivo") %>% hideGroup("Puntos de Reclamo")
  })
  
  observeEvent(input$btn_capa_calor, {
    capas_visibles$calor <- !capas_visibles$calor
    if (capas_visibles$calor) leafletProxy("mapa_interactivo") %>% showGroup("Mapa de Calor")
    else leafletProxy("mapa_interactivo") %>% hideGroup("Mapa de Calor")
  })
  
  observeEvent(input$btn_centrar_mapa, {
    leafletProxy("mapa_interactivo") %>% setView(lng = -57.9545, lat = -34.9214, zoom = 12)
  })
  
  observeEvent(input$mapa_interactivo_shape_click, {
    click <- input$mapa_interactivo_shape_click
    if (is.null(click$id)) return()
    mapa_data <- datos_procesados()$mapa_data
    barrio_seleccionado <- mapa_data %>% filter(Name == click$id)
    leafletProxy("mapa_interactivo", session) %>%
      clearGroup("barrio_destacado") %>%
      addPolygons(data = barrio_seleccionado, group = "barrio_destacado", fillColor = "#0284c7", fillOpacity = 0.75, color = "#38bdf8", weight = 3, opacity = 1, options = pathOptions(pane = "markerPane"))
  })
  
  observeEvent(input$mapa_interactivo_click, {
    leafletProxy("mapa_interactivo", session) %>% clearGroup("barrio_destacado") %>% clearPopups()
  })
  
  observeEvent(list(input$filtro_area, input$filtro_subtipo), {
    if (input$filtro_delegacion == "Todos") {
      leafletProxy("mapa_interactivo", session) %>% clearGroup("barrio_destacado")
    }
  }, ignoreInit = TRUE)
}







library(shiny)
library(bslib)
library(leaflet)
library(plotly)

ui <- page_navbar(
  theme = bs_theme(
    version = 5,
    bg = "#0f171e",         # Fondo oscuro institucional
    fg = "#ffffff",         # Texto blanco
    primary = "#007380",    # Verde/Azul Institucional (Petrol)
    secondary = "#38bdf8",  # Azul claro acento
    base_font = font_google("Inter")
  ),
  
  header = tags$head(
    tags$link(rel = "stylesheet", href = "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css"),
    tags$style(HTML("
      /* Sidebar de Gráfico (Derecha) */
      .sidebar-derecha {
        position: fixed;
        top: 55px;
        right: 0;
        width: 360px;
        height: calc(100vh - 55px);
        background-color: #16202b;
        z-index: 1050;
        padding: 20px 15px;
        box-shadow: -4px 0 15px rgba(0,0,0,0.5);
        transition: transform 0.3s ease-in-out;
        color: white;
        overflow-y: auto;
        border-left: 1px solid #2d3748;
      }
      .sidebar-derecha.colapsada {
        transform: translateX(360px);
      }
      .btn-toggle-right {
        position: fixed;
        top: 70px;
        right: 370px;
        z-index: 1051;
        background-color: #1e293b;
        color: #007380;
        border: 1px solid #475569;
        border-radius: 6px;
        width: 38px;
        height: 38px;
        cursor: pointer;
        transition: right 0.3s ease-in-out, background-color 0.2s;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      .btn-toggle-right.colapsado {
        right: 15px;
      }
      .btn-toggle-right:hover {
        background-color: #334155;
        color: #38bdf8;
      }
    ")),
    tags$script(HTML("
      $(document).on('click', '#toggle_right', function() {
        $('.sidebar-derecha').toggleClass('colapsada');
        $('#toggle_right').toggleClass('colapsado');
        $('#icon_right').toggleClass('fa-chevron-right fa-chart-bar');
      });

      $(document).on('click', '#btn_ir_mapa', function() {
        $('a[data-value=\"Mapa Interactivo\"]').tab('show');
      });
    "))
  ),
  
  title = div(
    style = "display: flex; align-items: center; gap: 12px;",
    img(src = "logo_laplata.png", height = "35px", style = "object-fit: contain;"),
    span(style = "font-weight: 700; font-size: 16px; color: #ffffff;", "INFORME DE BARRIOS INTERACTIVO")
  ),
  id = "nav_main",
  fillable = TRUE,
  
  # PESTAÑA 1: PRESENTACIÓN
  nav_panel(
    title = "Presentación",
    icon = icon("house"),
    
    div(
      style = "padding: 30px; max-width: 1200px; margin: 0 auto;",
      
      div(
        style = "background: linear-gradient(135deg, #007380 0%, #004d56 100%); 
                 padding: 40px; border-radius: 12px; margin-bottom: 30px; 
                 box-shadow: 0 10px 25px rgba(0,0,0,0.4); text-align: center;",
        
        img(src = "logo_laplata.png", height = "80px", style = "margin-bottom: 20px; max-width: 100%; object-fit: contain;"),
        
        h1(style = "color: #ffffff; font-weight: 800; font-size: 28px; margin-bottom: 15px; letter-spacing: -0.5px;", 
           "Sistema de Monitorización Urbana y Reclamos"),
        
        p(style = "font-size: 16px; color: #e2e8f0; max-width: 800px; margin: 0 auto 25px auto; line-height: 1.6;",
          "Bienvenido a la plataforma geográfica interactiva de la Ciudad de La Plata. ",
          "Este portal permite analizar la distribución territorial de los reclamos urbanos, identificar patrones anómalos por delegación y evaluar la carga operativa asignada a cada área."
        ),
        
        actionButton("btn_ir_mapa", " Explorar Mapa Interactivo", 
                     style = "background-color: #ffffff; color: #007380; font-weight: 700; border: none; padding: 12px 28px; font-size: 16px; border-radius: 8px; cursor: pointer;", 
                     icon = icon("map-location-dot"))
      ),
      
      layout_column_wrap(
        width = 1/3,
        style = "margin-bottom: 30px;",
        
        value_box(
          title = "Cobertura Territorial",
          value = "La Plata",
          showcase = icon("city", style = "color: #38bdf8;"),
          style = "background-color: #16202b; border: 1px solid #007380;",
          p("Análisis a nivel delegación y barrios")
        ),
        value_box(
          title = "Gestión Operativa",
          value = "Filtros en Vivo",
          showcase = icon("filter", style = "color: #38bdf8;"),
          style = "background-color: #16202b; border: 1px solid #007380;",
          p("Segmentación por Delegación, Área y Subtipo")
        ),
        value_box(
          title = "Detección de Anomalías",
          value = "Top 15",
          showcase = icon("chart-line", style = "color: #38bdf8;"),
          style = "background-color: #16202b; border: 1px solid #007380;",
          p("Desviaciones locales vs. Promedio General")
        )
      ),
      
      card(
        style = "background-color: #16202b; border: 1px solid #2d3748;",
        card_header(
          style = "background-color: #007380; color: #ffffff; font-weight: 700;", 
          " Guía Rápida de Exploración"
        ),
        card_body(
          layout_column_wrap(
            width = 1/2,
            div(
              h5(style = "color: #38bdf8; font-weight: 600;", "1. Mapa Geográfico"),
              p(style = "color: #9ca3af; font-size: 14px;", "Selecciona delegaciones en el mapa para desplegar su ficha de desviaciones respecto al promedio de la ciudad.")
            ),
            div(
              h5(style = "color: #38bdf8; font-weight: 600;", "2. Panel de Filtros y Gráficos"),
              p(style = "color: #9ca3af; font-size: 14px;", "Usa la barra lateral izquierda para refinar datos y el botón flotante derecho para desplegar la distribución por área operativa.")
            )
          )
        )
      )
    )
  ),
  
  # PESTAÑA 2: MAPA INTERACTIVO
  nav_panel(
    title = "Mapa Interactivo",
    icon = icon("map"),
    
    div(
      style = "position: relative; width: 100%; height: calc(100vh - 55px); overflow: hidden;",
      
      tags$button(
        id = "toggle_right", 
        class = "btn-toggle-right", 
        title = "Desplegar / Ocultar gráfico por área",
        tags$i(id = "icon_right", class = "fa-solid fa-chevron-right")
      ),
      
      div(
        class = "sidebar-derecha",
        h3(style = "margin-top:0; color:#38bdf8; font-size:16px; font-weight:bold; border-bottom:1px solid #334155; padding-bottom:8px;", "Análisis por Área"),
        p(style = "font-size:11px; color:#94a3b8; margin-bottom:15px;", "Distribución de reclamos registrados según el Área Operativa Asignada."),
        plotlyOutput("grafico_area_operativa", height = "75vh")
      ),
      
      page_sidebar(
        fillable = TRUE,
        padding = 0,
        
        sidebar = sidebar(
          title = "Filtros y Control",
          width = 300,
          bg = "#16202b",
          
          # REEMPLAZO: Filtro por Delegación
          selectInput(
            inputId = "filtro_delegacion", 
            label = "Delegación / Barrio", 
            choices = c("Todos"), 
            selected = "Todos"
          ),
          
          selectInput(
            inputId = "filtro_area", 
            label = "Área Asignada", 
            choices = c("Todos"), 
            selected = "Todos"
          ),
          
          selectInput(
            inputId = "filtro_subtipo", 
            label = "Subtipo / Carátula", 
            choices = c("Todos"), 
            selected = "Todos"
          ),
          
          hr(style = "border-top: 1px solid #2d3748; margin: 15px 0;"),
          
          p(style = "font-size: 12px; color: #9ca3af;",
            "Usa la tabla flotante superior derecha en el mapa para ver el ranking general de la ciudad."),
          p(style = "font-size: 12px; color: #9ca3af;",
            "Al hacer clic sobre cualquier delegación, se desplegará el reporte detallado con sus 15 principales desviaciones locales.")
        ),
        
        card(
          full_screen = TRUE,
          card_header(style = "color: #007a87; font-weight: bold;", "Distribución Espacial y Análisis de Anomalías de Reclamos"),
          leafletOutput("mapa_interactivo", height = "100%")
        )
      )
    )
  )
)
