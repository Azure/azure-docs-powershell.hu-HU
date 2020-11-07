---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 4bb121563c0fe7a635caeffe982502bff3468495
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838749"
---
# <span data-ttu-id="b8213-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="b8213-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="b8213-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8213-102">SYNOPSIS</span></span>
<span data-ttu-id="b8213-103">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b8213-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b8213-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8213-104">SYNTAX</span></span>

### <span data-ttu-id="b8213-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8213-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8213-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8213-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8213-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8213-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8213-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8213-108">DESCRIPTION</span></span>
<span data-ttu-id="b8213-109">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b8213-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="b8213-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b8213-110">EXAMPLES</span></span>

### <span data-ttu-id="b8213-111">Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="b8213-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="b8213-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8213-112">PARAMETERS</span></span>

### <span data-ttu-id="b8213-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8213-113">-DefaultProfile</span></span>
<span data-ttu-id="b8213-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8213-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8213-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8213-115">-InputObject</span></span>
<span data-ttu-id="b8213-116">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="b8213-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b8213-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="b8213-117">-KeyType</span></span>
<span data-ttu-id="b8213-118">A kulcs típusa elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="b8213-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="b8213-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8213-119">-Name</span></span>
<span data-ttu-id="b8213-120">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="b8213-120">SignalR service name.</span></span>

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

### <span data-ttu-id="b8213-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8213-121">-PassThru</span></span>
<span data-ttu-id="b8213-122">Igaz érték visszaadása, ha a regeneráció sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="b8213-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="b8213-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8213-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8213-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b8213-124">Resource group name.</span></span>

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

### <span data-ttu-id="b8213-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8213-125">-ResourceId</span></span>
<span data-ttu-id="b8213-126">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b8213-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b8213-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8213-127">-Confirm</span></span>
<span data-ttu-id="b8213-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8213-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8213-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8213-129">-WhatIf</span></span>
<span data-ttu-id="b8213-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8213-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8213-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8213-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8213-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8213-132">CommonParameters</span></span>
<span data-ttu-id="b8213-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8213-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8213-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8213-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8213-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8213-135">INPUTS</span></span>

### <span data-ttu-id="b8213-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b8213-136">System.String</span></span>
### <span data-ttu-id="b8213-137">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b8213-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="b8213-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8213-138">OUTPUTS</span></span>

### <span data-ttu-id="b8213-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8213-139">System.Boolean</span></span>
## <span data-ttu-id="b8213-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8213-140">NOTES</span></span>

## <span data-ttu-id="b8213-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8213-141">RELATED LINKS</span></span>
