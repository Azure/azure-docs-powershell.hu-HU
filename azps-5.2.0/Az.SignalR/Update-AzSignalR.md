---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329093"
---
# <span data-ttu-id="00304-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="00304-101">Update-AzSignalR</span></span>

## <span data-ttu-id="00304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00304-102">SYNOPSIS</span></span>
<span data-ttu-id="00304-103">Frissítsen egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="00304-103">Update a SignalR service.</span></span>

## <span data-ttu-id="00304-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00304-104">SYNTAX</span></span>

### <span data-ttu-id="00304-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00304-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00304-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00304-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00304-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00304-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00304-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00304-108">DESCRIPTION</span></span>
<span data-ttu-id="00304-109">Frissítsen egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="00304-109">Update a SignalR service.</span></span>
<span data-ttu-id="00304-110">Ha nincs megadva, a paraméterekhez az alábbi értékek használatosak:</span><span class="sxs-lookup"><span data-stu-id="00304-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="00304-111">`ResourceGroupName`: az alapértelmezett `Set-AzDefault -ResourceGroupName` erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="00304-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="00304-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="00304-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="00304-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00304-113">EXAMPLES</span></span>

### <span data-ttu-id="00304-114">Frissítsen egy adott SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="00304-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="00304-115">A ServiceMode és az AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="00304-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="00304-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00304-116">PARAMETERS</span></span>

### <span data-ttu-id="00304-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="00304-117">-AllowedOrigin</span></span>
<span data-ttu-id="00304-118">A SignalR szolgáltatás engedélyezett forrásai.</span><span class="sxs-lookup"><span data-stu-id="00304-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="00304-119">Ha az összeset engedélyezni szeretné, használja a "\*" lehetőséget, és távolítsa el az összes többi forrást a listából.</span><span class="sxs-lookup"><span data-stu-id="00304-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="00304-120">A perjel nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="00304-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="00304-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00304-121">-AsJob</span></span>
<span data-ttu-id="00304-122">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="00304-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="00304-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00304-123">-DefaultProfile</span></span>
<span data-ttu-id="00304-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00304-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00304-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00304-125">-InputObject</span></span>
<span data-ttu-id="00304-126">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="00304-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="00304-127">-Name</span><span class="sxs-lookup"><span data-stu-id="00304-127">-Name</span></span>
<span data-ttu-id="00304-128">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="00304-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="00304-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00304-129">-ResourceGroupName</span></span>
<span data-ttu-id="00304-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00304-130">The resource group name.</span></span>
<span data-ttu-id="00304-131">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="00304-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="00304-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00304-132">-ResourceId</span></span>
<span data-ttu-id="00304-133">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00304-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="00304-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="00304-134">-ServiceMode</span></span>
<span data-ttu-id="00304-135">A SignalR szolgáltatás szolgáltatási módja.</span><span class="sxs-lookup"><span data-stu-id="00304-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="00304-136">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="00304-136">-Sku</span></span>
<span data-ttu-id="00304-137">A SignalR szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="00304-137">The SignalR service SKU.</span></span>
<span data-ttu-id="00304-138">Alapértelmezés szerint a "Standard_S1" értéket.</span><span class="sxs-lookup"><span data-stu-id="00304-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="00304-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="00304-139">-Tag</span></span>
<span data-ttu-id="00304-140">A SignalR szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="00304-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="00304-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="00304-141">-UnitCount</span></span>
<span data-ttu-id="00304-142">A SignalR szolgáltatásegységének száma, csak {1, 2, 5, 10, 20, 50, 100} értékből.</span><span class="sxs-lookup"><span data-stu-id="00304-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="00304-143">Alapértelmezés szerint 1.</span><span class="sxs-lookup"><span data-stu-id="00304-143">Default to 1.</span></span>

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

### <span data-ttu-id="00304-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00304-144">-Confirm</span></span>
<span data-ttu-id="00304-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00304-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00304-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00304-146">-WhatIf</span></span>
<span data-ttu-id="00304-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00304-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00304-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00304-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00304-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00304-149">CommonParameters</span></span>
<span data-ttu-id="00304-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00304-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00304-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00304-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00304-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00304-152">INPUTS</span></span>

### <span data-ttu-id="00304-153">System.String</span><span class="sxs-lookup"><span data-stu-id="00304-153">System.String</span></span>

### <span data-ttu-id="00304-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="00304-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="00304-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00304-155">OUTPUTS</span></span>

### <span data-ttu-id="00304-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="00304-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="00304-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00304-157">NOTES</span></span>

## <span data-ttu-id="00304-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00304-158">RELATED LINKS</span></span>
