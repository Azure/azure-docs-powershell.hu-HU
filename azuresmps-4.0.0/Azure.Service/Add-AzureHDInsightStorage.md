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
# <span data-ttu-id="e2dcc-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e2dcc-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="e2dcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dcc-103">A blob-tároló-fiók bejegyzését hozzáadja egy HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="e2dcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2dcc-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2dcc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="e2dcc-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e2dcc-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e2dcc-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e2dcc-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e2dcc-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e2dcc-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="e2dcc-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e2dcc-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e2dcc-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e2dcc-112">Az **Add-AzureHDInsightStorage** parancsmag blob-tárolási fiókot ad hozzá egy Azure HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="e2dcc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e2dcc-113">EXAMPLES</span></span>

### <span data-ttu-id="e2dcc-114">1. példa: tárterület-fiók hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e2dcc-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="e2dcc-115">Ez a parancs hozzáadja a MyStorage nevű tárolási fiókot a $Config tárolt konfigurációs objektumhoz, majd a $StoreConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="e2dcc-116">2. példa: több tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="e2dcc-116">Example 2: Configure multiple storage accounts</span></span>
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

<span data-ttu-id="e2dcc-117">Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e2dcc-118">A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="e2dcc-119">A negyedik, az ötödik és a hatodik parancs hitelesítő adatokat kap az aktuális előfizetéshez, valamint a Oozie és a Kaptárhoz, majd tárolja a hitelesítő adatokat a változókban.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="e2dcc-120">A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="e2dcc-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="e2dcc-121">**Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="e2dcc-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="e2dcc-122">**Set-AzureHDInsightDefaultStorage** : a konfiguráció alapértelmezett tárolási fiókjának beállítása a MyBlobStorage.blob.Core.Windows.net</span><span class="sxs-lookup"><span data-stu-id="e2dcc-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="e2dcc-123">**Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók hozzáadása a konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="e2dcc-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="e2dcc-124">**Add-AzureHDInsightStorage** : metastore hozzáadása az Oozie-hoz és a struktúra metastore a konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="e2dcc-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="e2dcc-125">**Új – AzureHDInsightCluster** új HDInsight-fürtöt hozhat létre az új konfigurációval</span><span class="sxs-lookup"><span data-stu-id="e2dcc-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="e2dcc-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2dcc-126">PARAMETERS</span></span>

### <span data-ttu-id="e2dcc-127">-Config</span><span class="sxs-lookup"><span data-stu-id="e2dcc-127">-Config</span></span>
<span data-ttu-id="e2dcc-128">Konfigurációs objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-128">Specifies a configuration object.</span></span>
<span data-ttu-id="e2dcc-129">Ez a parancsmag a megfelelő tárterület-információkat hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2dcc-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2dcc-130">-Profile</span></span>
<span data-ttu-id="e2dcc-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2dcc-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2dcc-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2dcc-133">-StorageAccountKey</span></span>
<span data-ttu-id="e2dcc-134">A tárterület-fiók eléréséhez használt tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="e2dcc-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e2dcc-135">-StorageAccountName</span></span>
<span data-ttu-id="e2dcc-136">A hozzáadni kívánt Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2dcc-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="e2dcc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dcc-137">CommonParameters</span></span>
<span data-ttu-id="e2dcc-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2dcc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dcc-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dcc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dcc-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2dcc-140">INPUTS</span></span>

## <span data-ttu-id="e2dcc-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2dcc-141">OUTPUTS</span></span>

## <span data-ttu-id="e2dcc-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2dcc-142">NOTES</span></span>

## <span data-ttu-id="e2dcc-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2dcc-143">RELATED LINKS</span></span>

[<span data-ttu-id="e2dcc-144">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2dcc-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e2dcc-145">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e2dcc-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="e2dcc-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e2dcc-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


