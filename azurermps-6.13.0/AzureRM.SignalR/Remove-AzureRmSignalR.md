---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497276"
---
# <span data-ttu-id="f48d7-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="f48d7-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="f48d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f48d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f48d7-103">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f48d7-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f48d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f48d7-104">SYNTAX</span></span>

### <span data-ttu-id="f48d7-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f48d7-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48d7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48d7-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48d7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48d7-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48d7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f48d7-108">DESCRIPTION</span></span>
<span data-ttu-id="f48d7-109">A jelző szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f48d7-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="f48d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f48d7-110">EXAMPLES</span></span>

### <span data-ttu-id="f48d7-111">Jelfeldolgozó szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f48d7-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="f48d7-112">Az összes szignáló szolgáltatás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="f48d7-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="f48d7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f48d7-113">PARAMETERS</span></span>

### <span data-ttu-id="f48d7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f48d7-114">-AsJob</span></span>
<span data-ttu-id="f48d7-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f48d7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f48d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48d7-116">-DefaultProfile</span></span>
<span data-ttu-id="f48d7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f48d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f48d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f48d7-118">-InputObject</span></span>
<span data-ttu-id="f48d7-119">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="f48d7-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f48d7-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f48d7-120">-Name</span></span>
<span data-ttu-id="f48d7-121">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f48d7-121">SignalR service name.</span></span>

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

### <span data-ttu-id="f48d7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f48d7-122">-PassThru</span></span>
<span data-ttu-id="f48d7-123">Igaz érték visszaadása, ha az Eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="f48d7-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="f48d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="f48d7-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f48d7-125">Resource group name.</span></span>

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

### <span data-ttu-id="f48d7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48d7-126">-ResourceId</span></span>
<span data-ttu-id="f48d7-127">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f48d7-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f48d7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f48d7-128">-Confirm</span></span>
<span data-ttu-id="f48d7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f48d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48d7-130">-WhatIf</span></span>
<span data-ttu-id="f48d7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f48d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f48d7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f48d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48d7-133">CommonParameters</span></span>
<span data-ttu-id="f48d7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f48d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48d7-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48d7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48d7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f48d7-136">INPUTS</span></span>

### <span data-ttu-id="f48d7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f48d7-137">System.String</span></span>
<span data-ttu-id="f48d7-138">Paraméterek: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f48d7-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="f48d7-139">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f48d7-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="f48d7-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f48d7-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f48d7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f48d7-141">OUTPUTS</span></span>

### <span data-ttu-id="f48d7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f48d7-142">System.Boolean</span></span>

## <span data-ttu-id="f48d7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f48d7-143">NOTES</span></span>

## <span data-ttu-id="f48d7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f48d7-144">RELATED LINKS</span></span>
