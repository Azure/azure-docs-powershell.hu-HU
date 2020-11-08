---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015640"
---
# Get-AzureHDInsightJobOutput

## Áttekintés
A napló kimenetének lekérdezése a projekthez.

## SZINTAXISA

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a Linux-alapú fürtök létrehozása az [Azure PowerShell használatával HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)című témakört.
Ha többet szeretne tudni arról, hogy miként küldhet feladatokat az Azure PowerShell és más megközelítések segítségével, olvassa el [az Hadoop-feladatok elküldése az HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight-parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx)című témakörben talál.

A **Get-AzureHDInsightJobOutput** parancsmag a fürthöz társított tárolási fiókból kapja meg a napló kimenetét.
Különböző típusú beosztásokat kaphat, például a normál kimenetet, a normál hibát, a tevékenység naplókat és a naplók összegzését.

## Példák

### Példa 1: projekt kimenetének beszerzése
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

Az első parancs megkapja a jelenlegi előfizetés AZONOSÍTÓját, majd a $SubId változóban tárolja.

A második parancs a MyCluster nevet a $Clustername változóban tárolja.

A harmadik parancs létrehoz egy MapReduce, majd a $WordCountJob változóban tárolja.
A parancs átadja a feladatot $WordCountJob a **Start-AzureHDInsightJob** parancsmaggal a feladat indításához.
A **várakozás-AzureHDInsightJob** parancsmagot is átadja $WordCountJob a feladat befejezéséhez, majd a **Get-AzureHDInsightJobOutput** a projekt kimenetének beszerzéséhez használja.

## PARAMÉTEREK

### -Tanúsítvány
Az Azure-előfizetés kezelési tanúsítványát adja meg.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cluster
Egy fürtöt ad meg.
Ez a parancsmag olyan munkanaplókat kap a fürttől, amelyeket ez a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DownloadTaskLogs
Azt jelzi, hogy ez a parancsmag a feladat naplóit kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Végpont
Az Azure-hoz való csatlakozáshoz használandó végpontot adja meg.
Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett végpontot használja.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Az HDInsight szolgáltatás névterét adja meg, ha nem szeretné használni az alapértelmezett névteret.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Azt jelzi, hogy a program figyelmen kívül hagyja-e a biztonságos szoftvercsatorna-réteg (SSL) hibáit.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
A beolvasott feladat AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -StandardError
Azt jelzi, hogy ez a parancsmag a projekt StdErr kimenetét kapja.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardOutput
Azt jelzi, hogy ez a parancsmag a projekt SdtOut kimenetét kapja.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Előfizetés
A HDInsight-fürtöt tartalmazó előfizetést adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskLogsDirectory
Itt adhatja meg, hogy melyik helyi mappa tárolja a feladatok naplóit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSummary
Azt jelzi, hogy ez a parancsmag a műveletnapló összegzését kapja.

```yaml
Type: SwitchParameter
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

[Új – AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[Start-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Várjon-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)
