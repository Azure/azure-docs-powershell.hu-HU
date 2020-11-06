---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497280"
---
# <span data-ttu-id="c71d0-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="c71d0-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="c71d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c71d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c71d0-103">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c71d0-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c71d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c71d0-104">SYNTAX</span></span>

### <span data-ttu-id="c71d0-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c71d0-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c71d0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c71d0-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c71d0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c71d0-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c71d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c71d0-108">DESCRIPTION</span></span>
<span data-ttu-id="c71d0-109">Az Access-kulcs újragenerálása a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c71d0-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="c71d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c71d0-110">EXAMPLES</span></span>

### <span data-ttu-id="c71d0-111">Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="c71d0-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="c71d0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c71d0-112">PARAMETERS</span></span>

### <span data-ttu-id="c71d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71d0-113">-DefaultProfile</span></span>
<span data-ttu-id="c71d0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c71d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71d0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c71d0-115">-InputObject</span></span>
<span data-ttu-id="c71d0-116">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="c71d0-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="c71d0-117">-Típus</span><span class="sxs-lookup"><span data-stu-id="c71d0-117">-KeyType</span></span>
<span data-ttu-id="c71d0-118">A kulcs típusa elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="c71d0-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="c71d0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c71d0-119">-Name</span></span>
<span data-ttu-id="c71d0-120">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="c71d0-120">SignalR service name.</span></span>

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

### <span data-ttu-id="c71d0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c71d0-121">-PassThru</span></span>
<span data-ttu-id="c71d0-122">Igaz érték visszaadása, ha a regeneráció sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="c71d0-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="c71d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c71d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c71d0-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c71d0-124">Resource group name.</span></span>

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

### <span data-ttu-id="c71d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c71d0-125">-ResourceId</span></span>
<span data-ttu-id="c71d0-126">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c71d0-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="c71d0-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c71d0-127">-Confirm</span></span>
<span data-ttu-id="c71d0-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c71d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71d0-129">-WhatIf</span></span>
<span data-ttu-id="c71d0-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c71d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c71d0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c71d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71d0-132">CommonParameters</span></span>
<span data-ttu-id="c71d0-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c71d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71d0-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c71d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71d0-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c71d0-135">INPUTS</span></span>

### <span data-ttu-id="c71d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c71d0-136">System.String</span></span>
<span data-ttu-id="c71d0-137">Paraméterek: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c71d0-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="c71d0-138">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c71d0-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="c71d0-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c71d0-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c71d0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c71d0-140">OUTPUTS</span></span>

### <span data-ttu-id="c71d0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c71d0-141">System.Boolean</span></span>

## <span data-ttu-id="c71d0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c71d0-142">NOTES</span></span>

## <span data-ttu-id="c71d0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c71d0-143">RELATED LINKS</span></span>
