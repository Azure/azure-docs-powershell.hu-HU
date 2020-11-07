---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: b89772c1afe621e456dfb269fe869b6cd3fa8a8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670281"
---
# <span data-ttu-id="90504-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90504-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="90504-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90504-102">SYNOPSIS</span></span>
<span data-ttu-id="90504-103">Új útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="90504-103">Creates a route filter.</span></span>

## <span data-ttu-id="90504-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90504-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90504-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90504-105">DESCRIPTION</span></span>
<span data-ttu-id="90504-106">Az New-AzRouteFilter parancsmag egy Azure-útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="90504-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="90504-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90504-107">EXAMPLES</span></span>

### <span data-ttu-id="90504-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90504-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="90504-109">A parancs új útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="90504-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="90504-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90504-110">PARAMETERS</span></span>

### <span data-ttu-id="90504-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90504-111">-AsJob</span></span>
<span data-ttu-id="90504-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="90504-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90504-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90504-113">-DefaultProfile</span></span>
<span data-ttu-id="90504-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90504-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90504-115">-Force</span><span class="sxs-lookup"><span data-stu-id="90504-115">-Force</span></span>
<span data-ttu-id="90504-116">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útvonal-szűrő.</span><span class="sxs-lookup"><span data-stu-id="90504-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="90504-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="90504-117">-Location</span></span>
<span data-ttu-id="90504-118">Azt az Azure-területet adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="90504-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="90504-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90504-119">-Name</span></span>
<span data-ttu-id="90504-120">Az útvonal-szűrő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90504-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90504-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90504-121">-ResourceGroupName</span></span>
<span data-ttu-id="90504-122">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="90504-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="90504-123">-Szabály</span><span class="sxs-lookup"><span data-stu-id="90504-123">-Rule</span></span>
<span data-ttu-id="90504-124">Az útválasztási szűrő szabályait tartalmazó objektumok tömbjét adja meg az útvonal-szűrőhöz társítva.</span><span class="sxs-lookup"><span data-stu-id="90504-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90504-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="90504-125">-Tag</span></span>
<span data-ttu-id="90504-126">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="90504-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="90504-127">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="90504-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90504-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90504-128">-Confirm</span></span>
<span data-ttu-id="90504-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90504-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90504-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90504-130">-WhatIf</span></span>
<span data-ttu-id="90504-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90504-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90504-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90504-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90504-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90504-133">CommonParameters</span></span>
<span data-ttu-id="90504-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90504-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90504-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90504-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90504-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90504-136">INPUTS</span></span>

### <span data-ttu-id="90504-137">System. String</span><span class="sxs-lookup"><span data-stu-id="90504-137">System.String</span></span>

### <span data-ttu-id="90504-138">Microsoft. Azure. commands. Network. models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="90504-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="90504-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90504-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90504-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90504-140">OUTPUTS</span></span>

### <span data-ttu-id="90504-141">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90504-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="90504-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90504-142">NOTES</span></span>
<span data-ttu-id="90504-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="90504-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="90504-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90504-144">RELATED LINKS</span></span>

[<span data-ttu-id="90504-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90504-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="90504-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90504-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="90504-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90504-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="90504-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90504-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90504-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90504-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90504-150">Új – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90504-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90504-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90504-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90504-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90504-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
