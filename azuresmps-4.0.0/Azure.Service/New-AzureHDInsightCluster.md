---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015923"
---
# New-AzureHDInsightCluster

## Áttekintés
HDInsight-fürtöt hoz létre.

## SZINTAXISA

### Cluster by config (adott előfizetési hitelesítő adatokkal) (alapértelmezett)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Fürt név szerint (adott előfizetési hitelesítő adatokkal)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **New-AzureHDInsightCluster** parancsmag az Azure HDInsight-fürtöt a megadott paraméterekkel vagy a **New-AzureHDInsightClusterConfig** parancsmaggal létrehozott konfigurációs objektum használatával hozza létre.

## Példák

### Példa 1: HDInsight-fürt létrehozása
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

Ez a példa létrehoz egy HDInsight-fürtöt az aktuális előfizetéshez.

Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.

A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.

A negyedik, az ötödik és a hatodik parancs a **Get-hitelesítőadat** parancsmagot használja az aktuális előfizetéshez tartozó hitelesítő adatok beszerzéséhez, valamint a Oozie és a kaptárhoz, majd a hitelesítő adatok tárolása a változókban.

A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:

- **Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása.
- **Set-AzureHDInsightDefaultStorage** : beállíthatja a konfiguráció alapértelmezett tárolási fiókját a MyBlobStorage.blob.Core.Windows.net értékre.
- **Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók felvétele a konfigurációba.
- **Add-AzureHDInsightMetastore** : adjon hozzá egy Metastore a Oozie-hoz, és egy Metastore a kaptár számára a konfigurációhoz.
- **Új – AzureHDInsightCluster** : hozzon létre egy HDInsight-fürtöt az új konfigurációval.

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

### -ClusterSizeInNodes
A fürtökhöz létrehozandó adatcsomópontok számát adja meg.

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
A létrehozandó fürt típusát adja meg.

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
A **New-AzureHDInsightClusterConfig** parancsmaggal létrehozott konfigurációs objektumot adja meg.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Hitelesítő adatok
A Hadoop-fürtök távolról való eléréséhez használt alapértelmezett fiókhoz használt HDInsight felhasználói hitelesítő adatait adja meg.
Ezek a hitelesítő adatok eltérnek a felhasználó előfizetési hitelesítő adataitól.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataNodeVMSize
Az adatcsomópont virtuális számítógépének méretét adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
A HDInsight-fürtöt használó alapértelmezett tárterület-fiókhoz tartozó fiók kulcsát adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
A HDInsight-fürtöt használó alapértelmezett tárterület-fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageContainerName
Annak az alapértelmezett tárolónak a nevét adja meg az alapértelmezett Azure Storage-fiókban, amelyet egy HDInsight-fürt használ.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
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

### -HeadNodeVMSize
A fej csomópont virtuális számítógépének méretét adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Egy HDInsight-szolgáltatás névterét adja meg.
Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett névteret használja.

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

### -Hely
Azt a régiót adja meg, amelybe HDInsight-fürtöt szeretne létrehozni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A létrehozandó Azure HDInsight-fürt nevét adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
A fürt operációs rendszerét adja meg.

```yaml
Type: OSType
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

### -RdpAccessExpiry
Itt adhatja meg a fürthöz az RDP-hozzáféréssel való hozzáférés időpontját **datetime** -objektumként.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RdpCredential
A fürtök RDP-elérésének hitelesítő adatait adja meg.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshCredential
A HDInsight-fürt biztonságos rendszerhéj-(SSH) felhasználónevét és jelszavát adja meg.
Ez a paraméter csak Linux-fürtök esetén érvényes.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshPublicKey
A HDInsight-fürtök SSH-beli nyilvános kulcsát adja meg.
Ez a paraméter csak Linux-fürtök esetén érvényes.

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

### -SubnetName
Az alhálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Előfizetés
Azt az Azure-előfizetést adja meg, amelyben HDInsight-fürtöt hozhat létre.

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

### -Verzió
A létrehozandó HDInsight-fürt verziószámát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkId
Annak a virtuális hálózatnak az AZONOSÍTÓját adja meg, amelybe a fürtöt létre szeretné hozni.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZookeeperNodeVMSize
A ZooKeeper csomópont virtuális számítógépének méretét adja meg.
Ez a paraméter csak HBase-vagy Storm-fürtök esetén érvényes.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
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

[Add-AzureHDInsightMetastore](./Add-AzureHDInsightMetastore.md)

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[Get-AzureHDInsightCluster](./Get-AzureHDInsightCluster.md)

[Új – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Remove-AzureHDInsightCluster](./Remove-AzureHDInsightCluster.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)

[Use-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


