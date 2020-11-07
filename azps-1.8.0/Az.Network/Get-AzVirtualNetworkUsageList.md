---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670463"
---
# <span data-ttu-id="743b1-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="743b1-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="743b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="743b1-102">SYNOPSIS</span></span>
<span data-ttu-id="743b1-103">Megkapja a virtuális hálózat jelenlegi használatát.</span><span class="sxs-lookup"><span data-stu-id="743b1-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="743b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="743b1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="743b1-105">DESCRIPTION</span></span>
<span data-ttu-id="743b1-106">A **Get-AzVirtualNetworkUsageList** parancsmag a megadott virtuális hálózathoz tartozó alhálózati használatot kapja.</span><span class="sxs-lookup"><span data-stu-id="743b1-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="743b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="743b1-107">EXAMPLES</span></span>

### <span data-ttu-id="743b1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="743b1-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="743b1-109">A usagetest virtuális hálózat használati értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="743b1-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="743b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="743b1-110">PARAMETERS</span></span>

### <span data-ttu-id="743b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743b1-111">-DefaultProfile</span></span>
<span data-ttu-id="743b1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="743b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743b1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="743b1-113">-Name</span></span>
<span data-ttu-id="743b1-114">Annak a virtuális hálózatnak a nevét adja meg, amely a felhasználásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="743b1-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="743b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="743b1-116">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="743b1-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="743b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743b1-117">CommonParameters</span></span>
<span data-ttu-id="743b1-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="743b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743b1-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="743b1-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743b1-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="743b1-120">INPUTS</span></span>

### <span data-ttu-id="743b1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="743b1-121">System.String</span></span>

## <span data-ttu-id="743b1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="743b1-122">OUTPUTS</span></span>

### <span data-ttu-id="743b1-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="743b1-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="743b1-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="743b1-124">NOTES</span></span>

## <span data-ttu-id="743b1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="743b1-125">RELATED LINKS</span></span>
