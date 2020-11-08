---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181490"
---
# <span data-ttu-id="2b1c5-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="2b1c5-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="2b1c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1c5-103">Fürtök beolvasása és listázása</span><span class="sxs-lookup"><span data-stu-id="2b1c5-103">Get or list clusters</span></span>

## <span data-ttu-id="2b1c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b1c5-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1c5-106">Csoportosíthatja vagy listázhatja a fürtöket, az erőforráscsoport csoportban felsorolhatja az "-fürtnév" kifejezést, ha a "-fürtnév" és a "ResourceGroupName" nem volt megadva.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="2b1c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b1c5-107">EXAMPLES</span></span>

### <span data-ttu-id="2b1c5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b1c5-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="2b1c5-109">Fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="2b1c5-109">Get cluster</span></span>

## <span data-ttu-id="2b1c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b1c5-110">PARAMETERS</span></span>

### <span data-ttu-id="2b1c5-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="2b1c5-111">-ClusterName</span></span>
<span data-ttu-id="2b1c5-112">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1c5-113">-DefaultProfile</span></span>
<span data-ttu-id="2b1c5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1c5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b1c5-115">-ResourceGroupName</span></span>
<span data-ttu-id="2b1c5-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1c5-117">CommonParameters</span></span>
<span data-ttu-id="2b1c5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b1c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1c5-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1c5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1c5-120">INPUTS</span></span>

### <span data-ttu-id="2b1c5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2b1c5-121">System.String</span></span>

## <span data-ttu-id="2b1c5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1c5-122">OUTPUTS</span></span>

### <span data-ttu-id="2b1c5-123">Microsoft. Azure. Command. OperationalInsights. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2b1c5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="2b1c5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b1c5-124">NOTES</span></span>

## <span data-ttu-id="2b1c5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b1c5-125">RELATED LINKS</span></span>
