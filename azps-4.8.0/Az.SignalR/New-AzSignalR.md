---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025978"
---
# <span data-ttu-id="95796-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="95796-101">New-AzSignalR</span></span>

## <span data-ttu-id="95796-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95796-102">SYNOPSIS</span></span>
<span data-ttu-id="95796-103">Szignáló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="95796-103">Create a SignalR service.</span></span>

## <span data-ttu-id="95796-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95796-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95796-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95796-105">DESCRIPTION</span></span>
<span data-ttu-id="95796-106">Szignáló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="95796-106">Create a SignalR service.</span></span>
<span data-ttu-id="95796-107">Ha nem adja meg a paramétereket, a program a következő értékeket fogja használni:</span><span class="sxs-lookup"><span data-stu-id="95796-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="95796-108">`ResourceGroupName`: az alapértelmezett erőforráscsoport beállítása `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="95796-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="95796-109">`Location`: az erőforráscsoport helye</span><span class="sxs-lookup"><span data-stu-id="95796-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="95796-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="95796-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="95796-111">Példák</span><span class="sxs-lookup"><span data-stu-id="95796-111">EXAMPLES</span></span>

### <span data-ttu-id="95796-112">Szignáló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="95796-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="95796-113">A ServiceMode és a AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="95796-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="95796-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95796-114">PARAMETERS</span></span>

### <span data-ttu-id="95796-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="95796-115">-AllowedOrigin</span></span>
<span data-ttu-id="95796-116">A jelző szolgáltatás megengedett eredete.</span><span class="sxs-lookup"><span data-stu-id="95796-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="95796-117">Az összes engedélyezéséhez használja a "\*" és az összes többi eredetét a listából.</span><span class="sxs-lookup"><span data-stu-id="95796-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="95796-118">A kivágás nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="95796-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="95796-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95796-119">-AsJob</span></span>
<span data-ttu-id="95796-120">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="95796-120">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95796-121">-DefaultProfile</span></span>
<span data-ttu-id="95796-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95796-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95796-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="95796-123">-Location</span></span>
<span data-ttu-id="95796-124">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="95796-124">The SignalR service location.</span></span> <span data-ttu-id="95796-125">A program az erőforráscsoport helyét használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="95796-125">The resource group location will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95796-126">-Name</span></span>
<span data-ttu-id="95796-127">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="95796-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95796-128">-ResourceGroupName</span></span>
<span data-ttu-id="95796-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="95796-129">The resource group name.</span></span> <span data-ttu-id="95796-130">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="95796-130">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="95796-131">-ServiceMode</span></span>
<span data-ttu-id="95796-132">A jeladó szolgáltatás üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="95796-132">The service mode for the SignalR service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="95796-133">-Sku</span></span>
<span data-ttu-id="95796-134">A szignáló szolgáltatás SKU-je.</span><span class="sxs-lookup"><span data-stu-id="95796-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="95796-135">-Tag</span></span>
<span data-ttu-id="95796-136">A jelző szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="95796-136">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="95796-137">-UnitCount</span></span>
<span data-ttu-id="95796-138">A szignáló szolgáltatás egységének száma 1-től 10-ig.</span><span class="sxs-lookup"><span data-stu-id="95796-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="95796-139">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="95796-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95796-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95796-140">-Confirm</span></span>
<span data-ttu-id="95796-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95796-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95796-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95796-142">-WhatIf</span></span>
<span data-ttu-id="95796-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95796-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95796-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95796-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95796-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95796-145">CommonParameters</span></span>
<span data-ttu-id="95796-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95796-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95796-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95796-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95796-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95796-148">INPUTS</span></span>

### <span data-ttu-id="95796-149">System. String</span><span class="sxs-lookup"><span data-stu-id="95796-149">System.String</span></span>

## <span data-ttu-id="95796-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95796-150">OUTPUTS</span></span>

### <span data-ttu-id="95796-151">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="95796-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="95796-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95796-152">NOTES</span></span>

## <span data-ttu-id="95796-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95796-153">RELATED LINKS</span></span>
