---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025976"
---
# <span data-ttu-id="aee2a-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="aee2a-101">Update-AzSignalR</span></span>

## <span data-ttu-id="aee2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aee2a-102">SYNOPSIS</span></span>
<span data-ttu-id="aee2a-103">A szignáló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="aee2a-103">Update a SignalR service.</span></span>

## <span data-ttu-id="aee2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aee2a-104">SYNTAX</span></span>

### <span data-ttu-id="aee2a-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aee2a-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aee2a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee2a-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aee2a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aee2a-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aee2a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aee2a-108">DESCRIPTION</span></span>
<span data-ttu-id="aee2a-109">A szignáló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="aee2a-109">Update a SignalR service.</span></span>
<span data-ttu-id="aee2a-110">Ha nem adja meg a paramétereket, a program a következő értékeket fogja használni:</span><span class="sxs-lookup"><span data-stu-id="aee2a-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="aee2a-111">`ResourceGroupName`: az alapértelmezett erőforráscsoport beállítása `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="aee2a-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="aee2a-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="aee2a-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="aee2a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="aee2a-113">EXAMPLES</span></span>

### <span data-ttu-id="aee2a-114">Frissítsen egy adott jelfeldolgozó szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="aee2a-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="aee2a-115">A ServiceMode és a AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="aee2a-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="aee2a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aee2a-116">PARAMETERS</span></span>

### <span data-ttu-id="aee2a-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="aee2a-117">-AllowedOrigin</span></span>
<span data-ttu-id="aee2a-118">A jelző szolgáltatás megengedett eredete.</span><span class="sxs-lookup"><span data-stu-id="aee2a-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="aee2a-119">Az összes engedélyezéséhez használja a "\*" és az összes többi eredetét a listából.</span><span class="sxs-lookup"><span data-stu-id="aee2a-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="aee2a-120">A kivágás nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="aee2a-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="aee2a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aee2a-121">-AsJob</span></span>
<span data-ttu-id="aee2a-122">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="aee2a-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="aee2a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee2a-123">-DefaultProfile</span></span>
<span data-ttu-id="aee2a-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aee2a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee2a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aee2a-125">-InputObject</span></span>
<span data-ttu-id="aee2a-126">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="aee2a-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="aee2a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aee2a-127">-Name</span></span>
<span data-ttu-id="aee2a-128">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="aee2a-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="aee2a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee2a-129">-ResourceGroupName</span></span>
<span data-ttu-id="aee2a-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="aee2a-130">The resource group name.</span></span>
<span data-ttu-id="aee2a-131">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="aee2a-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="aee2a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aee2a-132">-ResourceId</span></span>
<span data-ttu-id="aee2a-133">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aee2a-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee2a-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="aee2a-134">-ServiceMode</span></span>
<span data-ttu-id="aee2a-135">A jeladó szolgáltatás üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="aee2a-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="aee2a-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="aee2a-136">-Sku</span></span>
<span data-ttu-id="aee2a-137">A szignáló szolgáltatás SKU-je.</span><span class="sxs-lookup"><span data-stu-id="aee2a-137">The SignalR service SKU.</span></span>
<span data-ttu-id="aee2a-138">Alapértelmezett érték: "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="aee2a-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="aee2a-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="aee2a-139">-Tag</span></span>
<span data-ttu-id="aee2a-140">A jelző szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="aee2a-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="aee2a-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="aee2a-141">-UnitCount</span></span>
<span data-ttu-id="aee2a-142">A szignáló szolgáltatás egységének értéke csak {1, 2, 5, 10, 20, 50, 100} esetén számítható ki.</span><span class="sxs-lookup"><span data-stu-id="aee2a-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="aee2a-143">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="aee2a-143">Default to 1.</span></span>

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

### <span data-ttu-id="aee2a-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aee2a-144">-Confirm</span></span>
<span data-ttu-id="aee2a-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aee2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee2a-146">-WhatIf</span></span>
<span data-ttu-id="aee2a-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aee2a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee2a-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aee2a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee2a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee2a-149">CommonParameters</span></span>
<span data-ttu-id="aee2a-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aee2a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee2a-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aee2a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee2a-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aee2a-152">INPUTS</span></span>

### <span data-ttu-id="aee2a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="aee2a-153">System.String</span></span>

### <span data-ttu-id="aee2a-154">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="aee2a-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="aee2a-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aee2a-155">OUTPUTS</span></span>

### <span data-ttu-id="aee2a-156">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="aee2a-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="aee2a-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aee2a-157">NOTES</span></span>

## <span data-ttu-id="aee2a-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aee2a-158">RELATED LINKS</span></span>
