---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
ms.openlocfilehash: 61717f314629259caca9329c2ef1a458aa9a0e0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848146"
---
# <span data-ttu-id="f1914-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="f1914-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="f1914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1914-102">SYNOPSIS</span></span>
<span data-ttu-id="f1914-103">Megkapja a virtuális hálózat jelenlegi használatát.</span><span class="sxs-lookup"><span data-stu-id="f1914-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1914-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1914-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1914-105">DESCRIPTION</span></span>
<span data-ttu-id="f1914-106">A **Get-AzureRmVirtualNetworkUsageList** parancsmag a megadott virtuális hálózathoz tartozó alhálózati használatot kapja.</span><span class="sxs-lookup"><span data-stu-id="f1914-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="f1914-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1914-107">EXAMPLES</span></span>

### <span data-ttu-id="f1914-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1914-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="f1914-109">A usagetest virtuális hálózat használati értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f1914-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="f1914-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1914-110">PARAMETERS</span></span>

### <span data-ttu-id="f1914-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1914-111">-DefaultProfile</span></span>
<span data-ttu-id="f1914-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1914-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1914-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1914-113">-Name</span></span>
<span data-ttu-id="f1914-114">Annak a virtuális hálózatnak a nevét adja meg, amely a felhasználásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f1914-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="f1914-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1914-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1914-116">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="f1914-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="f1914-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1914-117">CommonParameters</span></span>
<span data-ttu-id="f1914-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1914-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1914-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1914-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1914-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1914-120">INPUTS</span></span>

### <span data-ttu-id="f1914-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f1914-121">System.String</span></span>

## <span data-ttu-id="f1914-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1914-122">OUTPUTS</span></span>

### <span data-ttu-id="f1914-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="f1914-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="f1914-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1914-124">NOTES</span></span>

## <span data-ttu-id="f1914-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1914-125">RELATED LINKS</span></span>

