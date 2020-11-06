---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504320"
---
# <span data-ttu-id="141ea-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="141ea-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="141ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="141ea-102">SYNOPSIS</span></span>
<span data-ttu-id="141ea-103">A virtuális hálózat cél állapotának beállítása koppintással.</span><span class="sxs-lookup"><span data-stu-id="141ea-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="141ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="141ea-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="141ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="141ea-105">DESCRIPTION</span></span>
<span data-ttu-id="141ea-106">A **set-AzureRmVirtualNetworkTap** egy Azure Virtual Network cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="141ea-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="141ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="141ea-107">EXAMPLES</span></span>

### <span data-ttu-id="141ea-108">Példa 1: virtuális hálózat beállítása koppintás</span><span class="sxs-lookup"><span data-stu-id="141ea-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="141ea-109">A parancs frissíti a célhely IpConfiguration, és frissíti a virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="141ea-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="141ea-110">Ha vannak olyan koppintásos konfigurációk, amelyek hivatkoznak rá, akkor az összes forrás-forgalom nem fog megjelenni az új IP-címek konfigurációjának frissítése után.</span><span class="sxs-lookup"><span data-stu-id="141ea-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="141ea-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="141ea-111">PARAMETERS</span></span>

### <span data-ttu-id="141ea-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="141ea-112">-AsJob</span></span>
<span data-ttu-id="141ea-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="141ea-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141ea-114">-DefaultProfile</span></span>
<span data-ttu-id="141ea-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="141ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141ea-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="141ea-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="141ea-117">A virtuális hálózat koppintással</span><span class="sxs-lookup"><span data-stu-id="141ea-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="141ea-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="141ea-118">-Confirm</span></span>
<span data-ttu-id="141ea-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="141ea-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ea-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141ea-120">-WhatIf</span></span>
<span data-ttu-id="141ea-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="141ea-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141ea-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="141ea-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141ea-123">CommonParameters</span></span>
<span data-ttu-id="141ea-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="141ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141ea-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141ea-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="141ea-126">INPUTS</span></span>

### <span data-ttu-id="141ea-127">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="141ea-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="141ea-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="141ea-128">OUTPUTS</span></span>

### <span data-ttu-id="141ea-129">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="141ea-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="141ea-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="141ea-130">NOTES</span></span>

## <span data-ttu-id="141ea-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="141ea-131">RELATED LINKS</span></span>
