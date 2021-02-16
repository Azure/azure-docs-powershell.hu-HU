---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150643"
---
# <span data-ttu-id="92eea-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="92eea-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="92eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92eea-102">SYNOPSIS</span></span>
<span data-ttu-id="92eea-103">Távolítsa el a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="92eea-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="92eea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92eea-104">SYNTAX</span></span>

### <span data-ttu-id="92eea-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92eea-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92eea-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eea-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92eea-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92eea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92eea-108">DESCRIPTION</span></span>
<span data-ttu-id="92eea-109">Távolítsa el a SignalR-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="92eea-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="92eea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92eea-110">EXAMPLES</span></span>

### <span data-ttu-id="92eea-111">SignalR-szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="92eea-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="92eea-112">Az összes SignalR szolgáltatás eltávolítása a pipe-ból</span><span class="sxs-lookup"><span data-stu-id="92eea-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="92eea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92eea-113">PARAMETERS</span></span>

### <span data-ttu-id="92eea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92eea-114">-AsJob</span></span>
<span data-ttu-id="92eea-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="92eea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92eea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92eea-116">-DefaultProfile</span></span>
<span data-ttu-id="92eea-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92eea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92eea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92eea-118">-InputObject</span></span>
<span data-ttu-id="92eea-119">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="92eea-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="92eea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="92eea-120">-Name</span></span>
<span data-ttu-id="92eea-121">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="92eea-121">SignalR service name.</span></span>

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

### <span data-ttu-id="92eea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92eea-122">-PassThru</span></span>
<span data-ttu-id="92eea-123">Igaz értéket ad vissza, ha az eltávolítás sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="92eea-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="92eea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92eea-124">-ResourceGroupName</span></span>
<span data-ttu-id="92eea-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92eea-125">Resource group name.</span></span>

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

### <span data-ttu-id="92eea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92eea-126">-ResourceId</span></span>
<span data-ttu-id="92eea-127">A SignalR szolgáltatás erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="92eea-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="92eea-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92eea-128">-Confirm</span></span>
<span data-ttu-id="92eea-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92eea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92eea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92eea-130">-WhatIf</span></span>
<span data-ttu-id="92eea-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92eea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92eea-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92eea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92eea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92eea-133">CommonParameters</span></span>
<span data-ttu-id="92eea-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92eea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92eea-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92eea-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92eea-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92eea-136">INPUTS</span></span>

### <span data-ttu-id="92eea-137">System.String</span><span class="sxs-lookup"><span data-stu-id="92eea-137">System.String</span></span>
### <span data-ttu-id="92eea-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="92eea-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="92eea-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92eea-139">OUTPUTS</span></span>

### <span data-ttu-id="92eea-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92eea-140">System.Boolean</span></span>
## <span data-ttu-id="92eea-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92eea-141">NOTES</span></span>

## <span data-ttu-id="92eea-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92eea-142">RELATED LINKS</span></span>
