---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009126"
---
# <span data-ttu-id="fdcc1-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fdcc1-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fdcc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcc1-103">A fürtön telepített telepítés figyelési állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="fdcc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdcc1-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdcc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcc1-106">A **Get-AzHDInsightMonitoring** parancsmag egy Azure HDInsight-fürt telepítésének figyelési állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="fdcc1-107">Ha a figyelés engedélyezve van, akkor a naplóelemzés munkaterület-azonosítóját is visszaadja.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="fdcc1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdcc1-108">EXAMPLES</span></span>

### <span data-ttu-id="fdcc1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fdcc1-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fdcc1-110">A figyelés engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fdcc1-111">A naplókat folyamló figyelési munkaterület-azonosító: 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fdcc1-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fdcc1-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fdcc1-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fdcc1-113">A figyelés engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fdcc1-114">A naplókat folyamló figyelési munkaterület-azonosító: 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fdcc1-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fdcc1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fdcc1-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="fdcc1-116">A fürtben le van tiltva a figyelés, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="fdcc1-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="fdcc1-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="fdcc1-118">A fürtben le van tiltva a figyelés, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="fdcc1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdcc1-119">PARAMETERS</span></span>

### <span data-ttu-id="fdcc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcc1-120">-DefaultProfile</span></span>
<span data-ttu-id="fdcc1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fdcc1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdcc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fdcc1-122">-Name</span></span>
<span data-ttu-id="fdcc1-123">Annak a fürtnek a neve, amely a figyelés állapotát jelzi.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdcc1-125">A fürt erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcc1-126">CommonParameters</span></span>
<span data-ttu-id="fdcc1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdcc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcc1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdcc1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcc1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdcc1-129">INPUTS</span></span>

### <span data-ttu-id="fdcc1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fdcc1-130">System.String</span></span>

## <span data-ttu-id="fdcc1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdcc1-131">OUTPUTS</span></span>

### <span data-ttu-id="fdcc1-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fdcc1-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="fdcc1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdcc1-133">NOTES</span></span>

## <span data-ttu-id="fdcc1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdcc1-134">RELATED LINKS</span></span>
