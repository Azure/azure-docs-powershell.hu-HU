---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369765"
---
# <span data-ttu-id="d878b-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d878b-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d878b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d878b-102">SYNOPSIS</span></span>
<span data-ttu-id="d878b-103">A megadott privát DNS-zónához társított virtuális hálózati hivatkozást kap.</span><span class="sxs-lookup"><span data-stu-id="d878b-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="d878b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d878b-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d878b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d878b-105">DESCRIPTION</span></span>
<span data-ttu-id="d878b-106">A **Get-AzPrivateDnsVirtualNetworkLink** parancsmag virtuális hálózati hivatkozásokat kap egy adott privát DNS-zónához a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="d878b-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="d878b-107">Ha megadja a *Name paramétert,* egyetlen **PSPrivateDnsVirtualNetworkLink** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d878b-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="d878b-108">Ha nem adja meg a *Name* paramétert, a visszaadott érték egy tömb, amely a megadott erőforráscsoport zónával társított összes csatolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d878b-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="d878b-109">A **PSPrivateDnsVirtualNetworkLink** objektummal frissítheti a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d878b-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="d878b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d878b-110">EXAMPLES</span></span>

### <span data-ttu-id="d878b-111">1. példa: Virtuális hálózati hivatkozás lekérte.</span><span class="sxs-lookup"><span data-stu-id="d878b-111">Example 1: Get a virtual network link.</span></span>
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

<span data-ttu-id="d878b-112">Ebben a példában a virtuális hálózati kapcsolat mylink van társítva a myzone.com nevű privát DNS-zónával a megadott erőforráscsoportból, majd tárolja azt a $Link változóban.</span><span class="sxs-lookup"><span data-stu-id="d878b-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="d878b-113">2. példa: Egy erőforráscsoport zónával társított összes hivatkozásának be szereznie.</span><span class="sxs-lookup"><span data-stu-id="d878b-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
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

<span data-ttu-id="d878b-114">Ez a példa a megadott erőforráscsoportban a "myzone.com" privát DNS-zónához társított összes virtuális hálózati hivatkozást beveszi, majd a $Links tárolja.</span><span class="sxs-lookup"><span data-stu-id="d878b-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="d878b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d878b-115">PARAMETERS</span></span>

### <span data-ttu-id="d878b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d878b-116">-DefaultProfile</span></span>
<span data-ttu-id="d878b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d878b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d878b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d878b-118">-Name</span></span>
<span data-ttu-id="d878b-119">A lekért virtuális hálózati hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d878b-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="d878b-120">Ha nem ad meg értéket a *Name* paraméternek, ez a parancsmag a megadott privát DNS-zónához tartozó összes hivatkozást lekérte a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d878b-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="d878b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d878b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d878b-122">Annak az erőforráscsoportnak a neve, amely a lekért virtuális hálózati hivatkozást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d878b-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="d878b-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d878b-123">-ZoneName</span></span>
<span data-ttu-id="d878b-124">Annak a privát DNS-zónának a nevét adja meg, amelyhez a virtuális hálózati kapcsolat kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="d878b-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="d878b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d878b-125">CommonParameters</span></span>
<span data-ttu-id="d878b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d878b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d878b-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d878b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d878b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d878b-128">INPUTS</span></span>

### <span data-ttu-id="d878b-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="d878b-129">None</span></span>

## <span data-ttu-id="d878b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d878b-130">OUTPUTS</span></span>

### <span data-ttu-id="d878b-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d878b-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d878b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d878b-132">NOTES</span></span>

## <span data-ttu-id="d878b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d878b-133">RELATED LINKS</span></span>

[<span data-ttu-id="d878b-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d878b-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d878b-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d878b-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d878b-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d878b-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
