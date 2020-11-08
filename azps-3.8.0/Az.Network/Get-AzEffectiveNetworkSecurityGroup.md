---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014869"
---
# <span data-ttu-id="29066-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29066-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="29066-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29066-102">SYNOPSIS</span></span>
<span data-ttu-id="29066-103">Egy hálózati kapcsolat hatékony hálózati biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="29066-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="29066-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29066-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29066-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29066-105">DESCRIPTION</span></span>
<span data-ttu-id="29066-106">A **Get-AzEffectiveNetworkSecurityGroup** parancsmag a hálózati felületen alkalmazott hatékony hálózati biztonsági csoportot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="29066-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="29066-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29066-107">EXAMPLES</span></span>

### <span data-ttu-id="29066-108">Példa 1: a hatékony hálózat biztonsági csoportjának beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="29066-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="29066-109">Ez a parancs a myResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati csatolóval társított összes hatékony hálózati biztonsági szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="29066-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="29066-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29066-110">PARAMETERS</span></span>

### <span data-ttu-id="29066-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29066-111">-DefaultProfile</span></span>
<span data-ttu-id="29066-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29066-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29066-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="29066-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="29066-114">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="29066-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="29066-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29066-115">-ResourceGroupName</span></span>
<span data-ttu-id="29066-116">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29066-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="29066-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29066-117">CommonParameters</span></span>
<span data-ttu-id="29066-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29066-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29066-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29066-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29066-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29066-120">INPUTS</span></span>

### <span data-ttu-id="29066-121">System. String</span><span class="sxs-lookup"><span data-stu-id="29066-121">System.String</span></span>

## <span data-ttu-id="29066-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29066-122">OUTPUTS</span></span>

### <span data-ttu-id="29066-123">Microsoft. Azure. commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="29066-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="29066-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29066-124">NOTES</span></span>

## <span data-ttu-id="29066-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29066-125">RELATED LINKS</span></span>

[<span data-ttu-id="29066-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="29066-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


