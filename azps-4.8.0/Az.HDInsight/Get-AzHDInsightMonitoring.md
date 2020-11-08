---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018092"
---
# <span data-ttu-id="1d8d2-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1d8d2-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="1d8d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8d2-103">A telepítés figyelésének állapotát kapja meg a fürtben.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="1d8d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d8d2-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d8d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="1d8d2-106">A **Get-AzHDInsightMonitoring** parancsmag az Azure HDInsight-fürtökben a telepítés figyelésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="1d8d2-107">Ha a figyelés engedélyezve van, akkor az a log Analytics munkaterület-azonosítóját is visszaadja.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="1d8d2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1d8d2-108">EXAMPLES</span></span>

### <span data-ttu-id="1d8d2-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d8d2-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="1d8d2-110">A felügyelet engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="1d8d2-111">A naplókat átáramló figyelési munkaterület azonosítója 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="1d8d2-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="1d8d2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1d8d2-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="1d8d2-113">A felügyelet engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="1d8d2-114">A naplókat átáramló figyelési munkaterület azonosítója 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="1d8d2-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="1d8d2-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="1d8d2-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="1d8d2-116">A felügyelet le van tiltva a fürtben, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="1d8d2-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="1d8d2-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="1d8d2-118">A felügyelet le van tiltva a fürtben, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="1d8d2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d8d2-119">PARAMETERS</span></span>

### <span data-ttu-id="1d8d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8d2-120">-DefaultProfile</span></span>
<span data-ttu-id="1d8d2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d8d2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d8d2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d8d2-122">-Name</span></span>
<span data-ttu-id="1d8d2-123">Annak a csoportnak a neve, amely a figyelési állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="1d8d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d8d2-125">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="1d8d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8d2-126">CommonParameters</span></span>
<span data-ttu-id="1d8d2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d8d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8d2-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d8d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8d2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d8d2-129">INPUTS</span></span>

### <span data-ttu-id="1d8d2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d8d2-130">System.String</span></span>

## <span data-ttu-id="1d8d2-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d8d2-131">OUTPUTS</span></span>

### <span data-ttu-id="1d8d2-132">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1d8d2-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="1d8d2-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d8d2-133">NOTES</span></span>

## <span data-ttu-id="1d8d2-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d8d2-134">RELATED LINKS</span></span>
