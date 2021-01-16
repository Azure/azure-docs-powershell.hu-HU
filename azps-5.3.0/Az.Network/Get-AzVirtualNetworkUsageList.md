---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379818"
---
# <span data-ttu-id="eaf8a-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="eaf8a-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="eaf8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf8a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf8a-103">Virtuális hálózat aktuális használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="eaf8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eaf8a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaf8a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eaf8a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf8a-106">A **Get-AzVirtualNetworkUsageList** parancsmag a megadott virtuális hálózat alhálózati használatára terjed ki.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="eaf8a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eaf8a-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf8a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="eaf8a-108">Example 1</span></span>
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

<span data-ttu-id="eaf8a-109">Alhálózatonkénti aktuális használati értékeket kap a usagetest virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="eaf8a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf8a-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf8a-111">-DefaultProfile</span></span>
<span data-ttu-id="eaf8a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaf8a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="eaf8a-113">-Name</span></span>
<span data-ttu-id="eaf8a-114">Annak a virtuális hálózatnak a nevét adja meg, amely a használatot mutatja.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="eaf8a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf8a-115">-ResourceGroupName</span></span>
<span data-ttu-id="eaf8a-116">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="eaf8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf8a-117">CommonParameters</span></span>
<span data-ttu-id="eaf8a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf8a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaf8a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf8a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaf8a-120">INPUTS</span></span>

### <span data-ttu-id="eaf8a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="eaf8a-121">System.String</span></span>

## <span data-ttu-id="eaf8a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf8a-122">OUTPUTS</span></span>

### <span data-ttu-id="eaf8a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="eaf8a-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="eaf8a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eaf8a-124">NOTES</span></span>

## <span data-ttu-id="eaf8a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaf8a-125">RELATED LINKS</span></span>
