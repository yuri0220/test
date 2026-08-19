# test
from qgis.core import QgsDistanceArea, QgsCoordinateReferenceSystem, QgsProject, QgsPointXY

d = QgsDistanceArea()
d.setSourceCrs(
    QgsCoordinateReferenceSystem("EPSG:4326"),
    QgsProject.instance().transformContext()
)
d.setEllipsoid("WGS84")

d.measureLine(
    QgsPointXY(139.753583, 35.913685),
    QgsPointXY(139.753569, 35.912785)
)