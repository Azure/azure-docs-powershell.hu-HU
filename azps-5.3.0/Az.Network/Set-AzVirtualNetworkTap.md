---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470110"
---
# <span data-ttu-id="de362-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="de362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de362-102">SYNOPSIS</span></span>
<span data-ttu-id="de362-103">Virtuális hálózati koppintás frissítése.</span><span class="sxs-lookup"><span data-stu-id="de362-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="de362-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de362-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de362-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de362-105">DESCRIPTION</span></span>
<span data-ttu-id="de362-106">A **Set-AzVirtualNetworkTap** parancsmag frissíti a virtuális hálózatra való rákoppintást.</span><span class="sxs-lookup"><span data-stu-id="de362-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="de362-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de362-107">EXAMPLES</span></span>

### <span data-ttu-id="de362-108">1. példa: Virtuális hálózatra való koppintás konfigurálása</span><span class="sxs-lookup"><span data-stu-id="de362-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="de362-109">A parancs frissíti a Cél IpConfigurációt, és frissíti a virtuális hálózat koppintást.</span><span class="sxs-lookup"><span data-stu-id="de362-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="de362-110">Ha vannak rá vonatkozó koppintási konfigurációk, akkor a frissítés után a forrásforgalom nem indul el az új cél IP-konfigurációra tükrözve.</span><span class="sxs-lookup"><span data-stu-id="de362-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="de362-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de362-111">PARAMETERS</span></span>

### <span data-ttu-id="de362-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de362-112">-AsJob</span></span>
<span data-ttu-id="de362-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="de362-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de362-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de362-114">-DefaultProfile</span></span>
<span data-ttu-id="de362-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de362-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de362-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="de362-117">A virtuális hálózat koppintás</span><span class="sxs-lookup"><span data-stu-id="de362-117">The virtual network tap</span></span>

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

### <span data-ttu-id="de362-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de362-118">-Confirm</span></span>
<span data-ttu-id="de362-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de362-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de362-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de362-120">-WhatIf</span></span>
<span data-ttu-id="de362-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de362-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de362-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de362-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de362-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de362-123">CommonParameters</span></span>
<span data-ttu-id="de362-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de362-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de362-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de362-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de362-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de362-126">INPUTS</span></span>

### <span data-ttu-id="de362-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="de362-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de362-128">OUTPUTS</span></span>

### <span data-ttu-id="de362-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="de362-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de362-130">NOTES</span></span>

## <span data-ttu-id="de362-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de362-131">RELATED LINKS</span></span>

[<span data-ttu-id="de362-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="de362-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="de362-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="de362-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
