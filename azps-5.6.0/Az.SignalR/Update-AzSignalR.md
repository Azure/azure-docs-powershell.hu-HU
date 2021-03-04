---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920290"
---
# <span data-ttu-id="d90ae-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d90ae-101">Update-AzSignalR</span></span>

## <span data-ttu-id="d90ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d90ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d90ae-103">Frissítsen egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d90ae-103">Update a SignalR service.</span></span>

## <span data-ttu-id="d90ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d90ae-104">SYNTAX</span></span>

### <span data-ttu-id="d90ae-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d90ae-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d90ae-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d90ae-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d90ae-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d90ae-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d90ae-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d90ae-108">DESCRIPTION</span></span>
<span data-ttu-id="d90ae-109">Frissítsen egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d90ae-109">Update a SignalR service.</span></span>
<span data-ttu-id="d90ae-110">Ha nincs megadva, a paraméterekhez az alábbi értékek használatosak:</span><span class="sxs-lookup"><span data-stu-id="d90ae-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="d90ae-111">`ResourceGroupName`: az alapértelmezett `Set-AzDefault -ResourceGroupName` erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="d90ae-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="d90ae-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="d90ae-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="d90ae-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d90ae-113">EXAMPLES</span></span>

### <span data-ttu-id="d90ae-114">Frissítsen egy adott SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d90ae-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="d90ae-115">A ServiceMode és az AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="d90ae-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="d90ae-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d90ae-116">PARAMETERS</span></span>

### <span data-ttu-id="d90ae-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="d90ae-117">-AllowedOrigin</span></span>
<span data-ttu-id="d90ae-118">A SignalR szolgáltatás engedélyezett forrásai.</span><span class="sxs-lookup"><span data-stu-id="d90ae-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="d90ae-119">Ha az összeset engedélyezni szeretné, használja a "\*" lehetőséget, és távolítsa el az összes többi forrást a listából.</span><span class="sxs-lookup"><span data-stu-id="d90ae-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="d90ae-120">A perjel nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="d90ae-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="d90ae-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d90ae-121">-AsJob</span></span>
<span data-ttu-id="d90ae-122">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="d90ae-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d90ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90ae-123">-DefaultProfile</span></span>
<span data-ttu-id="d90ae-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d90ae-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d90ae-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d90ae-125">-InputObject</span></span>
<span data-ttu-id="d90ae-126">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="d90ae-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d90ae-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d90ae-127">-Name</span></span>
<span data-ttu-id="d90ae-128">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d90ae-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="d90ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="d90ae-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d90ae-130">The resource group name.</span></span>
<span data-ttu-id="d90ae-131">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="d90ae-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="d90ae-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d90ae-132">-ResourceId</span></span>
<span data-ttu-id="d90ae-133">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d90ae-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d90ae-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="d90ae-134">-ServiceMode</span></span>
<span data-ttu-id="d90ae-135">A SignalR szolgáltatás szolgáltatási módja.</span><span class="sxs-lookup"><span data-stu-id="d90ae-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="d90ae-136">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="d90ae-136">-Sku</span></span>
<span data-ttu-id="d90ae-137">A SignalR szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="d90ae-137">The SignalR service SKU.</span></span>
<span data-ttu-id="d90ae-138">Alapértelmezés szerint a "Standard_S1" értéket.</span><span class="sxs-lookup"><span data-stu-id="d90ae-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="d90ae-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d90ae-139">-Tag</span></span>
<span data-ttu-id="d90ae-140">A SignalR szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="d90ae-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="d90ae-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="d90ae-141">-UnitCount</span></span>
<span data-ttu-id="d90ae-142">A SignalR szolgáltatásegységének száma, csak {1, 2, 5, 10, 20, 50, 100} értékből.</span><span class="sxs-lookup"><span data-stu-id="d90ae-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="d90ae-143">Alapértelmezés szerint 1.</span><span class="sxs-lookup"><span data-stu-id="d90ae-143">Default to 1.</span></span>

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

### <span data-ttu-id="d90ae-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d90ae-144">-Confirm</span></span>
<span data-ttu-id="d90ae-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d90ae-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90ae-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90ae-146">-WhatIf</span></span>
<span data-ttu-id="d90ae-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d90ae-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90ae-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d90ae-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90ae-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90ae-149">CommonParameters</span></span>
<span data-ttu-id="d90ae-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90ae-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90ae-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d90ae-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90ae-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d90ae-152">INPUTS</span></span>

### <span data-ttu-id="d90ae-153">System.String</span><span class="sxs-lookup"><span data-stu-id="d90ae-153">System.String</span></span>

### <span data-ttu-id="d90ae-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d90ae-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d90ae-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d90ae-155">OUTPUTS</span></span>

### <span data-ttu-id="d90ae-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d90ae-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d90ae-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d90ae-157">NOTES</span></span>

## <span data-ttu-id="d90ae-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d90ae-158">RELATED LINKS</span></span>
