---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015728"
---
# Add-AzureHDInsightConfigValues

## Áttekintés
A Hadoop konfigurációs érték testreszabása vagy a kaptár megosztott tár testreszabása HDInsight-fürtkonfiguráció beállítással.

## SZINTAXISA

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell használatával HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)című témakört.
Ha többet szeretne tudni arról, hogy miként küldhet feladatokat az Azure PowerShell és más megközelítések segítségével, olvassa el [az Hadoop-feladatok elküldése az HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight-parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx)című témakörben talál.

Az **Add-AzureHDInsightConfigValues** parancsmag Hadoop-konfigurációt (például Core-site.xml vagy Hive-site.xml) ad hozzá, vagy egy, az Azure HDInsight cluster konfigurációjának megfelelő megosztott tár-testreszabást.

A parancsmag egyéni konfigurációs értékeket ad egy megadott konfigurációs objektumhoz.
Az egyéni beállítások hozzáadódnak a megfelelő Hadoop-szolgáltatások konfigurációs fájljaihoz a fürt telepítésekor.

## Példák

### 1. példa: fürt beállítása
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

Az első parancs létrehoz egy új **AzureHDInsightHiveConfiguration** objektumot, majd a $HiveConfigValues változóban tárolja.

A következő öt parancs a kaptár konfigurációs értékeit hozza létre, és az értékeket az $HiveConfigValues tagjaiként tárolja.

A hetedik parancs létrehoz egy **AzureHDInsightOozieConfiguration** objektumot, majd a $OozieConfigValues változóban tárolja.
A nyolcadik parancs létrehoz egy konfigurációs értéket a Oozie-hoz, majd az értékeket az $OozieConfigValues tagjaként tárolja.

A kilencedik parancs létrehoz egy **AzureHDInsightMapReduceConfiguration** objektumot, majd a $MapredConfigValues változóban tárolja.
A következő két parancs konfigurációs értékeket hoz létre a MapReduce, és ezeket az értékeket az $MapredConfigValues tagjaiként tárolja.

A tizenkettedik parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.
A parancs a pipeline operátor segítségével átadja $Config a **set-AzureHDInsightDefaultStorage** parancsmagnak, hogy frissítse az alapértelmezett tárterületet és az **Add-AzureHDInsightConfigValues** parancsmagot, hogy az új konfigurációs értékeket hozzáadja a fürtkonfiguráció beállításához.

A végleges parancs a pipeline operátor segítségével átadja $Configt a **New-AzureHDInsightCluster** parancsmagnak, hogy új HDInsight-fürtöt hozzon létre a testre szabott beállításokkal.

## PARAMÉTEREK

### -Config
Annak a konfigurációs objektumnak a megadása, amelyhez Hadoop-konfigurációt kíván hozzáadni.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Core
A Core-site.xml Hadoop konfigurációs értékeit adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HBase
A Hbase-site.xml HBase konfigurációs értékeit adja meg.

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hdfs
A Hdfs-site.xml Hadoop konfigurációs értékeit adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kaptár
A Hadoop-kaptár szolgáltatás testreszabási objektumát adja meg, többek között a Hive-site.xml és a kaptár megosztott tárakra vonatkozó konfigurációs értékeket is.

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapReduce
A MapReduce és a kapacitás-ütemező testreszabási objektumát adja meg.

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oozie
A Hadoop Oozie szolgáltatás testreszabási objektumát adja meg, többek között az Oozie-site.xml Hadoop konfigurációs értékeit is.

```yaml
Type: AzureHDInsightOozieConfiguration
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

### -Szikra
Az Apache Spark testreszabási objektumát adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storm
Az Apache Storm testreszabási objektumát adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fonal
A Hadoop-fonal testreszabási objektumát adja meg, amely a Yarn-site.xml egyéni fonal-konfigurációjának halmazát adja meg.

```yaml
Type: Hashtable
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

[Új – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Új – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
