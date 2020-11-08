---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013319"
---
# <span data-ttu-id="4131d-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4131d-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="4131d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4131d-102">SYNOPSIS</span></span>
<span data-ttu-id="4131d-103">Egy koppintással konfigurálható erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="4131d-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="4131d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4131d-104">SYNTAX</span></span>

### <span data-ttu-id="4131d-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4131d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4131d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4131d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4131d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4131d-107">DESCRIPTION</span></span>
<span data-ttu-id="4131d-108">A **Get-AzNetworkInterfaceTapConfig** parancsmag egy Azure TAP-konfigurációval rendelkezik egy adott erőforráscsoport esetén, a hálózati felületen, majd a konfiguráció neve vagy a TAP-konfigurációk listája egy erőforráscsoport-és hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="4131d-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="4131d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4131d-109">EXAMPLES</span></span>

### <span data-ttu-id="4131d-110">1. példa: az összes koppintás-konfiguráció beolvasása egy adott hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="4131d-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="4131d-111">Ez a parancs a megadott hálózati csatolón hozzáadott konfigurációkra koppint.</span><span class="sxs-lookup"><span data-stu-id="4131d-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="4131d-112">2. példa: adott koppintás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4131d-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="4131d-113">Ez a parancs a megadott hálózati interfészhez adott koppintás-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="4131d-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="4131d-114">3. példa: adott koppintás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4131d-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="4131d-115">Ez a parancs a "tapconfig" névvel kezdődő nevű hálózati interfészhez koppintva koppint a beállításokra.</span><span class="sxs-lookup"><span data-stu-id="4131d-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="4131d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4131d-116">PARAMETERS</span></span>

### <span data-ttu-id="4131d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4131d-117">-DefaultProfile</span></span>
<span data-ttu-id="4131d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4131d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4131d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4131d-119">-Name</span></span>
<span data-ttu-id="4131d-120">Az adott koppintás konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="4131d-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4131d-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4131d-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="4131d-122">A hálózati kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="4131d-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4131d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4131d-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4131d-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4131d-125">-ResourceId</span></span>
<span data-ttu-id="4131d-126">A TapConfiguration-erőforrás ResourceId</span><span class="sxs-lookup"><span data-stu-id="4131d-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4131d-127">-Confirm</span></span>
<span data-ttu-id="4131d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4131d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4131d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4131d-129">-WhatIf</span></span>
<span data-ttu-id="4131d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4131d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4131d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4131d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4131d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4131d-132">CommonParameters</span></span>
<span data-ttu-id="4131d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4131d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4131d-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4131d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4131d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4131d-135">INPUTS</span></span>

### <span data-ttu-id="4131d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4131d-136">System.String</span></span>

## <span data-ttu-id="4131d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4131d-137">OUTPUTS</span></span>

### <span data-ttu-id="4131d-138">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="4131d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="4131d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4131d-139">NOTES</span></span>

## <span data-ttu-id="4131d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4131d-140">RELATED LINKS</span></span>

[<span data-ttu-id="4131d-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4131d-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4131d-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4131d-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4131d-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4131d-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
