---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156259"
---
# <span data-ttu-id="4d3a1-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="4d3a1-101">New-AzSignalR</span></span>

## <span data-ttu-id="4d3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3a1-103">Hozzon létre egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-103">Create a SignalR service.</span></span>

## <span data-ttu-id="4d3a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d3a1-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3a1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="4d3a1-106">Hozzon létre egy SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-106">Create a SignalR service.</span></span>
<span data-ttu-id="4d3a1-107">Ha nincs megadva, a paraméterekhez az alábbi értékek használatosak:</span><span class="sxs-lookup"><span data-stu-id="4d3a1-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="4d3a1-108">`ResourceGroupName`: az alapértelmezett `Set-AzDefault -ResourceGroupName` erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="4d3a1-109">`Location`: az erőforráscsoport helye</span><span class="sxs-lookup"><span data-stu-id="4d3a1-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="4d3a1-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="4d3a1-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="4d3a1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d3a1-111">EXAMPLES</span></span>

### <span data-ttu-id="4d3a1-112">SignalR szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d3a1-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="4d3a1-113">A ServiceMode és az AllowedOrigin megadása</span><span class="sxs-lookup"><span data-stu-id="4d3a1-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="4d3a1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d3a1-114">PARAMETERS</span></span>

### <span data-ttu-id="4d3a1-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="4d3a1-115">-AllowedOrigin</span></span>
<span data-ttu-id="4d3a1-116">A SignalR szolgáltatás engedélyezett forrásai.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="4d3a1-117">Ha az összeset engedélyezni szeretné, használja a "\*" lehetőséget, és távolítsa el az összes többi forrást a listából.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="4d3a1-118">A perjel nem használható a tartomány részeként vagy a TLD után</span><span class="sxs-lookup"><span data-stu-id="4d3a1-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="4d3a1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d3a1-119">-AsJob</span></span>
<span data-ttu-id="4d3a1-120">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="4d3a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3a1-121">-DefaultProfile</span></span>
<span data-ttu-id="4d3a1-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d3a1-123">-Location</span><span class="sxs-lookup"><span data-stu-id="4d3a1-123">-Location</span></span>
<span data-ttu-id="4d3a1-124">A SignalR szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-124">The SignalR service location.</span></span> <span data-ttu-id="4d3a1-125">Ha nincs megadva, az erőforráscsoport helye lesz használatban.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="4d3a1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4d3a1-126">-Name</span></span>
<span data-ttu-id="4d3a1-127">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="4d3a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d3a1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-129">The resource group name.</span></span> <span data-ttu-id="4d3a1-130">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="4d3a1-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="4d3a1-131">-ServiceMode</span></span>
<span data-ttu-id="4d3a1-132">A SignalR szolgáltatás szolgáltatási módja.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="4d3a1-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="4d3a1-133">-Sku</span></span>
<span data-ttu-id="4d3a1-134">A SignalR szolgáltatás termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="4d3a1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d3a1-135">-Tag</span></span>
<span data-ttu-id="4d3a1-136">A SignalR szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="4d3a1-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="4d3a1-137">-UnitCount</span></span>
<span data-ttu-id="4d3a1-138">A SignalR szolgáltatásegység száma 1 és 10 között.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="4d3a1-139">Alapértelmezés szerint 1.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-139">Default to 1.</span></span>

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

### <span data-ttu-id="4d3a1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d3a1-140">-Confirm</span></span>
<span data-ttu-id="4d3a1-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d3a1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3a1-142">-WhatIf</span></span>
<span data-ttu-id="4d3a1-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3a1-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d3a1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3a1-145">CommonParameters</span></span>
<span data-ttu-id="4d3a1-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3a1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3a1-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d3a1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3a1-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d3a1-148">INPUTS</span></span>

### <span data-ttu-id="4d3a1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4d3a1-149">System.String</span></span>

## <span data-ttu-id="4d3a1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d3a1-150">OUTPUTS</span></span>

### <span data-ttu-id="4d3a1-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4d3a1-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="4d3a1-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d3a1-152">NOTES</span></span>

## <span data-ttu-id="4d3a1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d3a1-153">RELATED LINKS</span></span>
