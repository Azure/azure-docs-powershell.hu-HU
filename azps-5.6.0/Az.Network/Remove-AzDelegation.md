---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 65149a0a52bc1bbb696b78033ec38670db97da48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940186"
---
# <span data-ttu-id="83fc3-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="83fc3-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="83fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="83fc3-103">Eltávolítja a szolgáltatásdelegálást a megadott alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="83fc3-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="83fc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83fc3-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83fc3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="83fc3-106">Az **Remove-AzDelegation** parancsmag delegált alhálózatot vesz fel, és eltávolítja a megnevezett delegálást az alhálózatból.</span><span class="sxs-lookup"><span data-stu-id="83fc3-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="83fc3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="83fc3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="83fc3-108">Example 1</span></span>
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

<span data-ttu-id="83fc3-109">Ebben a példában az első (a _"Meghatalmazás_ hozzáadása meglévő alhálózathoz" rész alatt található) megegyezik az [Add-AzDelegation szöveggel.](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="83fc3-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="83fc3-110">A második felében az első két parancsmag lekéri a megfelelő alhálózatot, és frissíti a helyi példányt a kiszolgálón található adatokkal.</span><span class="sxs-lookup"><span data-stu-id="83fc3-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="83fc3-111">A harmadik parancsmag eltávolítja az első felében létrehozott meghatalmazást a _mySubnetről,_ és a frissített alhálózatot _$subnet._</span><span class="sxs-lookup"><span data-stu-id="83fc3-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="83fc3-112">Az utolsó parancsmag frissíti a kiszolgálót az eltávolított delegálással.</span><span class="sxs-lookup"><span data-stu-id="83fc3-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="83fc3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83fc3-113">PARAMETERS</span></span>

### <span data-ttu-id="83fc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fc3-114">-DefaultProfile</span></span>
<span data-ttu-id="83fc3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83fc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83fc3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="83fc3-116">-Name</span></span>
<span data-ttu-id="83fc3-117">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="83fc3-117">The name of the delegation</span></span>

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

### <span data-ttu-id="83fc3-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="83fc3-118">-Subnet</span></span>
<span data-ttu-id="83fc3-119">Az alhálózat, amelyből el szeretné távolítani a meghatalmazást</span><span class="sxs-lookup"><span data-stu-id="83fc3-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="83fc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fc3-120">CommonParameters</span></span>
<span data-ttu-id="83fc3-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fc3-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fc3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fc3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83fc3-123">INPUTS</span></span>

### <span data-ttu-id="83fc3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="83fc3-124">System.String</span></span>

### <span data-ttu-id="83fc3-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="83fc3-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="83fc3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83fc3-126">OUTPUTS</span></span>

### <span data-ttu-id="83fc3-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="83fc3-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="83fc3-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83fc3-128">NOTES</span></span>

## <span data-ttu-id="83fc3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83fc3-129">RELATED LINKS</span></span>

<span data-ttu-id="83fc3-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="83fc3-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>