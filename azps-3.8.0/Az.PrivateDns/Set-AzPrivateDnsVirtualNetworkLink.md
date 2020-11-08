---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011003"
---
# <span data-ttu-id="5604c-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5604c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5604c-102">SYNOPSIS</span></span>
<span data-ttu-id="5604c-103">Frissítések/virtuális hálózati kapcsolat bekapcsolása egy privát zónával és egy erőforrás-csoporthoz társítva.</span><span class="sxs-lookup"><span data-stu-id="5604c-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="5604c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5604c-104">SYNTAX</span></span>

### <span data-ttu-id="5604c-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5604c-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5604c-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="5604c-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5604c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5604c-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5604c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5604c-108">DESCRIPTION</span></span>
<span data-ttu-id="5604c-109">A **set-AzPrivateDnsVirtualNetworkLink** parancsmag frissíti a megadott erőforráscsoport zónájával társított hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5604c-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="5604c-110">A **PSPrivateDnsVirtualNetworkLink** -objektumokat átadhatja a *hivatkozás* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja *a* *ZoneName* és a *ResourceGroupName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5604c-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5604c-111">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5604c-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5604c-112">Ha a zónát egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a pipeline vagy a *hivatkozás* paraméterrel átadva) adja meg, a hivatkozás nem frissül, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5604c-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="5604c-113">Ez védelmet nyújt az egyidejű kapcsolatok változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5604c-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="5604c-114">Ezt a *felülírási* paraméter segítségével lehet letiltani, amely a hivatkozásokat az egyidejű módosításoktól függetlenül frissíti.</span><span class="sxs-lookup"><span data-stu-id="5604c-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="5604c-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5604c-115">EXAMPLES</span></span>

### <span data-ttu-id="5604c-116">Példa 1: hivatkozás beállítása</span><span class="sxs-lookup"><span data-stu-id="5604c-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="5604c-117">Ez a parancs beállítja a IsRegistrationEnabled a mylink nevű hivatkozáshoz a MyResourceGroup nevű erőforráscsoport myzone.com nevű zónájához társítva.</span><span class="sxs-lookup"><span data-stu-id="5604c-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5604c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5604c-118">PARAMETERS</span></span>

### <span data-ttu-id="5604c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5604c-119">-DefaultProfile</span></span>
<span data-ttu-id="5604c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5604c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5604c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5604c-121">-InputObject</span></span>
<span data-ttu-id="5604c-122">A beállítani kívánt virtuális hálózati kapcsolat objektum.</span><span class="sxs-lookup"><span data-stu-id="5604c-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="5604c-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="5604c-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="5604c-124">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a regisztráció a virtuális hálózaton hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="5604c-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5604c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5604c-125">-Name</span></span>
<span data-ttu-id="5604c-126">Annak a hivatkozásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5604c-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="5604c-127">Meg kell adnia a *ResourceGroupName* és a *ZoneName* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5604c-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="5604c-128">Azt is megteheti, hogy a *hivatkozás* paraméterrel megadhatja a magánhálózati DNS-hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5604c-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="5604c-129">-Átír</span><span class="sxs-lookup"><span data-stu-id="5604c-129">-Overwrite</span></span>
<span data-ttu-id="5604c-130">Ha a hivatkozást egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a csővezetéken vagy a *hivatkozás* paraméteren keresztül átadva) adja meg, a hivatkozás nem törlődik, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="5604c-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="5604c-131">Ez védelmet nyújt az egyidejű kapcsolatok változásaihoz.</span><span class="sxs-lookup"><span data-stu-id="5604c-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="5604c-132">Ezt a *felülírási* paraméter használatával lehet letiltani, amely a hivatkozásokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="5604c-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5604c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5604c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5604c-134">Az eltávolítandó hivatkozást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5604c-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="5604c-135">Meg kell adnia a *ZoneName* és a *Name* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="5604c-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="5604c-136">Azt is megteheti, hogy megadhatja a virtuális hálózati hivatkozást egy **PSPrivateDnsVirtualNetworkLink** objektummal, amelyet a csővezetéken vagy a *hivatkozás* paraméteren keresztül adott meg.</span><span class="sxs-lookup"><span data-stu-id="5604c-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="5604c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5604c-137">-ResourceId</span></span>
<span data-ttu-id="5604c-138">Privát DNS-zóna ResourceID.</span><span class="sxs-lookup"><span data-stu-id="5604c-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="5604c-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="5604c-139">-Tag</span></span>
<span data-ttu-id="5604c-140">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="5604c-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5604c-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5604c-141">-ZoneName</span></span>
<span data-ttu-id="5604c-142">A parancsmag által eltávolított DNS-zóna nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5604c-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="5604c-143">A *Name* és a *ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="5604c-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="5604c-144">Azt is megteheti, hogy a *hivatkozás* paraméterrel megadhatja a magánhálózati DNS-hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5604c-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="5604c-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5604c-145">-Confirm</span></span>
<span data-ttu-id="5604c-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5604c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5604c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5604c-147">-WhatIf</span></span>
<span data-ttu-id="5604c-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5604c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5604c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5604c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5604c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5604c-150">CommonParameters</span></span>
<span data-ttu-id="5604c-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5604c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5604c-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5604c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5604c-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5604c-153">INPUTS</span></span>

### <span data-ttu-id="5604c-154">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="5604c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="5604c-155">System.String</span></span>

## <span data-ttu-id="5604c-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5604c-156">OUTPUTS</span></span>

### <span data-ttu-id="5604c-157">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5604c-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5604c-158">NOTES</span></span>

## <span data-ttu-id="5604c-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5604c-159">RELATED LINKS</span></span>

[<span data-ttu-id="5604c-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5604c-161">Új – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5604c-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5604c-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
