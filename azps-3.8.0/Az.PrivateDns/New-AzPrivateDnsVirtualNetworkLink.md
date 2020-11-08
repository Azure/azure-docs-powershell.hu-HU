---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013083"
---
# <span data-ttu-id="3d752-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3d752-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="3d752-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d752-102">SYNOPSIS</span></span>
<span data-ttu-id="3d752-103">Új magánhálózati virtuális DNS-hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="3d752-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="3d752-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d752-104">SYNTAX</span></span>

### <span data-ttu-id="3d752-105">VirtualNetworkId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d752-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d752-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3d752-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d752-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d752-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d752-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d752-108">DESCRIPTION</span></span>
<span data-ttu-id="3d752-109">A **New-AzPrivateDnsVirtualNetworkLink** parancsmag új, privát tartománynévrendszer (DNS) virtuális hálózati hivatkozást hoz létre a megadott erőforráscsoport és privát zónában.</span><span class="sxs-lookup"><span data-stu-id="3d752-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="3d752-110">Adjon meg egy egyedi hivatkozás nevét a Name ( *név* ) paraméterhez, vagy a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3d752-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="3d752-111">A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d752-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3d752-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3d752-112">EXAMPLES</span></span>

### <span data-ttu-id="3d752-113">Példa 1: privát DNS virtuális hálózati hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="3d752-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

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

<span data-ttu-id="3d752-114">Ez a parancs létrehoz egy új virtuális hálózati hivatkozást, amely a myzone.com és a virtuális hálózat "myvirtualnetwork" nevű privát DNS-zónával van társítva (amelyet már létrehoztak az erőforráscsoport) a megadott erőforráscsoporthoz, majd a $Link változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d752-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="3d752-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d752-115">PARAMETERS</span></span>

### <span data-ttu-id="3d752-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d752-116">-DefaultProfile</span></span>
<span data-ttu-id="3d752-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d752-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d752-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="3d752-118">-EnableRegistration</span></span>
<span data-ttu-id="3d752-119">Váltás az olyan paraméterre, amely azt jelzi, hogy a hivatkozás engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="3d752-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="3d752-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d752-120">-Name</span></span>
<span data-ttu-id="3d752-121">A létrehozandó virtuális hálózati hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d752-121">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d752-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="3d752-123">Egy másik bérlői virtuális hálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d752-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d752-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d752-125">Azt az erőforráscsoportot adja meg, amelyben létre szeretné hozni a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="3d752-125">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="3d752-126">-Tag</span></span>
<span data-ttu-id="3d752-127">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="3d752-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3d752-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3d752-128">-VirtualNetwork</span></span>
<span data-ttu-id="3d752-129">A hivatkozáshoz társított virtuális hálózat-objektum.</span><span class="sxs-lookup"><span data-stu-id="3d752-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d752-130">-VirtualNetworkId</span></span>
<span data-ttu-id="3d752-131">A hivatkozáshoz társított virtuális hálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d752-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3d752-132">-ZoneName</span></span>
<span data-ttu-id="3d752-133">Annak a zónának a nevét adja meg, amely a virtuális hálózat hivatkozásához fog kapcsolódni.</span><span class="sxs-lookup"><span data-stu-id="3d752-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d752-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d752-134">-Confirm</span></span>
<span data-ttu-id="3d752-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d752-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d752-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d752-136">-WhatIf</span></span>
<span data-ttu-id="3d752-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d752-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d752-138">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d752-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d752-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d752-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d752-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d752-140">CommonParameters</span></span>
<span data-ttu-id="3d752-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d752-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d752-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d752-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d752-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d752-143">INPUTS</span></span>

### <span data-ttu-id="3d752-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d752-144">None</span></span>

## <span data-ttu-id="3d752-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d752-145">OUTPUTS</span></span>

### <span data-ttu-id="3d752-146">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3d752-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="3d752-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d752-147">NOTES</span></span>

## <span data-ttu-id="3d752-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d752-148">RELATED LINKS</span></span>

[<span data-ttu-id="3d752-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3d752-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3d752-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3d752-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3d752-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3d752-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
