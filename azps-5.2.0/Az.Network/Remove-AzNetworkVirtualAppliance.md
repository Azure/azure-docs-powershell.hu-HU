---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352986"
---
# <span data-ttu-id="5d84e-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5d84e-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5d84e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d84e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d84e-103">Hálózati virtuális eszköz típusú erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5d84e-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5d84e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d84e-104">SYNTAX</span></span>

### <span data-ttu-id="5d84e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d84e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d84e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d84e-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d84e-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d84e-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d84e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d84e-108">DESCRIPTION</span></span>
<span data-ttu-id="5d84e-109">A Remove-AzNetworkVirtualAppliance parancs eltávolítja a hálózati virtuális eszköz erőforrást.</span><span class="sxs-lookup"><span data-stu-id="5d84e-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5d84e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d84e-110">EXAMPLES</span></span>

### <span data-ttu-id="5d84e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d84e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="5d84e-112">Töröljön egy hálózati virtuális eszköz típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="5d84e-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5d84e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d84e-113">PARAMETERS</span></span>

### <span data-ttu-id="5d84e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d84e-114">-AsJob</span></span>
<span data-ttu-id="5d84e-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5d84e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d84e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d84e-116">-DefaultProfile</span></span>
<span data-ttu-id="5d84e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d84e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d84e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5d84e-118">-Force</span></span>
<span data-ttu-id="5d84e-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d84e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5d84e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5d84e-120">-Name</span></span>
<span data-ttu-id="5d84e-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d84e-121">The resource name.</span></span>

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

### <span data-ttu-id="5d84e-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5d84e-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="5d84e-123">Az erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="5d84e-123">The resource object.</span></span>

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

### <span data-ttu-id="5d84e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d84e-124">-PassThru</span></span>
<span data-ttu-id="5d84e-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5d84e-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5d84e-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5d84e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d84e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d84e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d84e-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d84e-128">The resource group name.</span></span>

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

### <span data-ttu-id="5d84e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d84e-129">-ResourceId</span></span>
<span data-ttu-id="5d84e-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5d84e-130">The Resource Id.</span></span>

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

### <span data-ttu-id="5d84e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d84e-131">-Confirm</span></span>
<span data-ttu-id="5d84e-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d84e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d84e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d84e-133">-WhatIf</span></span>
<span data-ttu-id="5d84e-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d84e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d84e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d84e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d84e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d84e-136">CommonParameters</span></span>
<span data-ttu-id="5d84e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d84e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d84e-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d84e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d84e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d84e-139">INPUTS</span></span>

### <span data-ttu-id="5d84e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5d84e-140">System.String</span></span>

### <span data-ttu-id="5d84e-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5d84e-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5d84e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d84e-142">OUTPUTS</span></span>

### <span data-ttu-id="5d84e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d84e-143">System.Boolean</span></span>

## <span data-ttu-id="5d84e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d84e-144">NOTES</span></span>

## <span data-ttu-id="5d84e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d84e-145">RELATED LINKS</span></span>
