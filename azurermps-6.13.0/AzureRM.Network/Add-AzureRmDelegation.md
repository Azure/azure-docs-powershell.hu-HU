---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502036"
---
# <span data-ttu-id="8f907-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="8f907-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="8f907-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f907-102">SYNOPSIS</span></span>
<span data-ttu-id="8f907-103">Meghatalmazást ad egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="8f907-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f907-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f907-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f907-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f907-105">DESCRIPTION</span></span>
<span data-ttu-id="8f907-106">Az **Add-AzureRmDelegation** parancsmag szolgáltatás-delegálást ad hozzá az Azure subnet-hoz.</span><span class="sxs-lookup"><span data-stu-id="8f907-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="8f907-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f907-107">EXAMPLES</span></span>

### <span data-ttu-id="8f907-108">1: meghatalmazás hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8f907-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="8f907-109">Az első parancs kikeresi azt a virtuális hálózatot, amelyen az alhálózat fekszik.</span><span class="sxs-lookup"><span data-stu-id="8f907-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="8f907-110">A második parancs elkülöníti az érdeklődési alhálózatot, amelyet delegálni szeretne.</span><span class="sxs-lookup"><span data-stu-id="8f907-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="8f907-111">A harmadik parancs felvesz egy delegálást az alhálózatba.</span><span class="sxs-lookup"><span data-stu-id="8f907-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="8f907-112">Ez a konkrét példa akkor hasznos, ha engedélyezni szeretné, hogy az SQL engedélyezze a kapcsolati végpontok létrehozását ebben az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="8f907-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="8f907-113">A végleges parancs elküldi a frissített alhálózatot a kiszolgálónak az alhálózat tényleges frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8f907-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="8f907-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f907-114">PARAMETERS</span></span>

### <span data-ttu-id="8f907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f907-115">-DefaultProfile</span></span>
<span data-ttu-id="8f907-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f907-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f907-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f907-117">-Name</span></span>
<span data-ttu-id="8f907-118">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="8f907-118">The name of the delegation</span></span>

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

### <span data-ttu-id="8f907-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="8f907-119">-ServiceName</span></span>
<span data-ttu-id="8f907-120">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="8f907-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="8f907-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="8f907-121">-Subnet</span></span>
<span data-ttu-id="8f907-122">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="8f907-122">The subnet</span></span>

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

### <span data-ttu-id="8f907-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f907-123">CommonParameters</span></span>
<span data-ttu-id="8f907-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f907-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8f907-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f907-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f907-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f907-126">INPUTS</span></span>

### <span data-ttu-id="8f907-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8f907-127">System.String</span></span>

### <span data-ttu-id="8f907-128">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8f907-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8f907-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f907-129">OUTPUTS</span></span>

### <span data-ttu-id="8f907-130">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8f907-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8f907-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f907-131">NOTES</span></span>

## <span data-ttu-id="8f907-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f907-132">RELATED LINKS</span></span>
<span data-ttu-id="8f907-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="8f907-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
