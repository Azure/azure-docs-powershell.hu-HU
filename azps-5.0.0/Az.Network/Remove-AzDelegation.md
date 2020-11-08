---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195356"
---
# <span data-ttu-id="84356-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="84356-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="84356-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84356-102">SYNOPSIS</span></span>
<span data-ttu-id="84356-103">A megadott alhálózatból eltávolítja a szolgáltatási meghatalmazást.</span><span class="sxs-lookup"><span data-stu-id="84356-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="84356-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84356-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84356-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84356-105">DESCRIPTION</span></span>
<span data-ttu-id="84356-106">A **Remove-AzDelegation** parancsmag delegált alhálózatot hoz létre, és az adott alhálózatról eltávolítja a névvel ellátott delegálást.</span><span class="sxs-lookup"><span data-stu-id="84356-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="84356-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84356-107">EXAMPLES</span></span>

### <span data-ttu-id="84356-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="84356-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="84356-109">Ebben a példában az első fele (a _"delegálás felvétele meglévő alhálózatba"_ ) azonos a [bővítmények AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="84356-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="84356-110">A második félidőben az első két parancsmag kikeresi az érdeklődési alhálózatot, és a kiszolgálón frissítheti a helyi példányt.</span><span class="sxs-lookup"><span data-stu-id="84356-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="84356-111">A harmadik parancsmag eltávolítja a _mySubnet_ első felén létrehozott delegálást, és a frissített alhálózatot tárolja _$subnet_.</span><span class="sxs-lookup"><span data-stu-id="84356-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="84356-112">A végleges parancsmag az eltávolított delegálással frissíti a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="84356-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="84356-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84356-113">PARAMETERS</span></span>

### <span data-ttu-id="84356-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84356-114">-DefaultProfile</span></span>
<span data-ttu-id="84356-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84356-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84356-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84356-116">-Name</span></span>
<span data-ttu-id="84356-117">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="84356-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84356-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="84356-118">-Subnet</span></span>
<span data-ttu-id="84356-119">Az az alhálózat, amelyből el szeretné távolítani a meghatalmazást</span><span class="sxs-lookup"><span data-stu-id="84356-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="84356-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84356-120">CommonParameters</span></span>
<span data-ttu-id="84356-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84356-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84356-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84356-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84356-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84356-123">INPUTS</span></span>

### <span data-ttu-id="84356-124">System. String</span><span class="sxs-lookup"><span data-stu-id="84356-124">System.String</span></span>

### <span data-ttu-id="84356-125">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="84356-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="84356-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84356-126">OUTPUTS</span></span>

### <span data-ttu-id="84356-127">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="84356-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="84356-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84356-128">NOTES</span></span>

## <span data-ttu-id="84356-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84356-129">RELATED LINKS</span></span>

<span data-ttu-id="84356-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Új – AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="84356-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>