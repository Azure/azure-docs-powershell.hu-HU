---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1c46cb01a2b30853248ca941cbb61d8b0429fc49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919890"
---
# <span data-ttu-id="1c6d9-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1c6d9-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="1c6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6d9-103">Koppintás konfigurációs erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="1c6d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c6d9-104">SYNTAX</span></span>

### <span data-ttu-id="1c6d9-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c6d9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c6d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c6d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6d9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c6d9-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6d9-108">A **Get-AzNetworkInterfaceTapConfig** parancsmag egy Azure Tap Configuration parancsmagot kap egy adott erőforráscsoporthoz, hálózati felülethez és koppintson a konfiguráció nevére vagy a koppintási konfigurációk listájára egy erőforráscsoportban és hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="1c6d9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c6d9-109">EXAMPLES</span></span>

### <span data-ttu-id="1c6d9-110">1. példa: Az adott hálózati felület összes koppintási konfigurációjának lekért beállítása</span><span class="sxs-lookup"><span data-stu-id="1c6d9-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="1c6d9-111">Ez a parancs koppintási beállításokat ad hozzá az adott hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="1c6d9-112">2. példa: Adott koppintási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="1c6d9-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="1c6d9-113">Ez a parancs konkrét koppintási konfigurációt ad hozzá az adott hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="1c6d9-114">3. példa: Adott koppintási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="1c6d9-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="1c6d9-115">Ez a parancs a "tapconfig" névvel kezdődő hálózati felületre vonatkozó koppintáskonfigurációkat kap.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="1c6d9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c6d9-116">PARAMETERS</span></span>

### <span data-ttu-id="1c6d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6d9-117">-DefaultProfile</span></span>
<span data-ttu-id="1c6d9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c6d9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1c6d9-119">-Name</span></span>
<span data-ttu-id="1c6d9-120">Az adott koppintási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="1c6d9-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1c6d9-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="1c6d9-122">A hálózati felület neve.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="1c6d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c6d9-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-124">The resource group name.</span></span>

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

### <span data-ttu-id="1c6d9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c6d9-125">-ResourceId</span></span>
<span data-ttu-id="1c6d9-126">A TapConfiguration erőforrás Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="1c6d9-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="1c6d9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c6d9-127">-Confirm</span></span>
<span data-ttu-id="1c6d9-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6d9-129">-WhatIf</span></span>
<span data-ttu-id="1c6d9-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c6d9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6d9-132">CommonParameters</span></span>
<span data-ttu-id="1c6d9-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6d9-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c6d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6d9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c6d9-135">INPUTS</span></span>

### <span data-ttu-id="1c6d9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1c6d9-136">System.String</span></span>

## <span data-ttu-id="1c6d9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6d9-137">OUTPUTS</span></span>

### <span data-ttu-id="1c6d9-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c6d9-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="1c6d9-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c6d9-139">NOTES</span></span>

## <span data-ttu-id="1c6d9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c6d9-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c6d9-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1c6d9-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="1c6d9-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1c6d9-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="1c6d9-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1c6d9-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
