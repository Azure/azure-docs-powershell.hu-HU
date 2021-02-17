---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165034"
---
# <span data-ttu-id="2eb55-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="2eb55-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="2eb55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb55-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb55-103">A SignalR szolgáltatás hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="2eb55-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="2eb55-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2eb55-104">SYNTAX</span></span>

### <span data-ttu-id="2eb55-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eb55-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb55-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eb55-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb55-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eb55-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb55-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2eb55-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb55-109">A SignalR szolgáltatás hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="2eb55-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="2eb55-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2eb55-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb55-111">Az elsődleges kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="2eb55-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="2eb55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb55-112">PARAMETERS</span></span>

### <span data-ttu-id="2eb55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb55-113">-DefaultProfile</span></span>
<span data-ttu-id="2eb55-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eb55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb55-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb55-115">-InputObject</span></span>
<span data-ttu-id="2eb55-116">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="2eb55-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="2eb55-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2eb55-117">-KeyType</span></span>
<span data-ttu-id="2eb55-118">A kulcs típusa, elsődleges vagy másodlagos.</span><span class="sxs-lookup"><span data-stu-id="2eb55-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="2eb55-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb55-119">-Name</span></span>
<span data-ttu-id="2eb55-120">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="2eb55-120">SignalR service name.</span></span>

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

### <span data-ttu-id="2eb55-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eb55-121">-PassThru</span></span>
<span data-ttu-id="2eb55-122">Igaz értéket ad vissza, ha a folyamat sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="2eb55-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="2eb55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb55-123">-ResourceGroupName</span></span>
<span data-ttu-id="2eb55-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2eb55-124">Resource group name.</span></span>

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

### <span data-ttu-id="2eb55-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb55-125">-ResourceId</span></span>
<span data-ttu-id="2eb55-126">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2eb55-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2eb55-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb55-127">-Confirm</span></span>
<span data-ttu-id="2eb55-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2eb55-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb55-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb55-129">-WhatIf</span></span>
<span data-ttu-id="2eb55-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2eb55-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb55-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2eb55-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb55-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb55-132">CommonParameters</span></span>
<span data-ttu-id="2eb55-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb55-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb55-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eb55-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb55-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eb55-135">INPUTS</span></span>

### <span data-ttu-id="2eb55-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2eb55-136">System.String</span></span>
### <span data-ttu-id="2eb55-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="2eb55-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="2eb55-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eb55-138">OUTPUTS</span></span>

### <span data-ttu-id="2eb55-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eb55-139">System.Boolean</span></span>
## <span data-ttu-id="2eb55-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2eb55-140">NOTES</span></span>

## <span data-ttu-id="2eb55-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eb55-141">RELATED LINKS</span></span>
