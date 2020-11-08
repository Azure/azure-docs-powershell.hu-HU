---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016010"
---
# New-AzureHDInsightPigJobDefinition

## Áttekintés
Új Pig-feladatot határoz meg egy HDInsight szolgáltatáshoz.

## SZINTAXISA

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **New-AzureHDInsightPigJobDefinition** definiál egy disznó-feladatot az Azure HDInsight szolgáltatáshoz.

## Példák

### Példa 1: új Pig-feladat definiálása
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

Az első parancs a karakterlánc értékét deklarálja, majd a $0 változóban tárolja őket.

A második parancs létrehoz egy disznó-feladatot, majd a $QueryString változóban tárolja.

A végleges parancs létrehoz egy olyan disznó-munkadefiníciót, amely a lekérdezést használja a $QueryString-ban, majd a $PigJobDefinition változóban tárolja a feladatdefiníció értékét.

## PARAMÉTEREK

### -Argumentumok
Argumentumok tömbjét adja meg a sertések feladatához.
Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fájl
A futtatandó lekérdezést tartalmazó fájl elérési útvonalát adja meg.
Ezt a paramétert a *query* paraméter helyett használhatja.

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
A disznó-feladathoz társított fájlok gyűjteményét adja meg.

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

### -Query
Egy Pig-Job lekérdezést ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

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

[Új – AzureHDInsightSqoopJobDefinition](./New-AzureHDInsightSqoopJobDefinition.md)

[Új – AzureHDInsightStreamingMapReduceJobDefinition](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


