---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024531"
---
# <span data-ttu-id="57a2b-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="57a2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="57a2b-103">Virtuális hálózat frissítése koppintással.</span><span class="sxs-lookup"><span data-stu-id="57a2b-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="57a2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57a2b-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a2b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="57a2b-106">A **set-AzVirtualNetworkTap** parancsmag a virtuális hálózatokra koppintva frissíti a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="57a2b-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="57a2b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="57a2b-108">Példa 1: virtuális hálózat beállítása koppintás</span><span class="sxs-lookup"><span data-stu-id="57a2b-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="57a2b-109">A parancs frissíti a célhely IpConfiguration, és frissíti a virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="57a2b-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="57a2b-110">Ha vannak olyan koppintásos konfigurációk, amelyek hivatkoznak rá, akkor az összes forrás-forgalom nem fog megjelenni az új IP-címek konfigurációjának frissítése után.</span><span class="sxs-lookup"><span data-stu-id="57a2b-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="57a2b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57a2b-111">PARAMETERS</span></span>

### <span data-ttu-id="57a2b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57a2b-112">-AsJob</span></span>
<span data-ttu-id="57a2b-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="57a2b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57a2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a2b-114">-DefaultProfile</span></span>
<span data-ttu-id="57a2b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57a2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57a2b-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="57a2b-117">A virtuális hálózat koppintással</span><span class="sxs-lookup"><span data-stu-id="57a2b-117">The virtual network tap</span></span>

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

### <span data-ttu-id="57a2b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57a2b-118">-Confirm</span></span>
<span data-ttu-id="57a2b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57a2b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a2b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a2b-120">-WhatIf</span></span>
<span data-ttu-id="57a2b-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57a2b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a2b-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57a2b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a2b-123">CommonParameters</span></span>
<span data-ttu-id="57a2b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57a2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a2b-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a2b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a2b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a2b-126">INPUTS</span></span>

### <span data-ttu-id="57a2b-127">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="57a2b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57a2b-128">OUTPUTS</span></span>

### <span data-ttu-id="57a2b-129">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="57a2b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57a2b-130">NOTES</span></span>

## <span data-ttu-id="57a2b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57a2b-131">RELATED LINKS</span></span>

[<span data-ttu-id="57a2b-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="57a2b-133">Új – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="57a2b-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="57a2b-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
