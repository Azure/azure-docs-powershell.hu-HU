---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 213c6616a143f7be64454f6538fac5d5c89afd54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014868"
---
# <span data-ttu-id="a9368-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="a9368-101">Get-AzDelegation</span></span>

## <span data-ttu-id="a9368-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9368-102">SYNOPSIS</span></span>
<span data-ttu-id="a9368-103">Egy adott alhálózathoz delegálhatja a meghatalmazást (vagy az összes delegálást).</span><span class="sxs-lookup"><span data-stu-id="a9368-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="a9368-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9368-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9368-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9368-105">DESCRIPTION</span></span>
<span data-ttu-id="a9368-106">A **Get-AzDelegation** parancsmag az alhálózatból kapja meg a elnevezett delegálást.</span><span class="sxs-lookup"><span data-stu-id="a9368-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="a9368-107">Ha a program nem nevezi el a meghatalmazást, akkor a megadott alhálózat összes delegációját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a9368-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="a9368-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a9368-108">EXAMPLES</span></span>

### <span data-ttu-id="a9368-109">1: adott meghatalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="a9368-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="a9368-110">Az első sorba beolvassa az érdeklődési alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="a9368-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a9368-111">A második soron a "myDelegation" nevű meghatalmazás delegálási adatai láthatók.</span><span class="sxs-lookup"><span data-stu-id="a9368-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="a9368-112">2: az összes alhálózati delegáció beolvasása</span><span class="sxs-lookup"><span data-stu-id="a9368-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="a9368-113">Az első sorba beolvassa az érdeklődési alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="a9368-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a9368-114">A második soron a $delegations változóban lévő _mySubnet_ összes delegációjának listáját tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9368-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="a9368-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9368-115">PARAMETERS</span></span>

### <span data-ttu-id="a9368-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9368-116">-DefaultProfile</span></span>
<span data-ttu-id="a9368-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9368-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9368-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9368-118">-Name</span></span>
<span data-ttu-id="a9368-119">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="a9368-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9368-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="a9368-120">-Subnet</span></span>
<span data-ttu-id="a9368-121">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="a9368-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9368-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9368-122">CommonParameters</span></span>
<span data-ttu-id="a9368-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9368-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9368-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9368-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9368-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9368-125">INPUTS</span></span>

### <span data-ttu-id="a9368-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a9368-126">System.String</span></span>

### <span data-ttu-id="a9368-127">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a9368-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a9368-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9368-128">OUTPUTS</span></span>

### <span data-ttu-id="a9368-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a9368-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a9368-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9368-130">NOTES</span></span>

## <span data-ttu-id="a9368-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9368-131">RELATED LINKS</span></span>

<span data-ttu-id="a9368-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Új – AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a9368-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>