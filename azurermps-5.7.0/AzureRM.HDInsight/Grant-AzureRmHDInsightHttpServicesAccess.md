---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493786"
---
# <span data-ttu-id="65d10-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="65d10-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="65d10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65d10-102">SYNOPSIS</span></span>
<span data-ttu-id="65d10-103">HTTP-hozzáférést biztosít a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65d10-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65d10-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65d10-105">DESCRIPTION</span></span>
<span data-ttu-id="65d10-106">A **Grant-AzureRmHDInsightHttpServicesAccess** parancsmag az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és a webes szolgáltatások segítségével http-hozzáférést ad.</span><span class="sxs-lookup"><span data-stu-id="65d10-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="65d10-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65d10-107">EXAMPLES</span></span>

### <span data-ttu-id="65d10-108">1. példa: HTTP-hozzáférés engedélyezése Azure HDInsight-fürthöz</span><span class="sxs-lookup"><span data-stu-id="65d10-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="65d10-109">Ez a parancs HTTP-hozzáférést ad a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65d10-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="65d10-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65d10-110">PARAMETERS</span></span>

### <span data-ttu-id="65d10-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="65d10-111">-ClusterName</span></span>
<span data-ttu-id="65d10-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65d10-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d10-113">-DefaultProfile</span></span>
<span data-ttu-id="65d10-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65d10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d10-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="65d10-115">-HttpCredential</span></span>
<span data-ttu-id="65d10-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65d10-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d10-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d10-117">-ResourceGroupName</span></span>
<span data-ttu-id="65d10-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65d10-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="65d10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d10-119">CommonParameters</span></span>
<span data-ttu-id="65d10-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65d10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d10-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d10-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d10-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d10-122">INPUTS</span></span>

### <span data-ttu-id="65d10-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="65d10-123">None</span></span>
<span data-ttu-id="65d10-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="65d10-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65d10-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d10-125">OUTPUTS</span></span>

### <span data-ttu-id="65d10-126">Microsoft. Azure. Management. HDInsight. models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="65d10-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="65d10-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65d10-127">NOTES</span></span>

## <span data-ttu-id="65d10-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65d10-128">RELATED LINKS</span></span>

[<span data-ttu-id="65d10-129">Visszavonás-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="65d10-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


