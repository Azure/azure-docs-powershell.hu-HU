---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015916"
---
# New-AzureHDInsightMapReduceJobDefinition

## Áttekintés
Új MapReduce-feladatot határoz meg.

## SZINTAXISA

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **New-AzureHDInsightMapReduceJobDefinition** parancsmag új MapReduce-feladatot határoz meg az Azure HDInsight-fürtökön való futtatáshoz.

## Példák

### 1. példa: MapReduce-feladat meghatározása, a feladat futtatása és a kimenet beszerzése
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

Az első parancs megkapja a jelenlegi előfizetés AZONOSÍTÓját, majd a $SubId változóban tárolja.

A második parancs a MyCluster nevet a $Clustername változóhoz rendeli.

A harmadik parancs a **New-AzureHDInsightMapReduceJobDefinition** parancsmagot használja MapReduce-feladatdefiníció létrehozásához, majd a $WordCountJob változóban való tárolásához.

A negyedik parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát: 

- **Indítsa** el a AzureHDInsightJob, és indítsa el a feladatot $ClusterName. 
- **Várjon – AzureHDInsightJob** , amíg meg nem várja a feladatot, és meg kell jelenítenie a Befejezés felé irányuló előrehaladást.
- **Get-AzureHDInsightJobOutput** a projekt kimenetének beszerzéséhez.

## PARAMÉTEREK

### -Argumentumok
Argumentumokat ad meg egy Hadoop-feladathoz.
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

### -Osztálynév
A Java Archive (JAR) fájlban lévő Job osztály nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Határozza meg
Itt adhatja meg a Hadoop konfigurációs értékeit a feladat futásakor.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Files
A projekthez szükséges WASB-fájlok tömbjét adja meg.

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

### -JarFile
Annak a JAR-fájlnak a teljesen minősített nevét adja meg, amely egy MapReduce-feladat kódját és függőségeit tartalmazza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Feladatnév
Egy MapReduce-feladat nevét adja meg.
Ez a paraméter nem kötelező.
Ha nem adja meg ezt a paramétert, a program az *Osztálynév* paraméter értékét használja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LibJars
A projekt LibJar hivatkozásait adja meg.

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

[Get-AzureHDInsightJobOutput](./Get-AzureHDInsightJobOutput.md)

[Új – AzureHDInsightHiveJobDefinition](./New-AzureHDInsightHiveJobDefinition.md)

[Új – AzureHDInsightPigJobDefinition](./New-AzureHDInsightPigJobDefinition.md)

[Új – AzureHDInsightSqoopJobDefinition](./New-AzureHDInsightSqoopJobDefinition.md)

[Start-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Várjon-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)


