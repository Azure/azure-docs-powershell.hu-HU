---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011287"
---
# <span data-ttu-id="f95ad-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="f95ad-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="f95ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f95ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f95ad-103">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f95ad-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f95ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f95ad-104">SYNTAX</span></span>

### <span data-ttu-id="f95ad-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f95ad-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f95ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95ad-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f95ad-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95ad-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95ad-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f95ad-108">DESCRIPTION</span></span>
<span data-ttu-id="f95ad-109">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f95ad-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f95ad-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f95ad-110">EXAMPLES</span></span>

### <span data-ttu-id="f95ad-111">Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f95ad-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="f95ad-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f95ad-112">PARAMETERS</span></span>

### <span data-ttu-id="f95ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95ad-113">-DefaultProfile</span></span>
<span data-ttu-id="f95ad-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f95ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95ad-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f95ad-115">-InputObject</span></span>
<span data-ttu-id="f95ad-116">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="f95ad-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f95ad-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="f95ad-117">-KeyType</span></span>
<span data-ttu-id="f95ad-118">A kulcs típusa elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="f95ad-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95ad-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f95ad-119">-Name</span></span>
<span data-ttu-id="f95ad-120">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f95ad-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f95ad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f95ad-121">-PassThru</span></span>
<span data-ttu-id="f95ad-122">Igaz érték visszaadása, ha a regeneráció sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="f95ad-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="f95ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="f95ad-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f95ad-124">Resource group name.</span></span>

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

### <span data-ttu-id="f95ad-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f95ad-125">-ResourceId</span></span>
<span data-ttu-id="f95ad-126">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f95ad-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f95ad-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f95ad-127">-Confirm</span></span>
<span data-ttu-id="f95ad-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f95ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95ad-129">-WhatIf</span></span>
<span data-ttu-id="f95ad-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f95ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95ad-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f95ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95ad-132">CommonParameters</span></span>
<span data-ttu-id="f95ad-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f95ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95ad-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f95ad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95ad-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95ad-135">INPUTS</span></span>

### <span data-ttu-id="f95ad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f95ad-136">System.String</span></span>
### <span data-ttu-id="f95ad-137">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f95ad-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="f95ad-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95ad-138">OUTPUTS</span></span>

### <span data-ttu-id="f95ad-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f95ad-139">System.Boolean</span></span>
## <span data-ttu-id="f95ad-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f95ad-140">NOTES</span></span>

## <span data-ttu-id="f95ad-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f95ad-141">RELATED LINKS</span></span>
