---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3aea2414a4b7fdfbc14e65d4d087bb7e31206aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838674"
---
# <span data-ttu-id="4ece8-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4ece8-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4ece8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ece8-102">SYNOPSIS</span></span>
<span data-ttu-id="4ece8-103">A megadott privát DNS-zónához társított virtuális hálózati hivatkozás kap.</span><span class="sxs-lookup"><span data-stu-id="4ece8-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="4ece8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ece8-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ece8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ece8-105">DESCRIPTION</span></span>
<span data-ttu-id="4ece8-106">A **Get-AzPrivateDnsVirtualNetworkLink** parancsmag virtuális hálózati hivatkozásokat kap, amelyek egy adott privát DNS-zónához kapcsolódnak a megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4ece8-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="4ece8-107">Ha a *Name* paramétert adja meg, a program egyetlen **PSPrivateDnsVirtualNetworkLink** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4ece8-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="4ece8-108">Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport zónájával társított összes hivatkozást tartalmazó tömböt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4ece8-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="4ece8-109">A hivatkozás frissítéséhez használhatja a **PSPrivateDnsVirtualNetworkLink** objektumot.</span><span class="sxs-lookup"><span data-stu-id="4ece8-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="4ece8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4ece8-110">EXAMPLES</span></span>

### <span data-ttu-id="4ece8-111">Példa 1: virtuális hálózati hivatkozás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4ece8-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="4ece8-112">Ebben a példában a myzone.com nevű privát DNS-zónához társított virtuális hálózati kapcsolat mylink a megadott erőforráscsoport, majd a $Link változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ece8-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="4ece8-113">2. példa: az erőforráscsoport egy zónájához társított összes hivatkozás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4ece8-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="4ece8-114">Ez a példa a megadott erőforráscsoport "myzone.com" privát DNS-zónájával társított virtuális hálózati hivatkozásokat kapja meg, majd a $Links változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ece8-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="4ece8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ece8-115">PARAMETERS</span></span>

### <span data-ttu-id="4ece8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ece8-116">-DefaultProfile</span></span>
<span data-ttu-id="4ece8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ece8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ece8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ece8-118">-Name</span></span>
<span data-ttu-id="4ece8-119">Annak a virtuális hálózati hivatkozásnak a neve, amelyből beolvasható.</span><span class="sxs-lookup"><span data-stu-id="4ece8-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="4ece8-120">Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoporthoz tartozó személyes DNS-zónához tartozó összes hivatkozást megkapja.</span><span class="sxs-lookup"><span data-stu-id="4ece8-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ece8-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ece8-122">Annak a csoportnak a neve, amely a virtuális hálózat hivatkozását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4ece8-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="4ece8-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="4ece8-123">-ZoneName</span></span>
<span data-ttu-id="4ece8-124">Annak a magánhálózati DNS-zónának a neve, amelyhez a virtuális hálózat hivatkozás van társítva.</span><span class="sxs-lookup"><span data-stu-id="4ece8-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="4ece8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ece8-125">CommonParameters</span></span>
<span data-ttu-id="4ece8-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ece8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ece8-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ece8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ece8-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ece8-128">INPUTS</span></span>

### <span data-ttu-id="4ece8-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ece8-129">None</span></span>

## <span data-ttu-id="4ece8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ece8-130">OUTPUTS</span></span>

### <span data-ttu-id="4ece8-131">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4ece8-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4ece8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ece8-132">NOTES</span></span>

## <span data-ttu-id="4ece8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ece8-133">RELATED LINKS</span></span>

[<span data-ttu-id="4ece8-134">Új – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4ece8-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4ece8-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4ece8-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4ece8-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4ece8-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
