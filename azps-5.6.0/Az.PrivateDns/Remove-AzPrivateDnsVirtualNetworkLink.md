---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925393"
---
# <span data-ttu-id="51356-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="51356-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="51356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51356-102">SYNOPSIS</span></span>
<span data-ttu-id="51356-103">Eltávolít egy virtuális hálózati hivatkozást egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="51356-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="51356-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51356-104">SYNTAX</span></span>

### <span data-ttu-id="51356-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51356-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51356-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="51356-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51356-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="51356-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51356-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51356-108">DESCRIPTION</span></span>
<span data-ttu-id="51356-109">A **Remove-AzPrivateDnsVirtualNetworkLink** parancsmag véglegesen töröl egy privát DNS-hivatkozást egy adott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="51356-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="51356-110">A **PSPrivateDnsVirtualNetworkLink** objektum a  Csatolás paraméterrel vagy a folyamat műveleti jelével adható át, vagy másik lehetőségként megadhatja a *Name* *ZoneName* és *az ResourceGroupName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="51356-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="51356-111">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="51356-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="51356-112">Ha **PSPrivateDnsVirtualNetworkLink** objektummal adja meg a hivatkozást  (amely a folyamaton vagy a Link paraméteren keresztül lett átadva), a csatolás nem törlődik, ha az Azure Private DNS-ben módosult a helyi **PSPrivateDnsVirtualNetworkLink** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="51356-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="51356-113">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="51356-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="51356-114">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="51356-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="51356-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51356-115">EXAMPLES</span></span>

### <span data-ttu-id="51356-116">1. példa: Hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51356-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="51356-117">Ez a parancs eltávolítja a MyResourceGroup nevű erőforráscsoportból a mylink myzone.com csatolt hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="51356-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="51356-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51356-118">PARAMETERS</span></span>

### <span data-ttu-id="51356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51356-119">-DefaultProfile</span></span>
<span data-ttu-id="51356-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="51356-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51356-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51356-121">-InputObject</span></span>
<span data-ttu-id="51356-122">Az eltávolítható virtuális hálózati csatolási objektum.</span><span class="sxs-lookup"><span data-stu-id="51356-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51356-123">-Name</span><span class="sxs-lookup"><span data-stu-id="51356-123">-Name</span></span>
<span data-ttu-id="51356-124">A törölnie kell hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51356-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="51356-125">Az *ResourceGroupName* és *a ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="51356-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="51356-126">Másik lehetőségként a Csatolás paramétert használva is *megadhatja a* hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="51356-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51356-127">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="51356-127">-Overwrite</span></span>
<span data-ttu-id="51356-128">Amikor a zónát **PSPrivateDnsVirtualNetworkLink** objektummal adja meg  (a folyamaton vagy a Csatolás paraméteren keresztül adja át), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **PSPrivateDnsVirtualNetworkLink** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="51356-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="51356-129">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="51356-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="51356-130">Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="51356-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51356-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51356-131">-PassThru</span></span>
<span data-ttu-id="51356-132">A művelet eredményének (logikai) végrehajtásához használható, amely törli a virtuális hálózati kapcsolatot a folyamaton belül tovább.</span><span class="sxs-lookup"><span data-stu-id="51356-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="51356-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51356-133">-ResourceGroupName</span></span>
<span data-ttu-id="51356-134">Annak az erőforráscsoportnak a nevét adja meg, amely az eltávolítható hivatkozást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="51356-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="51356-135">A *ZoneName* és a *Name paramétert is meg kell* adnia.</span><span class="sxs-lookup"><span data-stu-id="51356-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="51356-136">Másik lehetőségként megadhatja a DNS-zónát egy **PSPrivateDnsVirtualNetworkLink** objektummal, amely a folyamaton vagy a Csatolás paraméteren keresztül *áthalad.*</span><span class="sxs-lookup"><span data-stu-id="51356-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51356-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51356-137">-ResourceId</span></span>
<span data-ttu-id="51356-138">A ARM erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="51356-138">Specifies the ARM resource ID of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51356-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="51356-139">-ZoneName</span></span>
<span data-ttu-id="51356-140">Annak a privát DNS-zónának a neve, amelyhez a hivatkozás társítva van.</span><span class="sxs-lookup"><span data-stu-id="51356-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="51356-141">Az *ResourceGroupName* és a *Name paramétert is meg kell* adnia.</span><span class="sxs-lookup"><span data-stu-id="51356-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="51356-142">Másik lehetőségként a Csatolás paramétert használva is *megadhatja a* hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="51356-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51356-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51356-143">-Confirm</span></span>
<span data-ttu-id="51356-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="51356-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51356-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51356-145">-WhatIf</span></span>
<span data-ttu-id="51356-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="51356-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51356-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51356-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51356-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51356-148">CommonParameters</span></span>
<span data-ttu-id="51356-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51356-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51356-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51356-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51356-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51356-151">INPUTS</span></span>

### <span data-ttu-id="51356-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="51356-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="51356-153">System.String</span><span class="sxs-lookup"><span data-stu-id="51356-153">System.String</span></span>

## <span data-ttu-id="51356-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51356-154">OUTPUTS</span></span>

### <span data-ttu-id="51356-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51356-155">System.Boolean</span></span>

## <span data-ttu-id="51356-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51356-156">NOTES</span></span>

## <span data-ttu-id="51356-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51356-157">RELATED LINKS</span></span>

[<span data-ttu-id="51356-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="51356-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="51356-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="51356-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="51356-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="51356-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
