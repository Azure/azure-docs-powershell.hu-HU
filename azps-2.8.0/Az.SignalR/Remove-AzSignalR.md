---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 075c8e7604ab800e8f1065ff4d025b105d8effc3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837977"
---
# <span data-ttu-id="c2504-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c2504-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="c2504-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2504-102">SYNOPSIS</span></span>
<span data-ttu-id="c2504-103">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2504-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="c2504-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2504-104">SYNTAX</span></span>

### <span data-ttu-id="c2504-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2504-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2504-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2504-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2504-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2504-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2504-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2504-108">DESCRIPTION</span></span>
<span data-ttu-id="c2504-109">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2504-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="c2504-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c2504-110">EXAMPLES</span></span>

### <span data-ttu-id="c2504-111">Jelfeldolgozó szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2504-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="c2504-112">Az összes szignáló szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="c2504-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="c2504-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2504-113">PARAMETERS</span></span>

### <span data-ttu-id="c2504-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2504-114">-AsJob</span></span>
<span data-ttu-id="c2504-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2504-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2504-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2504-116">-DefaultProfile</span></span>
<span data-ttu-id="c2504-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2504-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2504-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2504-118">-InputObject</span></span>
<span data-ttu-id="c2504-119">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="c2504-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="c2504-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2504-120">-Name</span></span>
<span data-ttu-id="c2504-121">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="c2504-121">SignalR service name.</span></span>

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

### <span data-ttu-id="c2504-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2504-122">-PassThru</span></span>
<span data-ttu-id="c2504-123">Igaz érték visszaadása, ha az Eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="c2504-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="c2504-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2504-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2504-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c2504-125">Resource group name.</span></span>

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

### <span data-ttu-id="c2504-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2504-126">-ResourceId</span></span>
<span data-ttu-id="c2504-127">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c2504-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="c2504-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2504-128">-Confirm</span></span>
<span data-ttu-id="c2504-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2504-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2504-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2504-130">-WhatIf</span></span>
<span data-ttu-id="c2504-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2504-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2504-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2504-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2504-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2504-133">CommonParameters</span></span>
<span data-ttu-id="c2504-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2504-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2504-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c2504-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2504-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2504-136">INPUTS</span></span>

### <span data-ttu-id="c2504-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c2504-137">System.String</span></span>
### <span data-ttu-id="c2504-138">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c2504-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="c2504-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2504-139">OUTPUTS</span></span>

### <span data-ttu-id="c2504-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2504-140">System.Boolean</span></span>
## <span data-ttu-id="c2504-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2504-141">NOTES</span></span>

## <span data-ttu-id="c2504-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2504-142">RELATED LINKS</span></span>
