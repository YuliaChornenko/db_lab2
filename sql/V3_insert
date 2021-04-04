INSERT INTO "Region" ("RegName", "AreaName", "TerName", "TerTypeName")
SELECT DISTINCT REGNAME, AREANAME, TERNAME, TerTypeName
FROM zno_analytics;


INSERT INTO "Region" ("RegName", "AreaName", "TerName")
SELECT DISTINCT EORegName, EOAreaName, EOTerName
FROM zno_analytics
WHERE EORegName IS NOT NULL AND EOAreaName IS NOT NULL AND EOTerName IS NOT NULL
EXCEPT
SELECT "RegName", "AreaName", "TerName"
FROM "Region";

/* Educational objectives populate */

INSERT INTO "EO" ("EOName", "EOTypeName", "EOParent", "RegionID", "ClassLang")
SELECT DISTINCT on (zno_analytics.EONAME) zno_analytics.EONAME, zno_analytics.EOTYPENAME, zno_analytics.EOParent, "Region"."RegionID", zno_analytics.ClassLangName
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.EORegName = "Region"."RegName" AND zno_analytics.AreaName = "Region"."AreaName" AND zno_analytics.EOTerName = "Region"."TerName"
WHERE zno_analytics.EONAME IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.UkrPTName) zno_analytics.UkrPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.UkrPTRegName = "Region"."RegName" AND zno_analytics.UkrPTAreaName = "Region"."AreaName" AND zno_analytics.UkrPTTerName = "Region"."TerName"
WHERE zno_analytics.UkrPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.UkrPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.histPTName) zno_analytics.histPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.histPTRegName = "Region"."RegName" AND zno_analytics.histPTAreaName = "Region"."AreaName" AND zno_analytics.histPTTerName = "Region"."TerName"
WHERE zno_analytics.histPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.histPTName IS NOT NULL;

INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.mathPTName) zno_analytics.mathPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.mathPTRegName = "Region"."RegName" AND zno_analytics.mathPTAreaName = "Region"."AreaName" AND zno_analytics.mathPTTerName = "Region"."TerName"
WHERE zno_analytics.mathPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.mathPTName IS NOT NULL;

INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.histPTName) zno_analytics.physPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.physPTRegName = "Region"."RegName" AND zno_analytics.physPTAreaName = "Region"."AreaName" AND zno_analytics.physPTTerName = "Region"."TerName"
WHERE zno_analytics.physPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.physPTName IS NOT NULL;

INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.chemPTName) zno_analytics.chemPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.chemPTRegName = "Region"."RegName" AND zno_analytics.chemPTAreaName = "Region"."AreaName" AND zno_analytics.chemPTTerName = "Region"."TerName"
WHERE zno_analytics.chemPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.chemPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.bioPTName) zno_analytics.bioPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.bioPTRegName = "Region"."RegName" AND zno_analytics.bioPTAreaName = "Region"."AreaName" AND zno_analytics.bioPTTerName = "Region"."TerName"
WHERE zno_analytics.bioPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.bioPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.geoPTName) zno_analytics.geoPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.geoPTRegName = "Region"."RegName" AND zno_analytics.geoPTAreaName = "Region"."AreaName" AND zno_analytics.geoPTTerName = "Region"."TerName"
WHERE zno_analytics.geoPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.geoPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.engPTName) zno_analytics.engPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.engPTRegName = "Region"."RegName" AND zno_analytics.engPTAreaName = "Region"."AreaName" AND zno_analytics.engPTTerName = "Region"."TerName"
WHERE zno_analytics.engPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.engPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.engPTName) zno_analytics.fraPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.fraPTRegName = "Region"."RegName" AND zno_analytics.fraPTAreaName = "Region"."AreaName" AND zno_analytics.fraPTTerName = "Region"."TerName"
WHERE zno_analytics.fraPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.fraPTName IS NOT NULL;

INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.deuPTName) zno_analytics.deuPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.deuPTRegName = "Region"."RegName" AND zno_analytics.deuPTAreaName = "Region"."AreaName" AND zno_analytics.deuPTTerName = "Region"."TerName"
WHERE zno_analytics.deuPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.deuPTName IS NOT NULL;


INSERT INTO "EO" ("EOName", "RegionID")
SELECT DISTINCT ON (zno_analytics.spaPTName) zno_analytics.spaPTName, "Region"."RegionID"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.spaPTRegName = "Region"."RegName" AND zno_analytics.spaPTAreaName = "Region"."AreaName" AND zno_analytics.spaPTTerName = "Region"."TerName"
WHERE zno_analytics.spaPTName NOT IN (
SELECT "EOName"
FROM "EO"
) AND zno_analytics.spaPTName IS NOT NULL;




/* Person populate */

INSERT INTO "Student" ("OUTID", "Birth", "SexName", "RegionID", "RegTypeName", "ClassProfileName", "EOName")
SELECT zno_analytics.OUTID, zno_analytics.Birth, zno_analytics.SEXTYPENAME, "Region"."RegionID", zno_analytics.REGTYPENAME, zno_analytics.ClassProfileNAME, "EO"."EOName"
FROM zno_analytics
LEFT JOIN "Region"
ON zno_analytics.REGNAME = "Region"."RegName" AND zno_analytics.AREANAME = "Region"."AreaName" AND zno_analytics.TERNAME = "Region"."TerName"
LEFT JOIN "EO"
ON zno_analytics.EONAME = "EO"."EOName";



/* Test populate */

INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "AdaptScale", "PTEOName")
SELECT outID, UkrTest, year, UkrTestStatus, UkrBall100, UkrBall12, UkrBall, UkrAdaptScale, UkrPTName
FROM zno_analytics
WHERE zno_analytics.UkrTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, histTest, year, histTestStatus, histBall100, histBall12, histBall, histPTName, histLang
FROM zno_analytics
WHERE zno_analytics.histTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, mathTest, year, mathTestStatus, mathBall100, mathBall12, mathBall, mathPTName, mathLang
FROM zno_analytics
WHERE zno_analytics.mathTest IS NOT NULL;


INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, physTest, year, physTestStatus, physBall100, physBall12, physBall, physPTName, physLang
FROM zno_analytics
WHERE zno_analytics.physTest IS NOT NULL;


INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, chemTest, year, chemTestStatus, chemBall100, chemBall12, chemBall, chemPTName, chemLang
FROM zno_analytics
WHERE zno_analytics.chemTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, bioTest, year, bioTestStatus, bioBall100, bioBall12, bioBall, bioPTName, bioLang
FROM zno_analytics
WHERE zno_analytics.bioTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName", "Lang")
SELECT outID, geoTest, year, geoTestStatus, geoBall100, geoBall12, geoBall, geoPTName, geoLang
FROM zno_analytics
WHERE zno_analytics.geoTest IS NOT NULL;


INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName")
SELECT outID, engTest, year, engTestStatus, engBall100, engBall12, engBall, engPTName
FROM zno_analytics
WHERE zno_analytics.engTest IS NOT NULL;


INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName")
SELECT outID, fraTest, year, fraTestStatus, fraBall100, fraBall12, fraBall, fraPTName
FROM zno_analytics
WHERE zno_analytics.fraTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName")
SELECT outID, deuTest, year, deuTestStatus, deuBall100, deuBall12, deuBall, deuPTName
FROM zno_analytics
WHERE zno_analytics.deuTest IS NOT NULL;



INSERT INTO "Test" ("OUTID", "TestName", "Year", "TestStatus", "Ball100", "Ball12", "Ball", "PTEOName")
SELECT outID, spaTest, year, spaTestStatus, spaBall100, spaBall12, spaBall, spaPTName
FROM zno_analytics
WHERE zno_analytics.spaTest IS NOT NULL;
