---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182450"
---
# <span data-ttu-id="47e58-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="47e58-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="47e58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47e58-102">SYNOPSIS</span></span>
<span data-ttu-id="47e58-103">Útválasztási szabály hozzáadása a bővítőhelyhez</span><span class="sxs-lookup"><span data-stu-id="47e58-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="47e58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47e58-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47e58-105">DESCRIPTION</span></span>
<span data-ttu-id="47e58-106">Az **Add-AzWebAppTrafficRouting** parancsmag útválasztási szabályt ad az Azure Web App-bővítőhelyekhez.</span><span class="sxs-lookup"><span data-stu-id="47e58-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="47e58-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47e58-107">EXAMPLES</span></span>

### <span data-ttu-id="47e58-108">1. példa: útválasztási szabály hozzáadása a termelési forgalom 15%-ának átadásához STG-bővítőhelyre</span><span class="sxs-lookup"><span data-stu-id="47e58-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="47e58-109">Ez a parancs egy útválasztási szabályt ad hozzá a termelési forgalom 15%-ának a STG-bővítőhelyre való átviteléhez.</span><span class="sxs-lookup"><span data-stu-id="47e58-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="47e58-110">2. példa: útválasztási szabály hozzáadása a termelési forgalom átadásához a STG 50%-ról 90%-ra növekvő módon.</span><span class="sxs-lookup"><span data-stu-id="47e58-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="47e58-111">Ez a parancs egy útválasztási szabályt ad hozzá, amellyel átviheti a termelési forgalmat a 50%-ról 90%-ra növekvő STG.</span><span class="sxs-lookup"><span data-stu-id="47e58-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="47e58-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47e58-112">PARAMETERS</span></span>

### <span data-ttu-id="47e58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e58-113">-DefaultProfile</span></span>
<span data-ttu-id="47e58-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47e58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e58-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e58-115">-ResourceGroupName</span></span>
<span data-ttu-id="47e58-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="47e58-116">Resource Group Name</span></span>

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

### <span data-ttu-id="47e58-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="47e58-117">-RoutingRule</span></span>
<span data-ttu-id="47e58-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="47e58-118">Web App RoutingRule.</span></span>
<span data-ttu-id="47e58-119">Példa:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="47e58-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="47e58-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="47e58-120">-WebAppName</span></span>
<span data-ttu-id="47e58-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="47e58-121">WebApp Name</span></span>

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

### <span data-ttu-id="47e58-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47e58-122">-Confirm</span></span>
<span data-ttu-id="47e58-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47e58-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e58-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e58-124">-WhatIf</span></span>
<span data-ttu-id="47e58-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47e58-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e58-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47e58-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e58-127">CommonParameters</span></span>
<span data-ttu-id="47e58-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47e58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e58-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47e58-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e58-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47e58-130">INPUTS</span></span>

### <span data-ttu-id="47e58-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="47e58-131">None</span></span>

## <span data-ttu-id="47e58-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47e58-132">OUTPUTS</span></span>

### <span data-ttu-id="47e58-133">Microsoft. Azure. Management. WebSites. models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="47e58-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="47e58-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47e58-134">NOTES</span></span>

## <span data-ttu-id="47e58-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47e58-135">RELATED LINKS</span></span>
[<span data-ttu-id="47e58-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="47e58-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="47e58-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="47e58-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="47e58-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="47e58-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
