---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181384"
---
# <span data-ttu-id="d27a4-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d27a4-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="d27a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d27a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d27a4-103">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d27a4-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="d27a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d27a4-104">SYNTAX</span></span>

### <span data-ttu-id="d27a4-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d27a4-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d27a4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d27a4-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d27a4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d27a4-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d27a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d27a4-108">DESCRIPTION</span></span>
<span data-ttu-id="d27a4-109">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d27a4-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="d27a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d27a4-110">EXAMPLES</span></span>

### <span data-ttu-id="d27a4-111">Jelfeldolgozó szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d27a4-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="d27a4-112">Az összes szignáló szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="d27a4-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="d27a4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d27a4-113">PARAMETERS</span></span>

### <span data-ttu-id="d27a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d27a4-114">-AsJob</span></span>
<span data-ttu-id="d27a4-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d27a4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d27a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27a4-116">-DefaultProfile</span></span>
<span data-ttu-id="d27a4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d27a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d27a4-118">-InputObject</span></span>
<span data-ttu-id="d27a4-119">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="d27a4-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d27a4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d27a4-120">-Name</span></span>
<span data-ttu-id="d27a4-121">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d27a4-121">SignalR service name.</span></span>

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

### <span data-ttu-id="d27a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d27a4-122">-PassThru</span></span>
<span data-ttu-id="d27a4-123">Igaz érték visszaadása, ha az Eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="d27a4-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="d27a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="d27a4-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d27a4-125">Resource group name.</span></span>

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

### <span data-ttu-id="d27a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d27a4-126">-ResourceId</span></span>
<span data-ttu-id="d27a4-127">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d27a4-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d27a4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d27a4-128">-Confirm</span></span>
<span data-ttu-id="d27a4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d27a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d27a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d27a4-130">-WhatIf</span></span>
<span data-ttu-id="d27a4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d27a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27a4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d27a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d27a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27a4-133">CommonParameters</span></span>
<span data-ttu-id="d27a4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d27a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27a4-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d27a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27a4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27a4-136">INPUTS</span></span>

### <span data-ttu-id="d27a4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d27a4-137">System.String</span></span>
### <span data-ttu-id="d27a4-138">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d27a4-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="d27a4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27a4-139">OUTPUTS</span></span>

### <span data-ttu-id="d27a4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d27a4-140">System.Boolean</span></span>
## <span data-ttu-id="d27a4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d27a4-141">NOTES</span></span>

## <span data-ttu-id="d27a4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d27a4-142">RELATED LINKS</span></span>
