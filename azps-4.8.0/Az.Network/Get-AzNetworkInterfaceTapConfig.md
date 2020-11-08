---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180563"
---
# <span data-ttu-id="08a25-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="08a25-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="08a25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08a25-102">SYNOPSIS</span></span>
<span data-ttu-id="08a25-103">Egy koppintással konfigurálható erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="08a25-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="08a25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08a25-104">SYNTAX</span></span>

### <span data-ttu-id="08a25-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08a25-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a25-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08a25-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a25-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="08a25-107">DESCRIPTION</span></span>
<span data-ttu-id="08a25-108">A **Get-AzNetworkInterfaceTapConfig** parancsmag egy Azure TAP-konfigurációval rendelkezik egy adott erőforráscsoport esetén, a hálózati felületen, majd a konfiguráció neve vagy a TAP-konfigurációk listája egy erőforráscsoport-és hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="08a25-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="08a25-109">Példák</span><span class="sxs-lookup"><span data-stu-id="08a25-109">EXAMPLES</span></span>

### <span data-ttu-id="08a25-110">1. példa: az összes koppintás-konfiguráció beolvasása egy adott hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="08a25-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="08a25-111">Ez a parancs a megadott hálózati csatolón hozzáadott konfigurációkra koppint.</span><span class="sxs-lookup"><span data-stu-id="08a25-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="08a25-112">2. példa: adott koppintás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="08a25-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="08a25-113">Ez a parancs a megadott hálózati interfészhez adott koppintás-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="08a25-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="08a25-114">3. példa: adott koppintás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="08a25-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="08a25-115">Ez a parancs a "tapconfig" névvel kezdődő nevű hálózati interfészhez koppintva koppint a beállításokra.</span><span class="sxs-lookup"><span data-stu-id="08a25-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="08a25-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08a25-116">PARAMETERS</span></span>

### <span data-ttu-id="08a25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a25-117">-DefaultProfile</span></span>
<span data-ttu-id="08a25-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08a25-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08a25-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08a25-119">-Name</span></span>
<span data-ttu-id="08a25-120">Az adott koppintás konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="08a25-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="08a25-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="08a25-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="08a25-122">A hálózati kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="08a25-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="08a25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a25-123">-ResourceGroupName</span></span>
<span data-ttu-id="08a25-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="08a25-124">The resource group name.</span></span>

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

### <span data-ttu-id="08a25-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08a25-125">-ResourceId</span></span>
<span data-ttu-id="08a25-126">A TapConfiguration-erőforrás ResourceId</span><span class="sxs-lookup"><span data-stu-id="08a25-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="08a25-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08a25-127">-Confirm</span></span>
<span data-ttu-id="08a25-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08a25-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a25-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a25-129">-WhatIf</span></span>
<span data-ttu-id="08a25-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08a25-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08a25-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08a25-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a25-132">CommonParameters</span></span>
<span data-ttu-id="08a25-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08a25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a25-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08a25-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a25-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08a25-135">INPUTS</span></span>

### <span data-ttu-id="08a25-136">System. String</span><span class="sxs-lookup"><span data-stu-id="08a25-136">System.String</span></span>

## <span data-ttu-id="08a25-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08a25-137">OUTPUTS</span></span>

### <span data-ttu-id="08a25-138">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="08a25-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="08a25-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08a25-139">NOTES</span></span>

## <span data-ttu-id="08a25-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08a25-140">RELATED LINKS</span></span>

[<span data-ttu-id="08a25-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="08a25-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="08a25-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="08a25-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="08a25-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="08a25-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
