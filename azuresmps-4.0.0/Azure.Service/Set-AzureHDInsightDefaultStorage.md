---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015960"
---
# <span data-ttu-id="a8a71-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="a8a71-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="a8a71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8a71-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a71-103">A HDInsight-fürtök alapértelmezett tárolási fiókját állítja be.</span><span class="sxs-lookup"><span data-stu-id="a8a71-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="a8a71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8a71-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8a71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8a71-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a71-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="a8a71-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="a8a71-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="a8a71-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="a8a71-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="a8a71-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="a8a71-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="a8a71-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="a8a71-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="a8a71-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="a8a71-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a8a71-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="a8a71-112">A **set-AzureHDInsightDefaultStorage** parancsmag az alapértelmezett tárolási fiókot állítja be egy HDInsight-fürtkonfiguráció beállításához.</span><span class="sxs-lookup"><span data-stu-id="a8a71-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a8a71-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a8a71-113">EXAMPLES</span></span>

### <span data-ttu-id="a8a71-114">1. példa: az alapértelmezett tárterület-fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="a8a71-114">Example 1: Set the default storage account</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="a8a71-115">Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8a71-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="a8a71-116">A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8a71-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="a8a71-117">A negyedik, az ötödik és a hatodik parancs a **Get-hitelesítőadat** parancsmagot használja a jelenlegi előfizetéshez tartozó hitelesítő adatok beszerzéséhez, majd a hitelesítő adatokat tárolja a $creds, a $OozieCreds és a $HiveCreds változók között.</span><span class="sxs-lookup"><span data-stu-id="a8a71-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="a8a71-118">A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="a8a71-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="a8a71-119">**Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a8a71-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="a8a71-120">**Set-AzureHDInsightDefaultStorage** : beállíthatja a konfiguráció alapértelmezett tárolási fiókját a MyBlobStorage.blob.Core.Windows.net értékre.</span><span class="sxs-lookup"><span data-stu-id="a8a71-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="a8a71-121">**Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók felvétele a konfigurációba.</span><span class="sxs-lookup"><span data-stu-id="a8a71-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="a8a71-122">**Add-AzureHDInsightMetastore** : adjon hozzá egy Metastore a Oozie-hoz, és egy Metastore a kaptár számára a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="a8a71-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="a8a71-123">**Új – AzureHDInsightCluster** : hozzon létre egy HDInsight-fürtöt az új konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="a8a71-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="a8a71-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8a71-124">PARAMETERS</span></span>

### <span data-ttu-id="a8a71-125">-Config</span><span class="sxs-lookup"><span data-stu-id="a8a71-125">-Config</span></span>
<span data-ttu-id="a8a71-126">Konfigurációs objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a8a71-126">Specifies a configuration object.</span></span>
<span data-ttu-id="a8a71-127">Ez a parancsmag a paraméter által megadott objektum alapértelmezett tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8a71-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8a71-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8a71-128">-Profile</span></span>
<span data-ttu-id="a8a71-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a8a71-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8a71-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a8a71-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8a71-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a8a71-131">-StorageAccountKey</span></span>
<span data-ttu-id="a8a71-132">Az alapértelmezett tárterület-fiók eléréséhez használt tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8a71-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="a8a71-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8a71-133">-StorageAccountName</span></span>
<span data-ttu-id="a8a71-134">Az alapértelmezett tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8a71-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="a8a71-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a8a71-135">-StorageContainerName</span></span>
<span data-ttu-id="a8a71-136">A fürt alapértelmezett tárterületének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8a71-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="a8a71-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a71-137">CommonParameters</span></span>
<span data-ttu-id="a8a71-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8a71-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a71-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a71-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a71-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8a71-140">INPUTS</span></span>

## <span data-ttu-id="a8a71-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8a71-141">OUTPUTS</span></span>

## <span data-ttu-id="a8a71-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8a71-142">NOTES</span></span>

## <span data-ttu-id="a8a71-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8a71-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8a71-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="a8a71-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="a8a71-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a8a71-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="a8a71-146">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a8a71-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="a8a71-147">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a8a71-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


