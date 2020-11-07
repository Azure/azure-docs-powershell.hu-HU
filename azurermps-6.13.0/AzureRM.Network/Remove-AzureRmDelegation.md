---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680048"
---
# <span data-ttu-id="55bd2-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="55bd2-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="55bd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="55bd2-103">A megadott alhálózatból eltávolítja a szolgáltatási meghatalmazást.</span><span class="sxs-lookup"><span data-stu-id="55bd2-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55bd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55bd2-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55bd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="55bd2-106">A **Remove-AzureRmDelegation** parancsmag delegált alhálózatot hoz létre, és az adott alhálózatról eltávolítja a névvel ellátott delegálást.</span><span class="sxs-lookup"><span data-stu-id="55bd2-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="55bd2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="55bd2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="55bd2-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="55bd2-109">Ebben a példában az első fele (a _"delegálás felvétele meglévő alhálózatba"_ ) azonos a [bővítmények AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="55bd2-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="55bd2-110">A második félidőben az első két parancsmag kikeresi az érdeklődési alhálózatot, és a kiszolgálón frissítheti a helyi példányt.</span><span class="sxs-lookup"><span data-stu-id="55bd2-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="55bd2-111">A harmadik parancsmag eltávolítja a _mySubnet_ első felén létrehozott delegálást, és a frissített alhálózatot tárolja _$subnet_.</span><span class="sxs-lookup"><span data-stu-id="55bd2-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="55bd2-112">A végleges parancsmag az eltávolított delegálással frissíti a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="55bd2-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="55bd2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55bd2-113">PARAMETERS</span></span>

### <span data-ttu-id="55bd2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bd2-114">-DefaultProfile</span></span>
<span data-ttu-id="55bd2-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55bd2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bd2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55bd2-116">-Name</span></span>
<span data-ttu-id="55bd2-117">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="55bd2-117">The name of the delegation</span></span>

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

### <span data-ttu-id="55bd2-118">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="55bd2-118">-ServiceName</span></span>
<span data-ttu-id="55bd2-119">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="55bd2-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="55bd2-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="55bd2-120">-Subnet</span></span>
<span data-ttu-id="55bd2-121">Az az alhálózat, amelyből el szeretné távolítani a meghatalmazást</span><span class="sxs-lookup"><span data-stu-id="55bd2-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="55bd2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bd2-122">CommonParameters</span></span>
<span data-ttu-id="55bd2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55bd2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bd2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55bd2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bd2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55bd2-125">INPUTS</span></span>

### <span data-ttu-id="55bd2-126">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="55bd2-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="55bd2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="55bd2-127">System.String</span></span>
## <span data-ttu-id="55bd2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55bd2-128">OUTPUTS</span></span>

### <span data-ttu-id="55bd2-129">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="55bd2-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="55bd2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55bd2-130">NOTES</span></span>

## <span data-ttu-id="55bd2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55bd2-131">RELATED LINKS</span></span>

<span data-ttu-id="55bd2-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Új – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="55bd2-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
