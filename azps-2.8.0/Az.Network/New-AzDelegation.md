---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 32398b235ef28872730f5839cef52023fe0f4ee9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837478"
---
# <span data-ttu-id="fb50f-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="fb50f-101">New-AzDelegation</span></span>

## <span data-ttu-id="fb50f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb50f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb50f-103">Szolgáltatási meghatalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fb50f-103">Creates a service delegation.</span></span>

## <span data-ttu-id="fb50f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb50f-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb50f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb50f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb50f-106">A **New-AzDelegation** parancsmag létrehoz egy olyan szolgáltatási delegációt, amely hozzáadható egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="fb50f-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="fb50f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb50f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb50f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb50f-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="fb50f-109">Az első parancsmag létrehoz egy olyan delegálást, amelyet felvehet egy alhálózatba, és a $delegation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fb50f-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="fb50f-110">A második és a harmadik parancsmag kikeresi a delegálni kívánt alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="fb50f-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="fb50f-111">A negyedik parancsmag felveszi a létrehozott delegálást az érdeklődési alhálózatba, és a végleges parancsmag elküldi a frissített konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="fb50f-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="fb50f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb50f-112">PARAMETERS</span></span>

### <span data-ttu-id="fb50f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb50f-113">-DefaultProfile</span></span>
<span data-ttu-id="fb50f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb50f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb50f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb50f-115">-Name</span></span>
<span data-ttu-id="fb50f-116">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="fb50f-116">The name of the delegation</span></span>

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

### <span data-ttu-id="fb50f-117">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fb50f-117">-ServiceName</span></span>
<span data-ttu-id="fb50f-118">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="fb50f-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="fb50f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb50f-119">CommonParameters</span></span>
<span data-ttu-id="fb50f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb50f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb50f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb50f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb50f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb50f-122">INPUTS</span></span>

### <span data-ttu-id="fb50f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fb50f-123">System.String</span></span>

## <span data-ttu-id="fb50f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb50f-124">OUTPUTS</span></span>

### <span data-ttu-id="fb50f-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="fb50f-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="fb50f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb50f-126">NOTES</span></span>

## <span data-ttu-id="fb50f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb50f-127">RELATED LINKS</span></span>

<span data-ttu-id="fb50f-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="fb50f-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>