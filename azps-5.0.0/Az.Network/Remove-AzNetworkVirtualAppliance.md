---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186884"
---
# <span data-ttu-id="51457-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="51457-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="51457-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51457-102">SYNOPSIS</span></span>
<span data-ttu-id="51457-103">Hálózati virtuális készülék erőforrásának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="51457-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="51457-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51457-104">SYNTAX</span></span>

### <span data-ttu-id="51457-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51457-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51457-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51457-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51457-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51457-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51457-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="51457-108">DESCRIPTION</span></span>
<span data-ttu-id="51457-109">A Remove-AzNetworkVirtualAppliance parancs eltávolítja a hálózat virtuális Appliance-erőforrását.</span><span class="sxs-lookup"><span data-stu-id="51457-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="51457-110">Példák</span><span class="sxs-lookup"><span data-stu-id="51457-110">EXAMPLES</span></span>

### <span data-ttu-id="51457-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51457-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="51457-112">A hálózat virtuális készülékhez tartozó erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="51457-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="51457-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51457-113">PARAMETERS</span></span>

### <span data-ttu-id="51457-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51457-114">-AsJob</span></span>
<span data-ttu-id="51457-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="51457-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51457-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51457-116">-DefaultProfile</span></span>
<span data-ttu-id="51457-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51457-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51457-118">-Force</span><span class="sxs-lookup"><span data-stu-id="51457-118">-Force</span></span>
<span data-ttu-id="51457-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51457-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="51457-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51457-120">-Name</span></span>
<span data-ttu-id="51457-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="51457-121">The resource name.</span></span>

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

### <span data-ttu-id="51457-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="51457-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="51457-123">Az erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="51457-123">The resource object.</span></span>

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

### <span data-ttu-id="51457-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51457-124">-PassThru</span></span>
<span data-ttu-id="51457-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="51457-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="51457-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="51457-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51457-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51457-127">-ResourceGroupName</span></span>
<span data-ttu-id="51457-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="51457-128">The resource group name.</span></span>

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

### <span data-ttu-id="51457-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51457-129">-ResourceId</span></span>
<span data-ttu-id="51457-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="51457-130">The Resource Id.</span></span>

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

### <span data-ttu-id="51457-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51457-131">-Confirm</span></span>
<span data-ttu-id="51457-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51457-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51457-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51457-133">-WhatIf</span></span>
<span data-ttu-id="51457-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51457-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51457-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51457-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51457-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51457-136">CommonParameters</span></span>
<span data-ttu-id="51457-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51457-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51457-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51457-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51457-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51457-139">INPUTS</span></span>

### <span data-ttu-id="51457-140">System. String</span><span class="sxs-lookup"><span data-stu-id="51457-140">System.String</span></span>

### <span data-ttu-id="51457-141">Microsoft. Azure. commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="51457-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="51457-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51457-142">OUTPUTS</span></span>

### <span data-ttu-id="51457-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51457-143">System.Boolean</span></span>

## <span data-ttu-id="51457-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51457-144">NOTES</span></span>

## <span data-ttu-id="51457-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51457-145">RELATED LINKS</span></span>
