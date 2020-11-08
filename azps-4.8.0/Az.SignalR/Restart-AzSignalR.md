---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180850"
---
# <span data-ttu-id="6c156-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6c156-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="6c156-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c156-102">SYNOPSIS</span></span>
<span data-ttu-id="6c156-103">Indítsa újra a szignáló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="6c156-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="6c156-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c156-104">SYNTAX</span></span>

### <span data-ttu-id="6c156-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c156-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c156-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c156-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c156-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c156-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c156-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c156-108">DESCRIPTION</span></span>
<span data-ttu-id="6c156-109">Indítsa újra a szignáló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="6c156-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="6c156-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6c156-110">EXAMPLES</span></span>

### <span data-ttu-id="6c156-111">Adott jelfeldolgozó szolgáltatás újraindítása</span><span class="sxs-lookup"><span data-stu-id="6c156-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="6c156-112">Az alapértelmezett erőforráscsoport beállítása: \` set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="6c156-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="6c156-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c156-113">PARAMETERS</span></span>

### <span data-ttu-id="6c156-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c156-114">-AsJob</span></span>
<span data-ttu-id="6c156-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="6c156-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="6c156-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c156-116">-DefaultProfile</span></span>
<span data-ttu-id="6c156-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c156-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c156-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c156-118">-InputObject</span></span>
<span data-ttu-id="6c156-119">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="6c156-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="6c156-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c156-120">-Name</span></span>
<span data-ttu-id="6c156-121">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6c156-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="6c156-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c156-122">-PassThru</span></span>
<span data-ttu-id="6c156-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6c156-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6c156-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c156-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c156-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c156-125">The resource group name.</span></span>
<span data-ttu-id="6c156-126">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6c156-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="6c156-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c156-127">-ResourceId</span></span>
<span data-ttu-id="6c156-128">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6c156-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6c156-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c156-129">-Confirm</span></span>
<span data-ttu-id="6c156-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c156-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c156-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c156-131">-WhatIf</span></span>
<span data-ttu-id="6c156-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c156-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c156-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c156-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c156-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c156-134">CommonParameters</span></span>
<span data-ttu-id="6c156-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c156-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c156-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6c156-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c156-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c156-137">INPUTS</span></span>

### <span data-ttu-id="6c156-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6c156-138">System.String</span></span>

### <span data-ttu-id="6c156-139">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6c156-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6c156-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c156-140">OUTPUTS</span></span>

### <span data-ttu-id="6c156-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c156-141">System.Boolean</span></span>

## <span data-ttu-id="6c156-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c156-142">NOTES</span></span>

## <span data-ttu-id="6c156-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c156-143">RELATED LINKS</span></span>
