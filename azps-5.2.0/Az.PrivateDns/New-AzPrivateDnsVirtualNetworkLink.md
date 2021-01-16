---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343806"
---
# <span data-ttu-id="5973b-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5973b-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5973b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5973b-102">SYNOPSIS</span></span>
<span data-ttu-id="5973b-103">Létrehoz egy új virtuális DNS-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="5973b-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="5973b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5973b-104">SYNTAX</span></span>

### <span data-ttu-id="5973b-105">VirtualNetworkId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5973b-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5973b-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5973b-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5973b-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5973b-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5973b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5973b-108">DESCRIPTION</span></span>
<span data-ttu-id="5973b-109">A **New-AzPrivateDnsVirtualNetworkLink** parancsmag létrehoz egy új dns-virtuális hálózati kapcsolatot a megadott erőforráscsoportban és a privát zónában.</span><span class="sxs-lookup"><span data-stu-id="5973b-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="5973b-110">Meg kell adnia egy egyedi hivatkozásnevet a *Name* paraméternek, különben a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="5973b-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="5973b-111">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="5973b-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5973b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5973b-112">EXAMPLES</span></span>

### <span data-ttu-id="5973b-113">1. példa: Virtuális DNS-kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="5973b-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="5973b-114">Ez a parancs létrehoz egy új virtuális hálózati hivatkozást a myzone.com nevű privát DNS-zónához és a "myvirtualnetwork" virtuális hálózathoz (amely már létrejött az erőforráscsoportban) a megadott erőforráscsoportban, majd a $Link változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5973b-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="5973b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5973b-115">PARAMETERS</span></span>

### <span data-ttu-id="5973b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5973b-116">-DefaultProfile</span></span>
<span data-ttu-id="5973b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5973b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5973b-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="5973b-118">-EnableRegistration</span></span>
<span data-ttu-id="5973b-119">Switch parameter that represents if the link is registration enabled or not.</span><span class="sxs-lookup"><span data-stu-id="5973b-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="5973b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5973b-120">-Name</span></span>
<span data-ttu-id="5973b-121">A létrehozni szükséges virtuális hálózati hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5973b-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="5973b-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5973b-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5973b-123">Egy másik bérlő virtuális hálózatának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5973b-123">The resource id of the virtual network in another tenant.</span></span>

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

### <span data-ttu-id="5973b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5973b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5973b-125">Megadja azt az erőforráscsoportot, amelyben létre kell hoznia a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="5973b-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="5973b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5973b-126">-Tag</span></span>
<span data-ttu-id="5973b-127">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="5973b-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5973b-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5973b-128">-VirtualNetwork</span></span>
<span data-ttu-id="5973b-129">A csatolással társított virtuális hálózati objektum.</span><span class="sxs-lookup"><span data-stu-id="5973b-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="5973b-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5973b-130">-VirtualNetworkId</span></span>
<span data-ttu-id="5973b-131">A csatolással társított virtuális hálózat erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5973b-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="5973b-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5973b-132">-ZoneName</span></span>
<span data-ttu-id="5973b-133">Megadja annak a zónának a nevét, amely a virtuális hálózati kapcsolathoz lesz csatolva.</span><span class="sxs-lookup"><span data-stu-id="5973b-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="5973b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5973b-134">-Confirm</span></span>
<span data-ttu-id="5973b-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5973b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5973b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5973b-136">-WhatIf</span></span>
<span data-ttu-id="5973b-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5973b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5973b-138">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5973b-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5973b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5973b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5973b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5973b-140">CommonParameters</span></span>
<span data-ttu-id="5973b-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5973b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5973b-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5973b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5973b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5973b-143">INPUTS</span></span>

### <span data-ttu-id="5973b-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="5973b-144">None</span></span>

## <span data-ttu-id="5973b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5973b-145">OUTPUTS</span></span>

### <span data-ttu-id="5973b-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5973b-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5973b-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5973b-147">NOTES</span></span>

## <span data-ttu-id="5973b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5973b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5973b-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5973b-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5973b-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5973b-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5973b-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5973b-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
