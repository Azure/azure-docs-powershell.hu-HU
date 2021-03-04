---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941570"
---
# <span data-ttu-id="be573-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="be573-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="be573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be573-102">SYNOPSIS</span></span>
<span data-ttu-id="be573-103">Hálózati virtuális eszköz típusú erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="be573-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="be573-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be573-104">SYNTAX</span></span>

### <span data-ttu-id="be573-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be573-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be573-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be573-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be573-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be573-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be573-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be573-108">DESCRIPTION</span></span>
<span data-ttu-id="be573-109">A Remove-AzNetworkVirtualAppliance parancs eltávolítja a hálózati virtuális eszköz erőforrást.</span><span class="sxs-lookup"><span data-stu-id="be573-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="be573-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be573-110">EXAMPLES</span></span>

### <span data-ttu-id="be573-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="be573-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="be573-112">Töröljön egy hálózati virtuális eszköz típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="be573-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="be573-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be573-113">PARAMETERS</span></span>

### <span data-ttu-id="be573-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be573-114">-AsJob</span></span>
<span data-ttu-id="be573-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="be573-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be573-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be573-116">-DefaultProfile</span></span>
<span data-ttu-id="be573-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be573-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be573-118">-Force</span><span class="sxs-lookup"><span data-stu-id="be573-118">-Force</span></span>
<span data-ttu-id="be573-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be573-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="be573-120">-Name</span><span class="sxs-lookup"><span data-stu-id="be573-120">-Name</span></span>
<span data-ttu-id="be573-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="be573-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be573-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="be573-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="be573-123">Az erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="be573-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be573-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be573-124">-PassThru</span></span>
<span data-ttu-id="be573-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="be573-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="be573-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="be573-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be573-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be573-127">-ResourceGroupName</span></span>
<span data-ttu-id="be573-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be573-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be573-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be573-129">-ResourceId</span></span>
<span data-ttu-id="be573-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="be573-130">The Resource Id.</span></span>

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

### <span data-ttu-id="be573-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be573-131">-Confirm</span></span>
<span data-ttu-id="be573-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="be573-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be573-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be573-133">-WhatIf</span></span>
<span data-ttu-id="be573-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="be573-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be573-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be573-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be573-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be573-136">CommonParameters</span></span>
<span data-ttu-id="be573-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be573-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be573-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be573-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be573-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be573-139">INPUTS</span></span>

### <span data-ttu-id="be573-140">System.String</span><span class="sxs-lookup"><span data-stu-id="be573-140">System.String</span></span>

### <span data-ttu-id="be573-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="be573-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="be573-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be573-142">OUTPUTS</span></span>

### <span data-ttu-id="be573-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be573-143">System.Boolean</span></span>

## <span data-ttu-id="be573-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be573-144">NOTES</span></span>

## <span data-ttu-id="be573-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be573-145">RELATED LINKS</span></span>
