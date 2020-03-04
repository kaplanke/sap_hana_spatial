# sap_hana_spatial
SAP HANA Spherical Pseudo-Mercator projection for ESRI Map


SELECT ST_GeomFromWKT('POINT (' || TO_DOUBLE(l."ZLONGITUDE") * (3.141592/180) * 6378137 
			|| ' ' || LN(TAN(TO_DOUBLE(l."ZLATITUDE")  * (3.141592/180)/2 + 3.141592/4)) * 6378137 || ')') FROM DUMMY;
