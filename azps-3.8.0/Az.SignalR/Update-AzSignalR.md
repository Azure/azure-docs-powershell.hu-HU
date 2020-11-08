---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 52e422f6c86f17c6620c58c1034b45250d4edf08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011282"
---
# <span data-ttu-id="e1997-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="e1997-101">Update-AzSignalR</span></span>

## <span data-ttu-id="e1997-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1997-102">SYNOPSIS</span></span>
<span data-ttu-id="e1997-103">A szignáló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="e1997-103">Update a SignalR service.</span></span>

## <span data-ttu-id="e1997-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1997-104">SYNTAX</span></span>

### <span data-ttu-id="e1997-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1997-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1997-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1997-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1997-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1997-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1997-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1997-108">DESCRIPTION</span></span>
<span data-ttu-id="e1997-109">A szignáló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="e1997-109">Update a SignalR service.</span></span>
<span data-ttu-id="e1997-110">Ha nem adja meg a paramétereket, a program a következő értékeket fogja használni:</span><span class="sxs-lookup"><span data-stu-id="e1997-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="e1997-111">`ResourceGroupName`: az alapértelmezett erőforráscsoport beállítása `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="e1997-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="e1997-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="e1997-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="e1997-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e1997-113">EXAMPLES</span></span>

### <span data-ttu-id="e1997-114">Frissítsen egy adott jelfeldolgozó szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e1997-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="e1997-115">A ServiceMode és a AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="e1997-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="e1997-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1997-116">PARAMETERS</span></span>

### <span data-ttu-id="e1997-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="e1997-117">-AllowedOrigin</span></span>
<span data-ttu-id="e1997-118">A jelző szolgáltatás megengedett eredete.</span><span class="sxs-lookup"><span data-stu-id="e1997-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="e1997-119">Az összes engedélyezéséhez használja a "\*" és az összes többi eredetét a listából.</span><span class="sxs-lookup"><span data-stu-id="e1997-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="e1997-120">A kivágás nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="e1997-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="e1997-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1997-121">-AsJob</span></span>
<span data-ttu-id="e1997-122">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e1997-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="e1997-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1997-123">-DefaultProfile</span></span>
<span data-ttu-id="e1997-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1997-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1997-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1997-125">-InputObject</span></span>
<span data-ttu-id="e1997-126">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="e1997-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1997-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1997-127">-Name</span></span>
<span data-ttu-id="e1997-128">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e1997-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1997-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1997-129">-ResourceGroupName</span></span>
<span data-ttu-id="e1997-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1997-130">The resource group name.</span></span>
<span data-ttu-id="e1997-131">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e1997-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1997-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1997-132">-ResourceId</span></span>
<span data-ttu-id="e1997-133">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1997-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1997-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="e1997-134">-ServiceMode</span></span>
<span data-ttu-id="e1997-135">A jeladó szolgáltatás üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="e1997-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="e1997-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="e1997-136">-Sku</span></span>
<span data-ttu-id="e1997-137">A szignáló szolgáltatás SKU-je.</span><span class="sxs-lookup"><span data-stu-id="e1997-137">The SignalR service SKU.</span></span>
<span data-ttu-id="e1997-138">Alapértelmezett érték: "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="e1997-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="e1997-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="e1997-139">-Tag</span></span>
<span data-ttu-id="e1997-140">A jelző szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="e1997-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="e1997-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="e1997-141">-UnitCount</span></span>
<span data-ttu-id="e1997-142">A szignáló szolgáltatás egységének értéke csak {1, 2, 5, 10, 20, 50, 100} esetén számítható ki.</span><span class="sxs-lookup"><span data-stu-id="e1997-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="e1997-143">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="e1997-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1997-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1997-144">-Confirm</span></span>
<span data-ttu-id="e1997-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1997-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1997-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1997-146">-WhatIf</span></span>
<span data-ttu-id="e1997-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1997-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1997-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1997-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1997-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1997-149">CommonParameters</span></span>
<span data-ttu-id="e1997-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1997-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1997-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1997-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1997-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1997-152">INPUTS</span></span>

### <span data-ttu-id="e1997-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e1997-153">System.String</span></span>

### <span data-ttu-id="e1997-154">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="e1997-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="e1997-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1997-155">OUTPUTS</span></span>

### <span data-ttu-id="e1997-156">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="e1997-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="e1997-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1997-157">NOTES</span></span>

## <span data-ttu-id="e1997-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1997-158">RELATED LINKS</span></span>
