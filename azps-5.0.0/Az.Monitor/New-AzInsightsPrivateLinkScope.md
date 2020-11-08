---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194572"
---
# <span data-ttu-id="eb5db-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="eb5db-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="eb5db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb5db-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5db-103">privát hivatkozás létrehozása hatókör</span><span class="sxs-lookup"><span data-stu-id="eb5db-103">create private link scope</span></span>

## <span data-ttu-id="eb5db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb5db-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb5db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb5db-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5db-106">privát hivatkozás létrehozása hatókör</span><span class="sxs-lookup"><span data-stu-id="eb5db-106">create private link scope</span></span>

## <span data-ttu-id="eb5db-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb5db-107">EXAMPLES</span></span>

### <span data-ttu-id="eb5db-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb5db-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="eb5db-109">privát hivatkozás létrehozása "scope_name" névvel a "rg_name" nevű erőforráscsoport "eastus" csoportjában</span><span class="sxs-lookup"><span data-stu-id="eb5db-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="eb5db-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb5db-110">PARAMETERS</span></span>

### <span data-ttu-id="eb5db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5db-111">-DefaultProfile</span></span>
<span data-ttu-id="eb5db-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb5db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb5db-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb5db-113">-Location</span></span>
<span data-ttu-id="eb5db-114">Helyre</span><span class="sxs-lookup"><span data-stu-id="eb5db-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb5db-115">-Name</span></span>
<span data-ttu-id="eb5db-116">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="eb5db-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5db-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb5db-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="eb5db-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-119">-Címkék</span><span class="sxs-lookup"><span data-stu-id="eb5db-119">-Tags</span></span>
<span data-ttu-id="eb5db-120">Címkék</span><span class="sxs-lookup"><span data-stu-id="eb5db-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb5db-121">-Confirm</span></span>
<span data-ttu-id="eb5db-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb5db-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5db-123">-WhatIf</span></span>
<span data-ttu-id="eb5db-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb5db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb5db-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb5db-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5db-126">CommonParameters</span></span>
<span data-ttu-id="eb5db-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb5db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5db-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb5db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5db-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5db-129">INPUTS</span></span>

### <span data-ttu-id="eb5db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eb5db-130">System.String</span></span>

## <span data-ttu-id="eb5db-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5db-131">OUTPUTS</span></span>

### <span data-ttu-id="eb5db-132">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="eb5db-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="eb5db-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb5db-133">NOTES</span></span>

## <span data-ttu-id="eb5db-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb5db-134">RELATED LINKS</span></span>
