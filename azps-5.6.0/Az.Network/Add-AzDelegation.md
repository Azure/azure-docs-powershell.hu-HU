---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936170"
---
# <span data-ttu-id="2c50a-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="2c50a-101">Add-AzDelegation</span></span>

## <span data-ttu-id="2c50a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c50a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c50a-103">Delegálás hozzáadása alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="2c50a-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="2c50a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c50a-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c50a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c50a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c50a-106">Az **Add-AzDelegation** parancsmag hozzáad egy szolgáltatásdelegálást egy Azure-alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="2c50a-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="2c50a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c50a-107">EXAMPLES</span></span>

### <span data-ttu-id="2c50a-108">1. példa: Meghatalmazás hozzáadása</span><span class="sxs-lookup"><span data-stu-id="2c50a-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="2c50a-109">Az első parancs beolvassa azt a virtuális hálózatot, amelyen az alhálózat található.</span><span class="sxs-lookup"><span data-stu-id="2c50a-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="2c50a-110">A második parancs elkülöníti az érdekes alhálózatot – azt, amelyiket meg szeretné delegálni.</span><span class="sxs-lookup"><span data-stu-id="2c50a-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="2c50a-111">A harmadik parancs delegálást ad az alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="2c50a-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="2c50a-112">Ez a példa akkor lehet hasznos, ha engedélyezni szeretné az SQL-nek, hogy felületi végpontokat hozzon létre ebben az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="2c50a-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="2c50a-113">Az utolsó parancs elküldi a frissített alhálózatot a kiszolgálónak, hogy ténylegesen frissítse az alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="2c50a-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="2c50a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c50a-114">PARAMETERS</span></span>

### <span data-ttu-id="2c50a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c50a-115">-DefaultProfile</span></span>
<span data-ttu-id="2c50a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c50a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c50a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2c50a-117">-Name</span></span>
<span data-ttu-id="2c50a-118">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="2c50a-118">The name of the delegation</span></span>

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

### <span data-ttu-id="2c50a-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c50a-119">-ServiceName</span></span>
<span data-ttu-id="2c50a-120">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="2c50a-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="2c50a-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="2c50a-121">-Subnet</span></span>
<span data-ttu-id="2c50a-122">Az alhálózat</span><span class="sxs-lookup"><span data-stu-id="2c50a-122">The subnet</span></span>

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

### <span data-ttu-id="2c50a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c50a-123">CommonParameters</span></span>
<span data-ttu-id="2c50a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c50a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c50a-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c50a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c50a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c50a-126">INPUTS</span></span>

### <span data-ttu-id="2c50a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2c50a-127">System.String</span></span>

### <span data-ttu-id="2c50a-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2c50a-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2c50a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c50a-129">OUTPUTS</span></span>

### <span data-ttu-id="2c50a-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2c50a-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2c50a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c50a-131">NOTES</span></span>

## <span data-ttu-id="2c50a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c50a-132">RELATED LINKS</span></span>

<span data-ttu-id="2c50a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="2c50a-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>