---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195340"
---
# <span data-ttu-id="a9aa1-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a9aa1-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a9aa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9aa1-103">Virtuális készülék webhelyének eltávolítása egy hálózati virtuális készülék-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a9aa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9aa1-104">SYNTAX</span></span>

### <span data-ttu-id="a9aa1-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9aa1-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9aa1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9aa1-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9aa1-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9aa1-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9aa1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9aa1-108">DESCRIPTION</span></span>
<span data-ttu-id="a9aa1-109">A Remove-AzVirtualApplianceSite parancs eltávolítja a virtuális készülék webhelyét egy hálózati virtuális készülék-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a9aa1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a9aa1-110">EXAMPLES</span></span>

### <span data-ttu-id="a9aa1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9aa1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="a9aa1-112">A virtuális Appliance-webhely erőforrásainak törlése</span><span class="sxs-lookup"><span data-stu-id="a9aa1-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="a9aa1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9aa1-113">PARAMETERS</span></span>

### <span data-ttu-id="a9aa1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9aa1-114">-AsJob</span></span>
<span data-ttu-id="a9aa1-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a9aa1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9aa1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9aa1-116">-DefaultProfile</span></span>
<span data-ttu-id="a9aa1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9aa1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a9aa1-118">-Force</span></span>
<span data-ttu-id="a9aa1-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a9aa1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9aa1-120">-Name</span></span>
<span data-ttu-id="a9aa1-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-121">The resource name.</span></span>

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

### <span data-ttu-id="a9aa1-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a9aa1-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a9aa1-123">A webhellyel társított hálózati virtuális készülék erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="a9aa1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9aa1-124">-PassThru</span></span>
<span data-ttu-id="a9aa1-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a9aa1-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9aa1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9aa1-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9aa1-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-128">The resource group name.</span></span>

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

### <span data-ttu-id="a9aa1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9aa1-129">-ResourceId</span></span>
<span data-ttu-id="a9aa1-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-130">The resource id.</span></span>

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

### <span data-ttu-id="a9aa1-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a9aa1-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="a9aa1-132">A virtuális gép webhely objektuma.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9aa1-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9aa1-133">-Confirm</span></span>
<span data-ttu-id="a9aa1-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9aa1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9aa1-135">-WhatIf</span></span>
<span data-ttu-id="a9aa1-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9aa1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9aa1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9aa1-138">CommonParameters</span></span>
<span data-ttu-id="a9aa1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9aa1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9aa1-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9aa1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9aa1-141">INPUTS</span></span>

### <span data-ttu-id="a9aa1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a9aa1-142">System.String</span></span>

### <span data-ttu-id="a9aa1-143">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a9aa1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a9aa1-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9aa1-144">OUTPUTS</span></span>

### <span data-ttu-id="a9aa1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9aa1-145">System.Boolean</span></span>

## <span data-ttu-id="a9aa1-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9aa1-146">NOTES</span></span>

## <span data-ttu-id="a9aa1-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9aa1-147">RELATED LINKS</span></span>
