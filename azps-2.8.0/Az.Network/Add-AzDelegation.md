---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: e7646ff4a52131aaf1468cf32534235f71e7bf7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837685"
---
# <span data-ttu-id="cdc27-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="cdc27-101">Add-AzDelegation</span></span>

## <span data-ttu-id="cdc27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdc27-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc27-103">Meghatalmazást ad egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="cdc27-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="cdc27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdc27-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc27-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdc27-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc27-106">Az **Add-AzDelegation** parancsmag szolgáltatás-delegálást ad hozzá az Azure subnet-hoz.</span><span class="sxs-lookup"><span data-stu-id="cdc27-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="cdc27-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cdc27-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc27-108">1: meghatalmazás hozzáadása</span><span class="sxs-lookup"><span data-stu-id="cdc27-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="cdc27-109">Az első parancs kikeresi azt a virtuális hálózatot, amelyen az alhálózat fekszik.</span><span class="sxs-lookup"><span data-stu-id="cdc27-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="cdc27-110">A második parancs elkülöníti az érdeklődési alhálózatot, amelyet delegálni szeretne.</span><span class="sxs-lookup"><span data-stu-id="cdc27-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="cdc27-111">A harmadik parancs felvesz egy delegálást az alhálózatba.</span><span class="sxs-lookup"><span data-stu-id="cdc27-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="cdc27-112">Ez a konkrét példa akkor hasznos, ha engedélyezni szeretné, hogy az SQL engedélyezze a kapcsolati végpontok létrehozását ebben az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="cdc27-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="cdc27-113">A végleges parancs elküldi a frissített alhálózatot a kiszolgálónak az alhálózat tényleges frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="cdc27-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="cdc27-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdc27-114">PARAMETERS</span></span>

### <span data-ttu-id="cdc27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc27-115">-DefaultProfile</span></span>
<span data-ttu-id="cdc27-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdc27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc27-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdc27-117">-Name</span></span>
<span data-ttu-id="cdc27-118">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="cdc27-118">The name of the delegation</span></span>

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

### <span data-ttu-id="cdc27-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="cdc27-119">-ServiceName</span></span>
<span data-ttu-id="cdc27-120">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="cdc27-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="cdc27-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="cdc27-121">-Subnet</span></span>
<span data-ttu-id="cdc27-122">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="cdc27-122">The subnet</span></span>

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

### <span data-ttu-id="cdc27-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc27-123">CommonParameters</span></span>
<span data-ttu-id="cdc27-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdc27-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc27-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc27-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc27-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdc27-126">INPUTS</span></span>

### <span data-ttu-id="cdc27-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc27-127">System.String</span></span>

### <span data-ttu-id="cdc27-128">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cdc27-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cdc27-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdc27-129">OUTPUTS</span></span>

### <span data-ttu-id="cdc27-130">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cdc27-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="cdc27-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdc27-131">NOTES</span></span>

## <span data-ttu-id="cdc27-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdc27-132">RELATED LINKS</span></span>

<span data-ttu-id="cdc27-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cdc27-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>