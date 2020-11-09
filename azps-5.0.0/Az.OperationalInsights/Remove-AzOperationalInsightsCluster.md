---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300293"
---
# <span data-ttu-id="3416a-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="3416a-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="3416a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3416a-102">SYNOPSIS</span></span>
<span data-ttu-id="3416a-103">Fürt törlése</span><span class="sxs-lookup"><span data-stu-id="3416a-103">Delete cluster</span></span>

## <span data-ttu-id="3416a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3416a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3416a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3416a-105">DESCRIPTION</span></span>
<span data-ttu-id="3416a-106">Fürt törlése, csak a kiépítési állapotú fürtök esetében "sikerült"</span><span class="sxs-lookup"><span data-stu-id="3416a-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="3416a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3416a-107">EXAMPLES</span></span>

### <span data-ttu-id="3416a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3416a-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="3416a-109">Fürt törlése</span><span class="sxs-lookup"><span data-stu-id="3416a-109">Delete cluster</span></span>

## <span data-ttu-id="3416a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3416a-110">PARAMETERS</span></span>

### <span data-ttu-id="3416a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3416a-111">-AsJob</span></span>
<span data-ttu-id="3416a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3416a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3416a-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="3416a-113">-ClusterName</span></span>
<span data-ttu-id="3416a-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3416a-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3416a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3416a-115">-DefaultProfile</span></span>
<span data-ttu-id="3416a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3416a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3416a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3416a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3416a-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3416a-118">The resource group name.</span></span>

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

### <span data-ttu-id="3416a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3416a-119">-Confirm</span></span>
<span data-ttu-id="3416a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3416a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3416a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3416a-121">-WhatIf</span></span>
<span data-ttu-id="3416a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3416a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3416a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3416a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3416a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3416a-124">CommonParameters</span></span>
<span data-ttu-id="3416a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3416a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3416a-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3416a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3416a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3416a-127">INPUTS</span></span>

### <span data-ttu-id="3416a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3416a-128">System.String</span></span>

## <span data-ttu-id="3416a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3416a-129">OUTPUTS</span></span>

### <span data-ttu-id="3416a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3416a-130">System.Boolean</span></span>

## <span data-ttu-id="3416a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3416a-131">NOTES</span></span>

## <span data-ttu-id="3416a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3416a-132">RELATED LINKS</span></span>
