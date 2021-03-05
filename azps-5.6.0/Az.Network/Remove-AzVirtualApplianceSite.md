---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006118"
---
# <span data-ttu-id="8265b-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8265b-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="8265b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8265b-102">SYNOPSIS</span></span>
<span data-ttu-id="8265b-103">Távolítson el egy virtuális berendezés-webhelyet egy hálózati virtuális eszköz típusú erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="8265b-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8265b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8265b-104">SYNTAX</span></span>

### <span data-ttu-id="8265b-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8265b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8265b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8265b-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8265b-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8265b-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8265b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8265b-108">DESCRIPTION</span></span>
<span data-ttu-id="8265b-109">A Remove-AzVirtualApplianceSite parancs eltávolítja a virtuális eszköz webhelyét egy hálózati virtuális eszköz típusú erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="8265b-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8265b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8265b-110">EXAMPLES</span></span>

### <span data-ttu-id="8265b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8265b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="8265b-112">Virtuális eszköz webhelyerőforrás törlése.</span><span class="sxs-lookup"><span data-stu-id="8265b-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="8265b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8265b-113">PARAMETERS</span></span>

### <span data-ttu-id="8265b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8265b-114">-AsJob</span></span>
<span data-ttu-id="8265b-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8265b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8265b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8265b-116">-DefaultProfile</span></span>
<span data-ttu-id="8265b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8265b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8265b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8265b-118">-Force</span></span>
<span data-ttu-id="8265b-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8265b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8265b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8265b-120">-Name</span></span>
<span data-ttu-id="8265b-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8265b-121">The resource name.</span></span>

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

### <span data-ttu-id="8265b-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="8265b-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="8265b-123">A webhelyhez társított hálózati virtuális eszköz erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8265b-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="8265b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8265b-124">-PassThru</span></span>
<span data-ttu-id="8265b-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8265b-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8265b-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8265b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8265b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8265b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8265b-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8265b-128">The resource group name.</span></span>

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

### <span data-ttu-id="8265b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8265b-129">-ResourceId</span></span>
<span data-ttu-id="8265b-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8265b-130">The resource id.</span></span>

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

### <span data-ttu-id="8265b-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8265b-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="8265b-132">A virtuális gép webhelyobjektuma.</span><span class="sxs-lookup"><span data-stu-id="8265b-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="8265b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8265b-133">-Confirm</span></span>
<span data-ttu-id="8265b-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8265b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8265b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8265b-135">-WhatIf</span></span>
<span data-ttu-id="8265b-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8265b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8265b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8265b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8265b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8265b-138">CommonParameters</span></span>
<span data-ttu-id="8265b-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8265b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8265b-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8265b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8265b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8265b-141">INPUTS</span></span>

### <span data-ttu-id="8265b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8265b-142">System.String</span></span>

### <span data-ttu-id="8265b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8265b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="8265b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8265b-144">OUTPUTS</span></span>

### <span data-ttu-id="8265b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8265b-145">System.Boolean</span></span>

## <span data-ttu-id="8265b-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8265b-146">NOTES</span></span>

## <span data-ttu-id="8265b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8265b-147">RELATED LINKS</span></span>
