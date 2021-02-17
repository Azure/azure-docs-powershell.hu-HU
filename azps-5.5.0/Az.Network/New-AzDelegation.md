---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206774"
---
# <span data-ttu-id="5108e-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="5108e-101">New-AzDelegation</span></span>

## <span data-ttu-id="5108e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5108e-102">SYNOPSIS</span></span>
<span data-ttu-id="5108e-103">Szolgáltatásdelegálást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5108e-103">Creates a service delegation.</span></span>

## <span data-ttu-id="5108e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5108e-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5108e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5108e-105">DESCRIPTION</span></span>
<span data-ttu-id="5108e-106">A **New-AzDelegation** parancsmag létrehoz egy szolgáltatásdelegálást, amely hozzáadható az alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="5108e-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="5108e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5108e-107">EXAMPLES</span></span>

### <span data-ttu-id="5108e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5108e-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="5108e-109">Az első parancsmag létrehoz egy delegálást, amely hozzáadható egy alhálózathoz, és a helyi $delegation tárolja.</span><span class="sxs-lookup"><span data-stu-id="5108e-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="5108e-110">A második és a harmadik parancsmag beolvassa a delegálható alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="5108e-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="5108e-111">A negyedik parancsmag hozzáadja a létrehozott meghatalmazást az érdekes alhálózathoz, a végleges parancsmag pedig elküldi a frissített konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="5108e-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="5108e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5108e-112">PARAMETERS</span></span>

### <span data-ttu-id="5108e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5108e-113">-DefaultProfile</span></span>
<span data-ttu-id="5108e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5108e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5108e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5108e-115">-Name</span></span>
<span data-ttu-id="5108e-116">A meghatalmazás neve</span><span class="sxs-lookup"><span data-stu-id="5108e-116">The name of the delegation</span></span>

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

### <span data-ttu-id="5108e-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5108e-117">-ServiceName</span></span>
<span data-ttu-id="5108e-118">Annak a szolgáltatásnak a neve, amelyhez az alhálózatot delegálni kell</span><span class="sxs-lookup"><span data-stu-id="5108e-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="5108e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5108e-119">CommonParameters</span></span>
<span data-ttu-id="5108e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5108e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5108e-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5108e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5108e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5108e-122">INPUTS</span></span>

### <span data-ttu-id="5108e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5108e-123">System.String</span></span>

## <span data-ttu-id="5108e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5108e-124">OUTPUTS</span></span>

### <span data-ttu-id="5108e-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="5108e-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5108e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5108e-126">NOTES</span></span>

## <span data-ttu-id="5108e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5108e-127">RELATED LINKS</span></span>

<span data-ttu-id="5108e-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5108e-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>