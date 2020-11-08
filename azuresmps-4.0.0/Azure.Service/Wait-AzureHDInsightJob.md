---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015832"
---
# Wait-AzureHDInsightJob

## Áttekintés
Megvárja a HDInsight-feladatok befejezését vagy kudarcát, és megjeleníti a feladat előrehaladását.

## SZINTAXISA

### HDInsight-fürtök jobDetails-előzményeinek beszerzése (alapértelmezett)
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### HDInsight-fürtök jobDetails-előzményeinek beszerzése (adott előfizetési hitelesítő adatokkal)
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Várjon egy feladatot a JobId egy HDInsight-fürtjén
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Munka várakozása egy HDInsight-fürtön
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **WAIT-AzureHDInsightJob** parancsmag várja az Azure HDInsight-feladatok befejezését vagy kudarcát, és megjeleníti a feladat előrehaladását.

## Példák

### Példa 1: feladat futtatása és várakozás a befejezésre
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

Az első parancs a jelenlegi Azure-előfizetési azonosítót kapja, majd a $SubId változóban tárolja.

A második parancs a megadott fürtöt kapja, majd a $ClusterName változóban tárolja.

A harmadik parancs a **New-AzureHDInsightMapReduceJobDefinition** parancsmagot használja MapReduce-feladatdefiníció létrehozásához, majd a $WordCountJob változóban tárolja.

A negyedik parancs több parancsmagot használ a sorozatokban: 

- A munkafolyamatot a pipeline operátor segítségével átadja $WordCountJob a **Start-AzureHDInsightJob** parancsmagnak a feladat megkezdéséhez. 
- A feladatot átadják a **WAIT-AzureHDInsightJob** parancsmagnak, és a feladat befejezéséhez 3600 másodpercre kell várni. 
- Ha befejezte a feladatot, a parancs a **Get-AzureHDInsightJobOutput** parancsmagot használja a projekt kimenetének beszerzéséhez.

## PARAMÉTEREK

### -Tanúsítvány
Az Azure-előfizetés kezelési tanúsítványát adja meg.

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cluster
Egy fürtöt ad meg.
Ezzel a parancsmaggal egy olyan feladat vár, amelyet a megadott paraméter határoz meg a fürtben.

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Hitelesítő adatok
Megadja a fürtök közvetlen HTTP-eléréséhez használt hitelesítő adatokat.
Ezt a paramétert az *előfizetés* paraméter helyett úgy is megadhatja, hogy hitelesítse a hozzáférést egy fürthöz.

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

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
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Egy HDInsight-szolgáltatás névterét adja meg.
Ha nem adja meg ezt a paramétert, a program az alapértelmezett névteret használja.

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
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
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Egy Azure HDInsight-feladatot ad meg.

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre várni szeretne.

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

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

### -Előfizetés
Az előfizetést adja meg.
Ezzel a parancsmaggal megvárja az előfizetéshez tartozó munkát, amelyet a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitTimeoutInSeconds
A várakozási művelethez a másodpercben megadott időtúllépést adja meg.
Ha az időtúllépés lejár a feladat befejezésekor, a parancsmag megszűnik.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureHDInsightJob](./Get-AzureHDInsightJob.md)

[Get-AzureHDInsightJobOutput](./Get-AzureHDInsightJobOutput.md)

[Start-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Stop-AzureHDInsightJob](./Stop-AzureHDInsightJob.md)


