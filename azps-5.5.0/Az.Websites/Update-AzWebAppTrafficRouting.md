---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207423"
---
# <span data-ttu-id="3acf9-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3acf9-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="3acf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3acf9-102">SYNOPSIS</span></span>
<span data-ttu-id="3acf9-103">Továbbítási szabály frissítése a slotra.</span><span class="sxs-lookup"><span data-stu-id="3acf9-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="3acf9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3acf9-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3acf9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3acf9-105">DESCRIPTION</span></span>
<span data-ttu-id="3acf9-106">Az **Update-AzWebAppTrafficRouting** parancsmag frissíti az Azure Web App Slot útválasztási szabálykonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3acf9-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="3acf9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3acf9-107">EXAMPLES</span></span>

### <span data-ttu-id="3acf9-108">1. példa: Útválasztási szabály frissítése az adatforgalom 15%-ának Stg-re történő átviteléhez</span><span class="sxs-lookup"><span data-stu-id="3acf9-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="3acf9-109">Ez a parancs frissíti az útválasztási szabályt úgy, hogy az a production-forgalom 15%-át átnyússa az Stg-tárolóhelyre.</span><span class="sxs-lookup"><span data-stu-id="3acf9-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="3acf9-110">2. példa: Az útválasztási szabály frissítése a termelési adatforgalom Stg-tárolóhelyre való átviteléhez 50%-tól 90%-ig növekményes módon.</span><span class="sxs-lookup"><span data-stu-id="3acf9-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="3acf9-111">Ez a parancs Egy útválasztási szabály frissítése a termelési adatforgalom Stg-tárolóhelyre való átviteléhez 50%-tól 90%-ig növekményes módon.</span><span class="sxs-lookup"><span data-stu-id="3acf9-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="3acf9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3acf9-112">PARAMETERS</span></span>

### <span data-ttu-id="3acf9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acf9-113">-DefaultProfile</span></span>
<span data-ttu-id="3acf9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3acf9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3acf9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acf9-115">-ResourceGroupName</span></span>
<span data-ttu-id="3acf9-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acf9-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="3acf9-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="3acf9-117">-RoutingRule</span></span>
<span data-ttu-id="3acf9-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="3acf9-118">Web App RoutingRule.</span></span>
<span data-ttu-id="3acf9-119">Példa: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="3acf9-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="3acf9-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3acf9-120">-WebAppName</span></span>
<span data-ttu-id="3acf9-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="3acf9-121">WebApp Name</span></span>

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

### <span data-ttu-id="3acf9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3acf9-122">-Confirm</span></span>
<span data-ttu-id="3acf9-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3acf9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3acf9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3acf9-124">-WhatIf</span></span>
<span data-ttu-id="3acf9-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3acf9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3acf9-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3acf9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3acf9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acf9-127">CommonParameters</span></span>
<span data-ttu-id="3acf9-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acf9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acf9-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3acf9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acf9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3acf9-130">INPUTS</span></span>

### <span data-ttu-id="3acf9-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="3acf9-131">None</span></span>

## <span data-ttu-id="3acf9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3acf9-132">OUTPUTS</span></span>

### <span data-ttu-id="3acf9-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="3acf9-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="3acf9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3acf9-134">NOTES</span></span>

## <span data-ttu-id="3acf9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3acf9-135">RELATED LINKS</span></span>

[<span data-ttu-id="3acf9-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3acf9-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3acf9-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3acf9-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3acf9-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3acf9-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)