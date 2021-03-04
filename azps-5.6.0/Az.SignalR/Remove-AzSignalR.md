---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920346"
---
# <span data-ttu-id="b3a19-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="b3a19-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="b3a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a19-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a19-103">Távolítsa el a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b3a19-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="b3a19-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3a19-104">SYNTAX</span></span>

### <span data-ttu-id="b3a19-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3a19-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a19-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a19-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a19-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a19-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a19-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3a19-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a19-109">Távolítsa el a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b3a19-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="b3a19-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3a19-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a19-111">SignalR-szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b3a19-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="b3a19-112">Az összes SignalR szolgáltatás eltávolítása a pipe-ból</span><span class="sxs-lookup"><span data-stu-id="b3a19-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="b3a19-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a19-113">PARAMETERS</span></span>

### <span data-ttu-id="b3a19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3a19-114">-AsJob</span></span>
<span data-ttu-id="b3a19-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b3a19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3a19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a19-116">-DefaultProfile</span></span>
<span data-ttu-id="b3a19-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3a19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a19-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a19-118">-InputObject</span></span>
<span data-ttu-id="b3a19-119">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="b3a19-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b3a19-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b3a19-120">-Name</span></span>
<span data-ttu-id="b3a19-121">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="b3a19-121">SignalR service name.</span></span>

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

### <span data-ttu-id="b3a19-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3a19-122">-PassThru</span></span>
<span data-ttu-id="b3a19-123">Igaz értéket ad vissza, ha az eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="b3a19-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="b3a19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a19-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3a19-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b3a19-125">Resource group name.</span></span>

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

### <span data-ttu-id="b3a19-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a19-126">-ResourceId</span></span>
<span data-ttu-id="b3a19-127">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3a19-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b3a19-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3a19-128">-Confirm</span></span>
<span data-ttu-id="b3a19-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3a19-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a19-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a19-130">-WhatIf</span></span>
<span data-ttu-id="b3a19-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3a19-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a19-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3a19-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a19-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a19-133">CommonParameters</span></span>
<span data-ttu-id="b3a19-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a19-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a19-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a19-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a19-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a19-136">INPUTS</span></span>

### <span data-ttu-id="b3a19-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b3a19-137">System.String</span></span>
### <span data-ttu-id="b3a19-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b3a19-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="b3a19-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3a19-139">OUTPUTS</span></span>

### <span data-ttu-id="b3a19-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3a19-140">System.Boolean</span></span>
## <span data-ttu-id="b3a19-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3a19-141">NOTES</span></span>

## <span data-ttu-id="b3a19-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3a19-142">RELATED LINKS</span></span>
