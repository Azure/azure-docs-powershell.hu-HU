---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157026"
---
# <span data-ttu-id="2b7f3-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="2b7f3-101">Get-AzDelegation</span></span>

## <span data-ttu-id="2b7f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7f3-103">Delegálás (vagy az összes meghatalmazás) lekérte egy adott alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="2b7f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b7f3-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7f3-106">A **Get-AzDelegation** parancsmag egy alhálózatból kapja meg az elnevezett delegálást.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="2b7f3-107">Ha nincs delegálás elnevezve, akkor a megadott alhálózat összes delegálását visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="2b7f3-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b7f3-108">EXAMPLES</span></span>

### <span data-ttu-id="2b7f3-109">1: Adott meghatalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="2b7f3-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="2b7f3-110">Az első sor a kamat alhálózatát olvassa be.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="2b7f3-111">A második sorban a meghatalmazás "myDelegation" nevű meghatalmazási adatai megjelenik.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="2b7f3-112">2: Az összes alhálózati meghatalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="2b7f3-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="2b7f3-113">Az első sor a kamat alhálózatát olvassa be.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="2b7f3-114">A második sor a _mySubneten_ tárolja az összes delegált listáját a $delegations változóban.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="2b7f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b7f3-115">PARAMETERS</span></span>

### <span data-ttu-id="2b7f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7f3-116">-DefaultProfile</span></span>
<span data-ttu-id="2b7f3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7f3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2b7f3-118">-Name</span></span>
<span data-ttu-id="2b7f3-119">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="2b7f3-119">The name of the delegation</span></span>

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

### <span data-ttu-id="2b7f3-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="2b7f3-120">-Subnet</span></span>
<span data-ttu-id="2b7f3-121">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="2b7f3-121">The subnet</span></span>

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

### <span data-ttu-id="2b7f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7f3-122">CommonParameters</span></span>
<span data-ttu-id="2b7f3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7f3-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b7f3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7f3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7f3-125">INPUTS</span></span>

### <span data-ttu-id="2b7f3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2b7f3-126">System.String</span></span>

### <span data-ttu-id="2b7f3-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2b7f3-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2b7f3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b7f3-128">OUTPUTS</span></span>

### <span data-ttu-id="2b7f3-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="2b7f3-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="2b7f3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b7f3-130">NOTES</span></span>

## <span data-ttu-id="2b7f3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b7f3-131">RELATED LINKS</span></span>

<span data-ttu-id="2b7f3-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="2b7f3-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
