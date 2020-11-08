---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024587"
---
# <span data-ttu-id="b9a36-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="b9a36-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="b9a36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9a36-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a36-103">Virtuális készülék webhelyének eltávolítása egy hálózati virtuális készülék-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="b9a36-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b9a36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9a36-104">SYNTAX</span></span>

### <span data-ttu-id="b9a36-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9a36-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9a36-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a36-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a36-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a36-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a36-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9a36-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a36-109">A Remove-AzVirtualApplianceSite parancs eltávolítja a virtuális készülék webhelyét egy hálózati virtuális készülék-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="b9a36-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b9a36-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9a36-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a36-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9a36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="b9a36-112">A virtuális Appliance-webhely erőforrásainak törlése</span><span class="sxs-lookup"><span data-stu-id="b9a36-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="b9a36-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9a36-113">PARAMETERS</span></span>

### <span data-ttu-id="b9a36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9a36-114">-AsJob</span></span>
<span data-ttu-id="b9a36-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9a36-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9a36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a36-116">-DefaultProfile</span></span>
<span data-ttu-id="b9a36-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9a36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a36-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b9a36-118">-Force</span></span>
<span data-ttu-id="b9a36-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9a36-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9a36-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9a36-120">-Name</span></span>
<span data-ttu-id="b9a36-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b9a36-121">The resource name.</span></span>

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

### <span data-ttu-id="b9a36-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="b9a36-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="b9a36-123">A webhellyel társított hálózati virtuális készülék erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9a36-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="b9a36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9a36-124">-PassThru</span></span>
<span data-ttu-id="b9a36-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b9a36-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b9a36-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b9a36-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9a36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a36-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9a36-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9a36-128">The resource group name.</span></span>

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

### <span data-ttu-id="b9a36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a36-129">-ResourceId</span></span>
<span data-ttu-id="b9a36-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b9a36-130">The resource id.</span></span>

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

### <span data-ttu-id="b9a36-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="b9a36-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="b9a36-132">A virtuális gép webhely objektuma.</span><span class="sxs-lookup"><span data-stu-id="b9a36-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="b9a36-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9a36-133">-Confirm</span></span>
<span data-ttu-id="b9a36-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9a36-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a36-135">-WhatIf</span></span>
<span data-ttu-id="b9a36-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9a36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a36-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9a36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a36-138">CommonParameters</span></span>
<span data-ttu-id="b9a36-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9a36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a36-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9a36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a36-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9a36-141">INPUTS</span></span>

### <span data-ttu-id="b9a36-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a36-142">System.String</span></span>

### <span data-ttu-id="b9a36-143">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="b9a36-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="b9a36-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9a36-144">OUTPUTS</span></span>

### <span data-ttu-id="b9a36-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9a36-145">System.Boolean</span></span>

## <span data-ttu-id="b9a36-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9a36-146">NOTES</span></span>

## <span data-ttu-id="b9a36-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9a36-147">RELATED LINKS</span></span>
