---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669093"
---
# <span data-ttu-id="54485-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="54485-101">New-AzSignalR</span></span>

## <span data-ttu-id="54485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54485-102">SYNOPSIS</span></span>
<span data-ttu-id="54485-103">Szignáló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="54485-103">Create a SignalR service.</span></span>

## <span data-ttu-id="54485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54485-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54485-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54485-105">DESCRIPTION</span></span>
<span data-ttu-id="54485-106">Szignáló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="54485-106">Create a SignalR service.</span></span>
<span data-ttu-id="54485-107">Ha nem adja meg a paramétereket, a program a következő értékeket fogja használni:</span><span class="sxs-lookup"><span data-stu-id="54485-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="54485-108">`ResourceGroupName`: az alapértelmezett erőforráscsoport beállítása `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="54485-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="54485-109">`Location`: az erőforráscsoport helye</span><span class="sxs-lookup"><span data-stu-id="54485-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="54485-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="54485-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="54485-111">Példák</span><span class="sxs-lookup"><span data-stu-id="54485-111">EXAMPLES</span></span>

### <span data-ttu-id="54485-112">Jelző szolgáltatás teljesítményszámláló létrehozása</span><span class="sxs-lookup"><span data-stu-id="54485-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="54485-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54485-113">PARAMETERS</span></span>

### <span data-ttu-id="54485-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54485-114">-AsJob</span></span>
<span data-ttu-id="54485-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="54485-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="54485-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54485-116">-DefaultProfile</span></span>
<span data-ttu-id="54485-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54485-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54485-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="54485-118">-Location</span></span>
<span data-ttu-id="54485-119">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="54485-119">The SignalR service location.</span></span> <span data-ttu-id="54485-120">A program az erőforráscsoport helyét használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="54485-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="54485-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54485-121">-Name</span></span>
<span data-ttu-id="54485-122">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="54485-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="54485-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54485-123">-ResourceGroupName</span></span>
<span data-ttu-id="54485-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="54485-124">The resource group name.</span></span> <span data-ttu-id="54485-125">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="54485-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="54485-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="54485-126">-Sku</span></span>
<span data-ttu-id="54485-127">A szignáló szolgáltatás SKU-je.</span><span class="sxs-lookup"><span data-stu-id="54485-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="54485-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="54485-128">-Tag</span></span>
<span data-ttu-id="54485-129">A jelző szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="54485-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="54485-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="54485-130">-UnitCount</span></span>
<span data-ttu-id="54485-131">A szignáló szolgáltatás egységének száma 1-től 10-ig.</span><span class="sxs-lookup"><span data-stu-id="54485-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="54485-132">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="54485-132">Default to 1.</span></span>

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

### <span data-ttu-id="54485-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54485-133">-Confirm</span></span>
<span data-ttu-id="54485-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54485-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54485-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54485-135">-WhatIf</span></span>
<span data-ttu-id="54485-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54485-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54485-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54485-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54485-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54485-138">CommonParameters</span></span>
<span data-ttu-id="54485-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54485-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54485-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54485-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54485-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54485-141">INPUTS</span></span>

### <span data-ttu-id="54485-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="54485-142">None</span></span>

## <span data-ttu-id="54485-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54485-143">OUTPUTS</span></span>

### <span data-ttu-id="54485-144">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="54485-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="54485-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54485-145">NOTES</span></span>

## <span data-ttu-id="54485-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54485-146">RELATED LINKS</span></span>
