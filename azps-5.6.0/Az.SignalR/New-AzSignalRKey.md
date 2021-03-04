---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: a17f8e6457cc62799fdef3d3606e04962774fdac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920353"
---
# <span data-ttu-id="d61a9-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="d61a9-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="d61a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d61a9-103">A SignalR szolgáltatás hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="d61a9-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d61a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d61a9-104">SYNTAX</span></span>

### <span data-ttu-id="d61a9-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d61a9-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61a9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d61a9-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61a9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d61a9-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d61a9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d61a9-108">DESCRIPTION</span></span>
<span data-ttu-id="d61a9-109">A SignalR szolgáltatás hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="d61a9-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d61a9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d61a9-110">EXAMPLES</span></span>

### <span data-ttu-id="d61a9-111">Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="d61a9-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="d61a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d61a9-112">PARAMETERS</span></span>

### <span data-ttu-id="d61a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61a9-113">-DefaultProfile</span></span>
<span data-ttu-id="d61a9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d61a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d61a9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d61a9-115">-InputObject</span></span>
<span data-ttu-id="d61a9-116">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="d61a9-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d61a9-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d61a9-117">-KeyType</span></span>
<span data-ttu-id="d61a9-118">A kulcs típusa, elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="d61a9-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="d61a9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d61a9-119">-Name</span></span>
<span data-ttu-id="d61a9-120">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d61a9-120">SignalR service name.</span></span>

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

### <span data-ttu-id="d61a9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d61a9-121">-PassThru</span></span>
<span data-ttu-id="d61a9-122">Igaz értéket ad vissza, ha a folyamat sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="d61a9-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="d61a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="d61a9-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d61a9-124">Resource group name.</span></span>

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

### <span data-ttu-id="d61a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d61a9-125">-ResourceId</span></span>
<span data-ttu-id="d61a9-126">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d61a9-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d61a9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d61a9-127">-Confirm</span></span>
<span data-ttu-id="d61a9-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d61a9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d61a9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d61a9-129">-WhatIf</span></span>
<span data-ttu-id="d61a9-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d61a9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d61a9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d61a9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d61a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61a9-132">CommonParameters</span></span>
<span data-ttu-id="d61a9-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61a9-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d61a9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61a9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d61a9-135">INPUTS</span></span>

### <span data-ttu-id="d61a9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d61a9-136">System.String</span></span>
### <span data-ttu-id="d61a9-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d61a9-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="d61a9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d61a9-138">OUTPUTS</span></span>

### <span data-ttu-id="d61a9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d61a9-139">System.Boolean</span></span>
## <span data-ttu-id="d61a9-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d61a9-140">NOTES</span></span>

## <span data-ttu-id="d61a9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d61a9-141">RELATED LINKS</span></span>
