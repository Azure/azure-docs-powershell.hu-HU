---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838658"
---
# <span data-ttu-id="5db74-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5db74-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5db74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5db74-102">SYNOPSIS</span></span>
<span data-ttu-id="5db74-103">A virtuális hálózati hivatkozás eltávolítása egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="5db74-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="5db74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5db74-104">SYNTAX</span></span>

### <span data-ttu-id="5db74-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5db74-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db74-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="5db74-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db74-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5db74-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db74-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5db74-108">DESCRIPTION</span></span>
<span data-ttu-id="5db74-109">A **Remove-AzPrivateDnsVirtualNetworkLink** parancsmag véglegesen törli a privát tartománynévrendszer (DNS) hivatkozását egy adott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="5db74-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="5db74-110">A **PSPrivateDnsVirtualNetworkLink** -objektumokat átadhatja a *hivatkozás* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja *a* *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5db74-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5db74-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5db74-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5db74-112">Ha a hivatkozást egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a csővezetéken vagy a *hivatkozás* paraméteren keresztül átadva) adja meg, a hivatkozás nem törlődik, ha az Azure Private DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5db74-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="5db74-113">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5db74-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="5db74-114">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="5db74-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5db74-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5db74-115">EXAMPLES</span></span>

### <span data-ttu-id="5db74-116">Példa 1: hivatkozás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5db74-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="5db74-117">Ez a parancs eltávolítja a MyResourceGroup nevű erőforráscsoport mylink csatolt myzone.com nevű hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5db74-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5db74-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5db74-118">PARAMETERS</span></span>

### <span data-ttu-id="5db74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db74-119">-DefaultProfile</span></span>
<span data-ttu-id="5db74-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5db74-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5db74-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db74-121">-InputObject</span></span>
<span data-ttu-id="5db74-122">A virtuális hálózati kapcsolat objektum eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5db74-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="5db74-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5db74-123">-Name</span></span>
<span data-ttu-id="5db74-124">A törlendő hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5db74-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="5db74-125">Meg kell adnia a *ResourceGroupName* és a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5db74-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="5db74-126">Másik lehetőségként *a hivatkozás paramétert* használva is megadhatja a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5db74-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="5db74-127">-Átír</span><span class="sxs-lookup"><span data-stu-id="5db74-127">-Overwrite</span></span>
<span data-ttu-id="5db74-128">Ha a zónát egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a pipeline vagy a *hivatkozás* paraméterrel átadva) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5db74-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="5db74-129">Ez védelmet nyújt a zónák egyidejű változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5db74-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5db74-130">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.</span><span class="sxs-lookup"><span data-stu-id="5db74-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5db74-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5db74-131">-PassThru</span></span>
<span data-ttu-id="5db74-132">A művelet eredményének (logikai) elvégzéséhez használható a virtuális hálózat törlése hivatkozás a csővezetéken lejjebb.</span><span class="sxs-lookup"><span data-stu-id="5db74-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="5db74-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db74-133">-ResourceGroupName</span></span>
<span data-ttu-id="5db74-134">Az eltávolítandó hivatkozást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5db74-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="5db74-135">Meg kell adnia a *ZoneName* és a *Name* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5db74-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="5db74-136">Azt is megteheti, hogy megadhatja a DNS-zónát egy **PSPrivateDnsVirtualNetworkLink** objektummal, amelyet a csővezetéken vagy a *hivatkozás* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="5db74-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="5db74-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5db74-137">-ResourceId</span></span>
<span data-ttu-id="5db74-138">A hivatkozás ARM erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5db74-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="5db74-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5db74-139">-ZoneName</span></span>
<span data-ttu-id="5db74-140">Annak a magánhálózati DNS-zónának a neve, amelyhez a hivatkozás társítva van.</span><span class="sxs-lookup"><span data-stu-id="5db74-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="5db74-141">Meg kell adnia a *ResourceGroupName* és a *Name* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5db74-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="5db74-142">Másik lehetőségként *a hivatkozás paramétert* használva is megadhatja a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5db74-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="5db74-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5db74-143">-Confirm</span></span>
<span data-ttu-id="5db74-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5db74-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db74-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db74-145">-WhatIf</span></span>
<span data-ttu-id="5db74-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5db74-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db74-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5db74-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db74-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db74-148">CommonParameters</span></span>
<span data-ttu-id="5db74-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5db74-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db74-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db74-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db74-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5db74-151">INPUTS</span></span>

### <span data-ttu-id="5db74-152">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5db74-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="5db74-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5db74-153">System.String</span></span>

## <span data-ttu-id="5db74-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5db74-154">OUTPUTS</span></span>

### <span data-ttu-id="5db74-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5db74-155">System.Boolean</span></span>

## <span data-ttu-id="5db74-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5db74-156">NOTES</span></span>

## <span data-ttu-id="5db74-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5db74-157">RELATED LINKS</span></span>

[<span data-ttu-id="5db74-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5db74-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5db74-159">Új – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5db74-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5db74-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5db74-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
