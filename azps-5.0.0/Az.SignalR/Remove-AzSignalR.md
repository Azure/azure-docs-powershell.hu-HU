---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187528"
---
# <span data-ttu-id="36d4b-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="36d4b-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="36d4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="36d4b-103">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36d4b-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="36d4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36d4b-104">SYNTAX</span></span>

### <span data-ttu-id="36d4b-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36d4b-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d4b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d4b-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d4b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d4b-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="36d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="36d4b-109">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36d4b-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="36d4b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="36d4b-110">EXAMPLES</span></span>

### <span data-ttu-id="36d4b-111">Jelfeldolgozó szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36d4b-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="36d4b-112">Az összes szignáló szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="36d4b-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="36d4b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36d4b-113">PARAMETERS</span></span>

### <span data-ttu-id="36d4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36d4b-114">-AsJob</span></span>
<span data-ttu-id="36d4b-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36d4b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d4b-116">-DefaultProfile</span></span>
<span data-ttu-id="36d4b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36d4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d4b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d4b-118">-InputObject</span></span>
<span data-ttu-id="36d4b-119">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="36d4b-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="36d4b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36d4b-120">-Name</span></span>
<span data-ttu-id="36d4b-121">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="36d4b-121">SignalR service name.</span></span>

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

### <span data-ttu-id="36d4b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d4b-122">-PassThru</span></span>
<span data-ttu-id="36d4b-123">Igaz érték visszaadása, ha az Eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="36d4b-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="36d4b-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="36d4b-125">Resource group name.</span></span>

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

### <span data-ttu-id="36d4b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d4b-126">-ResourceId</span></span>
<span data-ttu-id="36d4b-127">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36d4b-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="36d4b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36d4b-128">-Confirm</span></span>
<span data-ttu-id="36d4b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36d4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d4b-130">-WhatIf</span></span>
<span data-ttu-id="36d4b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36d4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d4b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36d4b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d4b-133">CommonParameters</span></span>
<span data-ttu-id="36d4b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36d4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d4b-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36d4b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d4b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d4b-136">INPUTS</span></span>

### <span data-ttu-id="36d4b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="36d4b-137">System.String</span></span>
### <span data-ttu-id="36d4b-138">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="36d4b-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="36d4b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d4b-139">OUTPUTS</span></span>

### <span data-ttu-id="36d4b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36d4b-140">System.Boolean</span></span>
## <span data-ttu-id="36d4b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36d4b-141">NOTES</span></span>

## <span data-ttu-id="36d4b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36d4b-142">RELATED LINKS</span></span>
