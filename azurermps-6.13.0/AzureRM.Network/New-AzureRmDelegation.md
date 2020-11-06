---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500192"
---
# <span data-ttu-id="a1399-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a1399-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="a1399-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1399-102">SYNOPSIS</span></span>
<span data-ttu-id="a1399-103">Szolgáltatási meghatalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a1399-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1399-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1399-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1399-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1399-105">DESCRIPTION</span></span>
<span data-ttu-id="a1399-106">A **New-AzureRmDelegation** parancsmag létrehoz egy olyan szolgáltatási delegációt, amely hozzáadható egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="a1399-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="a1399-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1399-107">EXAMPLES</span></span>

### <span data-ttu-id="a1399-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1399-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="a1399-109">Az első parancsmag létrehoz egy olyan delegálást, amelyet felvehet egy alhálózatba, és a $delegation változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a1399-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="a1399-110">A második és a harmadik parancsmag kikeresi a delegálni kívánt alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="a1399-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="a1399-111">A negyedik parancsmag felveszi a létrehozott delegálást az érdeklődési alhálózatba, és a végleges parancsmag elküldi a frissített konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="a1399-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="a1399-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1399-112">PARAMETERS</span></span>

### <span data-ttu-id="a1399-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1399-113">-DefaultProfile</span></span>
<span data-ttu-id="a1399-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1399-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1399-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1399-115">-Name</span></span>
<span data-ttu-id="a1399-116">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="a1399-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1399-117">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a1399-117">-ServiceName</span></span>
<span data-ttu-id="a1399-118">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="a1399-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1399-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1399-119">CommonParameters</span></span>
<span data-ttu-id="a1399-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1399-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a1399-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1399-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1399-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1399-122">INPUTS</span></span>

### <span data-ttu-id="a1399-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a1399-123">System.String</span></span>

## <span data-ttu-id="a1399-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1399-124">OUTPUTS</span></span>

### <span data-ttu-id="a1399-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a1399-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a1399-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1399-126">NOTES</span></span>

## <span data-ttu-id="a1399-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1399-127">RELATED LINKS</span></span>
<span data-ttu-id="a1399-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a1399-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
