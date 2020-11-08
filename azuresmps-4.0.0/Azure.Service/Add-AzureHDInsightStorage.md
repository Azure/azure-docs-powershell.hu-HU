---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015716"
---
# Add-AzureHDInsightStorage

## Áttekintés
A blob-tároló-fiók bejegyzését hozzáadja egy HDInsight-konfigurációhoz.

## SZINTAXISA

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Az **Add-AzureHDInsightStorage** parancsmag blob-tárolási fiókot ad hozzá egy Azure HDInsight-konfigurációhoz.

## Példák

### 1. példa: tárterület-fiók hozzáadása
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

Ez a parancs hozzáadja a MyStorage nevű tárolási fiókot a $Config tárolt konfigurációs objektumhoz, majd a $StoreConfig változóban tárolja a konfigurációt.

### 2. példa: több tárolási fiók beállítása
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.

A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.

A negyedik, az ötödik és a hatodik parancs hitelesítő adatokat kap az aktuális előfizetéshez, valamint a Oozie és a Kaptárhoz, majd tárolja a hitelesítő adatokat a változókban.

A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:

- **Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása
- **Set-AzureHDInsightDefaultStorage** : a konfiguráció alapértelmezett tárolási fiókjának beállítása a MyBlobStorage.blob.Core.Windows.net
- **Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók hozzáadása a konfigurációhoz
- **Add-AzureHDInsightStorage** : metastore hozzáadása az Oozie-hoz és a struktúra metastore a konfigurációhoz
- **Új – AzureHDInsightCluster** új HDInsight-fürtöt hozhat létre az új konfigurációval

## PARAMÉTEREK

### -Config
Konfigurációs objektumot ad meg.
Ez a parancsmag a megfelelő tárterület-információkat hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.

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

### -StorageAccountKey
A tárterület-fiók eléréséhez használt tárolási fiók kulcsát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
A hozzáadni kívánt Azure Storage-fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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


