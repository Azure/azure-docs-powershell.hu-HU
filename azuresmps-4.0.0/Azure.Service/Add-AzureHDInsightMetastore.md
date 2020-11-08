---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015723"
---
# <span data-ttu-id="24506-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="24506-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="24506-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24506-102">SYNOPSIS</span></span>
<span data-ttu-id="24506-103">SQL Server-adatbázis-fiókot ad hozzá egy HDInsight-fürt konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="24506-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="24506-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24506-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="24506-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24506-105">DESCRIPTION</span></span>
<span data-ttu-id="24506-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="24506-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="24506-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="24506-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="24506-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="24506-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="24506-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="24506-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="24506-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="24506-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="24506-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="24506-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="24506-112">Az **Add-AzureHDInsightMetastore** PARANCSMAG Microsoft SQL Server-adatbázist ad hozzá a **New-AzureHDInsightClusterConfig** parancsmag által létrehozott Azure HDInsight-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="24506-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="24506-113">Az adatbázis a kaptár vagy a Oozie (vagy mindkettő) metaadatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="24506-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="24506-114">Példák</span><span class="sxs-lookup"><span data-stu-id="24506-114">EXAMPLES</span></span>

### <span data-ttu-id="24506-115">1. példa: metastore hozzáadása</span><span class="sxs-lookup"><span data-stu-id="24506-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="24506-116">Ez a parancs hozzáadja a ContosoSQLServer nevű SQL Server-adatbázist a HDInsight-fürtök kaptár-metastore.</span><span class="sxs-lookup"><span data-stu-id="24506-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="24506-117">2. példa: a tárterület beállítása és a metastores hozzáadása</span><span class="sxs-lookup"><span data-stu-id="24506-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="24506-118">Az első parancs a **Get-AzureSubscription** parancsmagot használja a jelenlegi előfizetés-azonosító beolvasásához, majd a $SubId változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="24506-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="24506-119">A második és a harmadik parancs a **Get-AzureStorageKey** parancsmagot használja a MyBlobStorage és a MySecondBlobStorage elsődleges tárterületének megadásához, majd a billentyűket a $Key 1 és $Key 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="24506-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="24506-120">A negyedik, az ötödik és a hatodik parancs a **Get-hitelesítőadat** parancsmagot használja az aktuális előfizetéshez tartozó hitelesítő adatok beszerzéséhez, valamint a Oozie és a kaptárhoz, majd a hitelesítő adatok tárolása a változókban.</span><span class="sxs-lookup"><span data-stu-id="24506-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="24506-121">A végleges parancs az alábbi parancsmagok használatával hajtja végre a műveletek sorozatát:</span><span class="sxs-lookup"><span data-stu-id="24506-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="24506-122">**Új – AzureHDInsightClusterConfig** : HDInsight-fürtkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="24506-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="24506-123">**Set-AzureHDInsightDefaultStorage** : beállíthatja a konfiguráció alapértelmezett tárolási fiókját a MyBlobStorage.blob.Core.Windows.net értékre.</span><span class="sxs-lookup"><span data-stu-id="24506-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="24506-124">**Add-AzureHDInsightStorage** : a MySecondBlobStorage.blob.Core.Windows.net nevű második tárolási fiók felvétele a konfigurációba.</span><span class="sxs-lookup"><span data-stu-id="24506-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="24506-125">**Add-AzureHDInsightMetastore** : adjon hozzá egy Metastore a Oozie-hoz, és egy Metastore a kaptár számára a konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="24506-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="24506-126">**Új – AzureHDInsightCluster** : hozzon létre egy HDInsight-fürtöt az új konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="24506-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="24506-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24506-127">PARAMETERS</span></span>

### <span data-ttu-id="24506-128">-Config</span><span class="sxs-lookup"><span data-stu-id="24506-128">-Config</span></span>
<span data-ttu-id="24506-129">Konfigurációs objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="24506-129">Specifies a configuration object.</span></span>
<span data-ttu-id="24506-130">Ez a parancsmag a metastore adatait hozzáadja a konfigurációs objektumhoz, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="24506-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="24506-131">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="24506-131">-Credential</span></span>
<span data-ttu-id="24506-132">Megadja az SQL Server-adatbázisok eléréséhez használt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="24506-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24506-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24506-133">-DatabaseName</span></span>
<span data-ttu-id="24506-134">Annak az adatbázisnak a nevét adja meg, amely a kaptár vagy a Oozie metaadatait tárolja.</span><span class="sxs-lookup"><span data-stu-id="24506-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="24506-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="24506-135">-MetastoreType</span></span>
<span data-ttu-id="24506-136">A metastore típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="24506-136">Specifies the metastore type.</span></span>
<span data-ttu-id="24506-137">A paraméter elfogadható értékei a következők: HiveMetaStore vagy OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="24506-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24506-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="24506-138">-Profile</span></span>
<span data-ttu-id="24506-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="24506-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24506-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="24506-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24506-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="24506-141">-SqlAzureServerName</span></span>
<span data-ttu-id="24506-142">Annak az SQL-kiszolgálónak a teljes tartománynevét adja meg, amely a metaadatok tárolására szolgáló adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="24506-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="24506-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24506-143">CommonParameters</span></span>
<span data-ttu-id="24506-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24506-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24506-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24506-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24506-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24506-146">INPUTS</span></span>

## <span data-ttu-id="24506-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24506-147">OUTPUTS</span></span>

## <span data-ttu-id="24506-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24506-148">NOTES</span></span>

## <span data-ttu-id="24506-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24506-149">RELATED LINKS</span></span>

[<span data-ttu-id="24506-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="24506-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="24506-151">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="24506-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="24506-152">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="24506-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="24506-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="24506-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
