---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 618fdf2ebe32f365bce72353f6e148fa3059cf66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505896"
---
# <span data-ttu-id="acfc5-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="acfc5-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="acfc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="acfc5-103">Megkapja a virtuális hálózat jelenlegi használatát.</span><span class="sxs-lookup"><span data-stu-id="acfc5-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acfc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acfc5-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acfc5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="acfc5-105">DESCRIPTION</span></span>
<span data-ttu-id="acfc5-106">A **Get-AzureRmVirtualNetworkUsageList** parancsmag a megadott virtuális hálózathoz tartozó alhálózati használatot kapja.</span><span class="sxs-lookup"><span data-stu-id="acfc5-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="acfc5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="acfc5-107">EXAMPLES</span></span>

### <span data-ttu-id="acfc5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="acfc5-108">Example 1</span></span>
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

<span data-ttu-id="acfc5-109">A usagetest virtuális hálózat használati értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="acfc5-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="acfc5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acfc5-110">PARAMETERS</span></span>

### <span data-ttu-id="acfc5-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acfc5-111">-Name</span></span>
<span data-ttu-id="acfc5-112">Annak a virtuális hálózatnak a nevét adja meg, amely a felhasználásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="acfc5-112">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="acfc5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acfc5-113">-ResourceGroupName</span></span>
<span data-ttu-id="acfc5-114">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="acfc5-114">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="acfc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acfc5-115">-DefaultProfile</span></span>
<span data-ttu-id="acfc5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acfc5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acfc5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acfc5-117">CommonParameters</span></span>
<span data-ttu-id="acfc5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acfc5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acfc5-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acfc5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acfc5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acfc5-120">INPUTS</span></span>

### <span data-ttu-id="acfc5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="acfc5-121">System.String</span></span>

## <span data-ttu-id="acfc5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acfc5-122">OUTPUTS</span></span>

### <span data-ttu-id="acfc5-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="acfc5-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="acfc5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acfc5-124">NOTES</span></span>

## <span data-ttu-id="acfc5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acfc5-125">RELATED LINKS</span></span>

