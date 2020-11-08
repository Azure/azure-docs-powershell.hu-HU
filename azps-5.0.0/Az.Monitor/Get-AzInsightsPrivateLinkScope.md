---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194309"
---
# <span data-ttu-id="00335-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="00335-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="00335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00335-102">SYNOPSIS</span></span>
<span data-ttu-id="00335-103">Magánjellegű hivatkozás beszerzése</span><span class="sxs-lookup"><span data-stu-id="00335-103">Get private link scope</span></span>

## <span data-ttu-id="00335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00335-104">SYNTAX</span></span>

### <span data-ttu-id="00335-105">ByResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00335-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00335-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00335-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00335-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00335-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00335-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="00335-108">DESCRIPTION</span></span>
<span data-ttu-id="00335-109">A lista vagy a magánjellegű hivatkozás beszerzése</span><span class="sxs-lookup"><span data-stu-id="00335-109">List or get private link scope</span></span> 

## <span data-ttu-id="00335-110">Példák</span><span class="sxs-lookup"><span data-stu-id="00335-110">EXAMPLES</span></span>

### <span data-ttu-id="00335-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00335-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="00335-112">A magánjellegű hivatkozásokat felsoroló hatókörök listája az erőforráscsoport "rg_name" csoportjába</span><span class="sxs-lookup"><span data-stu-id="00335-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="00335-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="00335-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="00335-114">A privát hivatkozás lekérése "scope_name" névvel az erőforráscsoport "rg_name" csoportjában</span><span class="sxs-lookup"><span data-stu-id="00335-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="00335-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00335-115">PARAMETERS</span></span>

### <span data-ttu-id="00335-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00335-116">-DefaultProfile</span></span>
<span data-ttu-id="00335-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00335-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00335-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00335-118">-Name</span></span>
<span data-ttu-id="00335-119">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="00335-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00335-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00335-120">-ResourceGroupName</span></span>
<span data-ttu-id="00335-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="00335-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00335-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00335-122">-ResourceId</span></span>
<span data-ttu-id="00335-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="00335-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00335-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00335-124">CommonParameters</span></span>
<span data-ttu-id="00335-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00335-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00335-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00335-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00335-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00335-127">INPUTS</span></span>

### <span data-ttu-id="00335-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00335-128">System.String</span></span>

## <span data-ttu-id="00335-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00335-129">OUTPUTS</span></span>

### <span data-ttu-id="00335-130">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="00335-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="00335-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00335-131">NOTES</span></span>

## <span data-ttu-id="00335-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00335-132">RELATED LINKS</span></span>