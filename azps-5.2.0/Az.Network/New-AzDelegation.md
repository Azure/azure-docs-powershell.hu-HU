---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371683"
---
# <span data-ttu-id="26429-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="26429-101">New-AzDelegation</span></span>

## <span data-ttu-id="26429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26429-102">SYNOPSIS</span></span>
<span data-ttu-id="26429-103">Szolgáltatásdelegálást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26429-103">Creates a service delegation.</span></span>

## <span data-ttu-id="26429-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26429-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26429-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26429-105">DESCRIPTION</span></span>
<span data-ttu-id="26429-106">A **New-AzDelegation** parancsmag létrehoz egy szolgáltatásdelegálást, amely hozzáadható az alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="26429-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="26429-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26429-107">EXAMPLES</span></span>

### <span data-ttu-id="26429-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="26429-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="26429-109">Az első parancsmag létrehoz egy delegálást, amely hozzáadható egy alhálózathoz, és a helyi $delegation tárolja.</span><span class="sxs-lookup"><span data-stu-id="26429-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="26429-110">A második és a harmadik parancsmag lekéri a delegálható alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="26429-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="26429-111">A negyedik parancsmag hozzáadja a létrehozott meghatalmazást az érdekes alhálózathoz, a végleges parancsmag pedig elküldi a frissített konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="26429-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="26429-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26429-112">PARAMETERS</span></span>

### <span data-ttu-id="26429-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26429-113">-DefaultProfile</span></span>
<span data-ttu-id="26429-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26429-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26429-115">-Name</span><span class="sxs-lookup"><span data-stu-id="26429-115">-Name</span></span>
<span data-ttu-id="26429-116">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="26429-116">The name of the delegation</span></span>

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

### <span data-ttu-id="26429-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="26429-117">-ServiceName</span></span>
<span data-ttu-id="26429-118">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="26429-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="26429-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26429-119">CommonParameters</span></span>
<span data-ttu-id="26429-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26429-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26429-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26429-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26429-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26429-122">INPUTS</span></span>

### <span data-ttu-id="26429-123">System.String</span><span class="sxs-lookup"><span data-stu-id="26429-123">System.String</span></span>

## <span data-ttu-id="26429-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26429-124">OUTPUTS</span></span>

### <span data-ttu-id="26429-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="26429-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="26429-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26429-126">NOTES</span></span>

## <span data-ttu-id="26429-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26429-127">RELATED LINKS</span></span>

<span data-ttu-id="26429-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="26429-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>