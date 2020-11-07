---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f8971070851da36fb1bf72aef33085e974ef1fb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847613"
---
# <span data-ttu-id="3277d-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="3277d-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="3277d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3277d-102">SYNOPSIS</span></span>
<span data-ttu-id="3277d-103">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="3277d-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="3277d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3277d-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3277d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3277d-105">DESCRIPTION</span></span>
<span data-ttu-id="3277d-106">Az **Add-AzHDInsightMetastore** parancsmag az New-AzHDInsightClusterConfig parancsmag által létrehozott HDInsight-konfigurációs objektumhoz ad hozzá egy kaptárt vagy egy Oozie metastore.</span><span class="sxs-lookup"><span data-stu-id="3277d-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="3277d-107">A metastore egy SQL-adatbázis, amellyel a kaptár, a Oozie vagy mindkettő metaadatait tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="3277d-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="3277d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3277d-108">EXAMPLES</span></span>

### <span data-ttu-id="3277d-109">1. példa: SQL-adatbázis metastore felvétele a fürtkonfigurációs objektumba</span><span class="sxs-lookup"><span data-stu-id="3277d-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="3277d-110">A parancs hozzáadja az SQL-adatbázis metastore a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="3277d-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3277d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3277d-111">PARAMETERS</span></span>

### <span data-ttu-id="3277d-112">-Config</span><span class="sxs-lookup"><span data-stu-id="3277d-112">-Config</span></span>
<span data-ttu-id="3277d-113">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3277d-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3277d-114">Ezt az objektumot a **New-AzHDInsightClusterConfig** parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3277d-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-115">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="3277d-115">-Credential</span></span>
<span data-ttu-id="3277d-116">Az AzureSQL kiszolgálói adatbázishoz használandó hitelesítő adatok megadása.</span><span class="sxs-lookup"><span data-stu-id="3277d-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3277d-117">-DatabaseName</span></span>
<span data-ttu-id="3277d-118">A AzureSQL-kiszolgálópéldány azon adatbázisát adja meg, amely ehhez a metastore használható.</span><span class="sxs-lookup"><span data-stu-id="3277d-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3277d-119">-DefaultProfile</span></span>
<span data-ttu-id="3277d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3277d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="3277d-121">-MetastoreType</span></span>
<span data-ttu-id="3277d-122">A metastore típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3277d-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="3277d-123">Lehetséges értékek: HiveMetastore vagy OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="3277d-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="3277d-124">-SqlAzureServerName</span></span>
<span data-ttu-id="3277d-125">Itt adhatja meg a metastore használni kívánt AzureSQL-kiszolgálópéldány használatát.</span><span class="sxs-lookup"><span data-stu-id="3277d-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3277d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3277d-126">CommonParameters</span></span>
<span data-ttu-id="3277d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3277d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3277d-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3277d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3277d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3277d-129">INPUTS</span></span>

### <span data-ttu-id="3277d-130">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3277d-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3277d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3277d-131">OUTPUTS</span></span>

### <span data-ttu-id="3277d-132">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3277d-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3277d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3277d-133">NOTES</span></span>

## <span data-ttu-id="3277d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3277d-134">RELATED LINKS</span></span>

[<span data-ttu-id="3277d-135">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3277d-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


