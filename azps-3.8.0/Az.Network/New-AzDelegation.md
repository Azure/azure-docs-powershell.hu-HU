---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014755"
---
# <span data-ttu-id="65d56-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="65d56-101">New-AzDelegation</span></span>

## <span data-ttu-id="65d56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65d56-102">SYNOPSIS</span></span>
<span data-ttu-id="65d56-103">Szolgáltatási meghatalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="65d56-103">Creates a service delegation.</span></span>

## <span data-ttu-id="65d56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65d56-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65d56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65d56-105">DESCRIPTION</span></span>
<span data-ttu-id="65d56-106">A **New-AzDelegation** parancsmag létrehoz egy olyan szolgáltatási delegációt, amely hozzáadható egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="65d56-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="65d56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65d56-107">EXAMPLES</span></span>

### <span data-ttu-id="65d56-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65d56-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="65d56-109">Az első parancsmag létrehoz egy olyan delegálást, amelyet felvehet egy alhálózatba, és a $delegation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="65d56-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="65d56-110">A második és a harmadik parancsmag kikeresi a delegálni kívánt alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="65d56-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="65d56-111">A negyedik parancsmag felveszi a létrehozott delegálást az érdeklődési alhálózatba, és a végleges parancsmag elküldi a frissített konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="65d56-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="65d56-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65d56-112">PARAMETERS</span></span>

### <span data-ttu-id="65d56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d56-113">-DefaultProfile</span></span>
<span data-ttu-id="65d56-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65d56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d56-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65d56-115">-Name</span></span>
<span data-ttu-id="65d56-116">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="65d56-116">The name of the delegation</span></span>

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

### <span data-ttu-id="65d56-117">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="65d56-117">-ServiceName</span></span>
<span data-ttu-id="65d56-118">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="65d56-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="65d56-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d56-119">CommonParameters</span></span>
<span data-ttu-id="65d56-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65d56-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d56-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d56-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d56-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d56-122">INPUTS</span></span>

### <span data-ttu-id="65d56-123">System. String</span><span class="sxs-lookup"><span data-stu-id="65d56-123">System.String</span></span>

## <span data-ttu-id="65d56-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d56-124">OUTPUTS</span></span>

### <span data-ttu-id="65d56-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="65d56-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="65d56-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65d56-126">NOTES</span></span>

## <span data-ttu-id="65d56-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65d56-127">RELATED LINKS</span></span>

<span data-ttu-id="65d56-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="65d56-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>