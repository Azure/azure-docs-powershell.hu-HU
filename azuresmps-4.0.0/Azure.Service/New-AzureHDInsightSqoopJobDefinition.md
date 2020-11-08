---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015915"
---
# New-AzureHDInsightSqoopJobDefinition

## Áttekintés
Új Sqoop-feladatot határoz meg.

## SZINTAXISA

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **New-AzureHDInsightSqoopJobDefinition** parancsmag létrehoz egy Sqoop feladatot az Azure HDInsight-fürtökön való futtatáshoz.

A Sqoop egy eszköz, amellyel átviheti az adatátvitelt a Hadoop-fürtök és a relációs adatbázisok között.
Az Sqoop segítségével az SQL Server-adatbázisokból származó adatok importálhatók Hadoop-es elosztott fájlrendszerbe (HDFS), az adatok átalakítása a Hadoop MapReduce, majd az adatok exportálása az HDFS az SQL Server-adatbázisból.

## Példák

### 1. példa: az adatimportálás
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

Ez a parancs olyan Sqoop-feladatot határoz meg, amely egy AzureSQL kiszolgálói adatbázisból egy HDInsight-fürtbe importálja az összes sort, majd a $SqoopJobDef változóban tárolja a feladatdefiníció értékét.

## PARAMÉTEREK

### -Command
A Sqoop parancsot és annak argumentumait adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fájl
A futtatandó parancsokat tartalmazó parancsfájl elérési útvonalát adja meg.
A parancsfájlnak a WASB-on kell lennie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Files
A projekthez szükséges WASB-fájlok gyűjteményét adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusFolder
Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureHDInsightHiveJobDefinition](./New-AzureHDInsightHiveJobDefinition.md)

[Új – AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[Új – AzureHDInsightPigJobDefinition](./New-AzureHDInsightPigJobDefinition.md)

[Új – AzureHDInsightStreamingMapReduceJobDefinition](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


