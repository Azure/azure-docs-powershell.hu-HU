---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149747"
---
# <span data-ttu-id="48f11-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48f11-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="48f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f11-102">SYNOPSIS</span></span>
<span data-ttu-id="48f11-103">Adjon hozzá egy útválasztási szabályt a slothoz.</span><span class="sxs-lookup"><span data-stu-id="48f11-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="48f11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48f11-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f11-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48f11-105">DESCRIPTION</span></span>
<span data-ttu-id="48f11-106">Az **Add-AzWebAppTrafficRouting** parancsmag útválasztási szabályt ad az Azure Web App slothoz.</span><span class="sxs-lookup"><span data-stu-id="48f11-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="48f11-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48f11-107">EXAMPLES</span></span>

### <span data-ttu-id="48f11-108">1. példa útválasztási szabály hozzáadása a termelési forgalom 15%-ának átviteléhez Stg-tárolóhelyre</span><span class="sxs-lookup"><span data-stu-id="48f11-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="48f11-109">Ez a parancs egy útválasztási szabályt ad hozzá, amely a production traffice 15%-át az Stg-tárolóhelyre továbbítja</span><span class="sxs-lookup"><span data-stu-id="48f11-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="48f11-110">2. példa: Adjon hozzá egy útválasztási szabályt a termelési forgalom Stg-tárolóhelyre való átviteléhez 50%-tól 90%-ig növekményes módon.</span><span class="sxs-lookup"><span data-stu-id="48f11-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="48f11-111">Ez a parancs egy útválasztási szabályt ad hozzá a termelési adatforgalom Stg-tárolóhelyre való átviteléhez, növekményes módon 50%-tól 90%-ig.</span><span class="sxs-lookup"><span data-stu-id="48f11-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="48f11-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48f11-112">PARAMETERS</span></span>

### <span data-ttu-id="48f11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f11-113">-DefaultProfile</span></span>
<span data-ttu-id="48f11-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48f11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48f11-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f11-115">-ResourceGroupName</span></span>
<span data-ttu-id="48f11-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="48f11-116">Resource Group Name</span></span>

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

### <span data-ttu-id="48f11-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="48f11-117">-RoutingRule</span></span>
<span data-ttu-id="48f11-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="48f11-118">Web App RoutingRule.</span></span>
<span data-ttu-id="48f11-119">Példa: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="48f11-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="48f11-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="48f11-120">-WebAppName</span></span>
<span data-ttu-id="48f11-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="48f11-121">WebApp Name</span></span>

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

### <span data-ttu-id="48f11-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48f11-122">-Confirm</span></span>
<span data-ttu-id="48f11-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="48f11-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f11-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f11-124">-WhatIf</span></span>
<span data-ttu-id="48f11-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="48f11-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f11-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48f11-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f11-127">CommonParameters</span></span>
<span data-ttu-id="48f11-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f11-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48f11-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f11-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48f11-130">INPUTS</span></span>

### <span data-ttu-id="48f11-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="48f11-131">None</span></span>

## <span data-ttu-id="48f11-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48f11-132">OUTPUTS</span></span>

### <span data-ttu-id="48f11-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="48f11-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="48f11-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48f11-134">NOTES</span></span>

## <span data-ttu-id="48f11-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48f11-135">RELATED LINKS</span></span>
[<span data-ttu-id="48f11-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48f11-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="48f11-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48f11-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="48f11-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="48f11-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
