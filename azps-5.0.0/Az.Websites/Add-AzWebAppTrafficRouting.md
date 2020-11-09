---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300911"
---
# <span data-ttu-id="e7664-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e7664-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="e7664-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7664-102">SYNOPSIS</span></span>
<span data-ttu-id="e7664-103">Útválasztási szabály hozzáadása a bővítőhelyhez</span><span class="sxs-lookup"><span data-stu-id="e7664-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="e7664-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7664-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7664-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7664-105">DESCRIPTION</span></span>
<span data-ttu-id="e7664-106">Az **Add-AzWebAppTrafficRouting** parancsmag útválasztási szabályt ad az Azure Web App-bővítőhelyekhez.</span><span class="sxs-lookup"><span data-stu-id="e7664-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="e7664-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7664-107">EXAMPLES</span></span>

### <span data-ttu-id="e7664-108">1. példa: útválasztási szabály hozzáadása a termelési forgalom 15%-ának átadásához STG-bővítőhelyre</span><span class="sxs-lookup"><span data-stu-id="e7664-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="e7664-109">Ez a parancs egy útválasztási szabályt ad hozzá a termelési forgalom 15%-ának a STG-bővítőhelyre való átviteléhez.</span><span class="sxs-lookup"><span data-stu-id="e7664-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="e7664-110">2. példa: útválasztási szabály hozzáadása a termelési forgalom átadásához a STG 50%-ról 90%-ra növekvő módon.</span><span class="sxs-lookup"><span data-stu-id="e7664-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="e7664-111">Ez a parancs egy útválasztási szabályt ad hozzá, amellyel átviheti a termelési forgalmat a 50%-ról 90%-ra növekvő STG.</span><span class="sxs-lookup"><span data-stu-id="e7664-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="e7664-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7664-112">PARAMETERS</span></span>

### <span data-ttu-id="e7664-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7664-113">-DefaultProfile</span></span>
<span data-ttu-id="e7664-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7664-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7664-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7664-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7664-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e7664-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e7664-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7664-117">-RoutingRule</span></span>
<span data-ttu-id="e7664-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="e7664-118">Web App RoutingRule.</span></span>
<span data-ttu-id="e7664-119">Példa:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="e7664-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7664-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e7664-120">-WebAppName</span></span>
<span data-ttu-id="e7664-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e7664-121">WebApp Name</span></span>

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

### <span data-ttu-id="e7664-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7664-122">-Confirm</span></span>
<span data-ttu-id="e7664-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7664-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7664-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7664-124">-WhatIf</span></span>
<span data-ttu-id="e7664-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7664-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7664-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7664-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7664-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7664-127">CommonParameters</span></span>
<span data-ttu-id="e7664-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7664-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7664-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7664-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7664-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7664-130">INPUTS</span></span>

### <span data-ttu-id="e7664-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7664-131">None</span></span>

## <span data-ttu-id="e7664-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7664-132">OUTPUTS</span></span>

### <span data-ttu-id="e7664-133">Microsoft. Azure. Management. WebSites. models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="e7664-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="e7664-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7664-134">NOTES</span></span>

## <span data-ttu-id="e7664-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7664-135">RELATED LINKS</span></span>
[<span data-ttu-id="e7664-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e7664-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e7664-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e7664-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e7664-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e7664-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
