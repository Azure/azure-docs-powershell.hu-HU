---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501124"
---
# <span data-ttu-id="5b2a1-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5b2a1-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="5b2a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2a1-103">Egy adott alhálózathoz delegálhatja a meghatalmazást (vagy az összes delegálást).</span><span class="sxs-lookup"><span data-stu-id="5b2a1-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b2a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b2a1-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b2a1-105">DESCRIPTION</span></span>
<span data-ttu-id="5b2a1-106">A **Get-AzureRmDelegation** parancsmag az alhálózatból kapja meg a elnevezett delegálást.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="5b2a1-107">Ha a program nem nevezi el a meghatalmazást, akkor a megadott alhálózat összes delegációját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="5b2a1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5b2a1-108">EXAMPLES</span></span>

### <span data-ttu-id="5b2a1-109">1: adott meghatalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="5b2a1-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="5b2a1-110">Az első sorba beolvassa az érdeklődési alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5b2a1-111">A második soron a "myDelegation" nevű meghatalmazás delegálási adatai láthatók.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="5b2a1-112">2: az összes alhálózati delegáció beolvasása</span><span class="sxs-lookup"><span data-stu-id="5b2a1-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="5b2a1-113">Az első sorba beolvassa az érdeklődési alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5b2a1-114">A második soron a $delegations változóban lévő _mySubnet_ összes delegációjának listáját tárolja.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="5b2a1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b2a1-115">PARAMETERS</span></span>

### <span data-ttu-id="5b2a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2a1-116">-DefaultProfile</span></span>
<span data-ttu-id="5b2a1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b2a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2a1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b2a1-118">-Name</span></span>
<span data-ttu-id="5b2a1-119">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="5b2a1-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2a1-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5b2a1-120">-Subnet</span></span>
<span data-ttu-id="5b2a1-121">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="5b2a1-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b2a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2a1-122">CommonParameters</span></span>
<span data-ttu-id="5b2a1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b2a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b2a1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b2a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2a1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b2a1-125">INPUTS</span></span>

### <span data-ttu-id="5b2a1-126">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5b2a1-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5b2a1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b2a1-127">OUTPUTS</span></span>

### <span data-ttu-id="5b2a1-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="5b2a1-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5b2a1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b2a1-129">NOTES</span></span>

## <span data-ttu-id="5b2a1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b2a1-130">RELATED LINKS</span></span>
<span data-ttu-id="5b2a1-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Új – AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="5b2a1-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
