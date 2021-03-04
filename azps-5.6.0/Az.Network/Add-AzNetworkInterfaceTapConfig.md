---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933841"
---
# <span data-ttu-id="190f3-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="190f3-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="190f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="190f3-102">SYNOPSIS</span></span>
<span data-ttu-id="190f3-103">Egy NetworkInterface-hez társított TapConfiguration erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="190f3-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="190f3-104">Ez egy meglévő VirtualNetworkTap erőforrásra fog hivatkozni.</span><span class="sxs-lookup"><span data-stu-id="190f3-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="190f3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="190f3-105">SYNTAX</span></span>

### <span data-ttu-id="190f3-106">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="190f3-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="190f3-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="190f3-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="190f3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="190f3-108">DESCRIPTION</span></span>
<span data-ttu-id="190f3-109">Az **Add-AzNetworkInterfaceTapConfig** parancsmag létrehoz egy NetworkInterface-hez társított TapConfiguration erőforrást.</span><span class="sxs-lookup"><span data-stu-id="190f3-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="190f3-110">Ez egy meglévő VirtualNetworkTap erőforrásra fog hivatkozni.</span><span class="sxs-lookup"><span data-stu-id="190f3-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="190f3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="190f3-111">EXAMPLES</span></span>

### <span data-ttu-id="190f3-112">1. példa: TapConfiguration hozzáadása egy adott NetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="190f3-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="190f3-113">Adja hozzá a TapConfiguration bővítményt a sourceNic fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="190f3-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="190f3-114">A sourceNic VM-ről származó forgalom a vVirtualNetworkTap erőforrásban hivatkozott cél VM-re lesz tükrözve.</span><span class="sxs-lookup"><span data-stu-id="190f3-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="190f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="190f3-115">PARAMETERS</span></span>

### <span data-ttu-id="190f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190f3-116">-DefaultProfile</span></span>
<span data-ttu-id="190f3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="190f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190f3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="190f3-118">-Name</span></span>
<span data-ttu-id="190f3-119">A koppintás konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="190f3-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f3-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="190f3-120">-NetworkInterface</span></span>
<span data-ttu-id="190f3-121">A hálózati felület erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="190f3-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="190f3-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="190f3-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="190f3-123">A virtuális hálózat koppintási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="190f3-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="190f3-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="190f3-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="190f3-125">A virtuális hálózat koppintási erőforrásának hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="190f3-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="190f3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="190f3-126">-Confirm</span></span>
<span data-ttu-id="190f3-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="190f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190f3-128">-WhatIf</span></span>
<span data-ttu-id="190f3-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="190f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="190f3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="190f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190f3-131">CommonParameters</span></span>
<span data-ttu-id="190f3-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190f3-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190f3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="190f3-134">INPUTS</span></span>

### <span data-ttu-id="190f3-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="190f3-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="190f3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="190f3-136">System.String</span></span>

### <span data-ttu-id="190f3-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="190f3-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="190f3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="190f3-138">OUTPUTS</span></span>

### <span data-ttu-id="190f3-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="190f3-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="190f3-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="190f3-140">NOTES</span></span>

## <span data-ttu-id="190f3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="190f3-141">RELATED LINKS</span></span>

[<span data-ttu-id="190f3-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="190f3-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="190f3-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="190f3-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="190f3-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="190f3-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
