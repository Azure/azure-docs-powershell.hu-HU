---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836026"
---
# <span data-ttu-id="c523e-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c523e-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="c523e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c523e-102">SYNOPSIS</span></span>
<span data-ttu-id="c523e-103">HTTP-hozzáférést biztosít a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c523e-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="c523e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c523e-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c523e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c523e-105">DESCRIPTION</span></span>
<span data-ttu-id="c523e-106">A **Grant-AzHDInsightHttpServicesAccess** parancsmag az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és a webes szolgáltatások segítségével http-hozzáférést ad.</span><span class="sxs-lookup"><span data-stu-id="c523e-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="c523e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c523e-107">EXAMPLES</span></span>

### <span data-ttu-id="c523e-108">1. példa: HTTP-hozzáférés engedélyezése Azure HDInsight-fürthöz</span><span class="sxs-lookup"><span data-stu-id="c523e-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="c523e-109">Ez a parancs HTTP-hozzáférést ad a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c523e-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c523e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c523e-110">PARAMETERS</span></span>

### <span data-ttu-id="c523e-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c523e-111">-ClusterName</span></span>
<span data-ttu-id="c523e-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c523e-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c523e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c523e-113">-DefaultProfile</span></span>
<span data-ttu-id="c523e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c523e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c523e-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c523e-115">-HttpCredential</span></span>
<span data-ttu-id="c523e-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c523e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c523e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c523e-117">-ResourceGroupName</span></span>
<span data-ttu-id="c523e-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c523e-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c523e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c523e-119">CommonParameters</span></span>
<span data-ttu-id="c523e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c523e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c523e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c523e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c523e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c523e-122">INPUTS</span></span>

### <span data-ttu-id="c523e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c523e-123">None</span></span>

## <span data-ttu-id="c523e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c523e-124">OUTPUTS</span></span>

### <span data-ttu-id="c523e-125">Microsoft. Azure. Management. HDInsight. models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="c523e-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="c523e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c523e-126">NOTES</span></span>

## <span data-ttu-id="c523e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c523e-127">RELATED LINKS</span></span>

[<span data-ttu-id="c523e-128">Visszavonás-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c523e-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


