---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680803"
---
# <span data-ttu-id="dba81-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="dba81-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="dba81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dba81-102">SYNOPSIS</span></span>
<span data-ttu-id="dba81-103">Egy koppintással konfigurálható erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="dba81-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dba81-104">SYNTAX</span></span>

### <span data-ttu-id="dba81-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dba81-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba81-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba81-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba81-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dba81-107">DESCRIPTION</span></span>
<span data-ttu-id="dba81-108">A **Get-AzureRmNetworkInterfaceTapConfig** parancsmag egy Azure TAP-konfigurációval rendelkezik egy adott erőforráscsoport esetén, a hálózati felületen, majd a konfiguráció neve vagy a TAP-konfigurációk listája egy erőforráscsoport-és hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="dba81-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="dba81-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dba81-109">EXAMPLES</span></span>

### <span data-ttu-id="dba81-110">1. példa: az összes koppintás-konfiguráció beolvasása egy adott hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="dba81-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="dba81-111">Ez a parancs a megadott hálózati csatolón hozzáadott konfigurációkra koppint.</span><span class="sxs-lookup"><span data-stu-id="dba81-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="dba81-112">2. példa: adott koppintás konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dba81-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="dba81-113">Ez a parancs a megadott hálózati interfészhez adott koppintás-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="dba81-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="dba81-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dba81-114">PARAMETERS</span></span>

### <span data-ttu-id="dba81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba81-115">-DefaultProfile</span></span>
<span data-ttu-id="dba81-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dba81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba81-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dba81-117">-Name</span></span>
<span data-ttu-id="dba81-118">Az adott koppintás konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="dba81-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba81-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="dba81-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="dba81-120">A hálózati kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="dba81-120">The Network Interface name.</span></span>

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

### <span data-ttu-id="dba81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba81-121">-ResourceGroupName</span></span>
<span data-ttu-id="dba81-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dba81-122">The resource group name.</span></span>

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

### <span data-ttu-id="dba81-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba81-123">-ResourceId</span></span>
<span data-ttu-id="dba81-124">A TapConfiguration-erőforrás ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba81-124">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="dba81-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dba81-125">-Confirm</span></span>
<span data-ttu-id="dba81-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dba81-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba81-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba81-127">-WhatIf</span></span>
<span data-ttu-id="dba81-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dba81-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dba81-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dba81-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba81-130">CommonParameters</span></span>
<span data-ttu-id="dba81-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dba81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba81-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba81-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba81-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba81-133">INPUTS</span></span>

### <span data-ttu-id="dba81-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dba81-134">System.String</span></span>

## <span data-ttu-id="dba81-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba81-135">OUTPUTS</span></span>

### <span data-ttu-id="dba81-136">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="dba81-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="dba81-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dba81-137">NOTES</span></span>

## <span data-ttu-id="dba81-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dba81-138">RELATED LINKS</span></span>
