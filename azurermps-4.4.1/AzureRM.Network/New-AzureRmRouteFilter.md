---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494829"
---
# <span data-ttu-id="36cc5-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="36cc5-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="36cc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="36cc5-103">Új útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36cc5-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36cc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36cc5-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36cc5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="36cc5-106">Az New-AzureRmRouteFilter parancsmag egy Azure-útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36cc5-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="36cc5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36cc5-107">EXAMPLES</span></span>

### <span data-ttu-id="36cc5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36cc5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="36cc5-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="36cc5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="36cc5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36cc5-110">PARAMETERS</span></span>

### <span data-ttu-id="36cc5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="36cc5-111">-Force</span></span>
<span data-ttu-id="36cc5-112">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útvonal-szűrő.</span><span class="sxs-lookup"><span data-stu-id="36cc5-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="36cc5-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="36cc5-113">-Location</span></span>
<span data-ttu-id="36cc5-114">Azt az Azure-területet adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="36cc5-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="36cc5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36cc5-115">-Name</span></span>
<span data-ttu-id="36cc5-116">Az útvonal-szűrő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36cc5-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="36cc5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cc5-117">-ResourceGroupName</span></span>
<span data-ttu-id="36cc5-118">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="36cc5-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="36cc5-119">-Szabály</span><span class="sxs-lookup"><span data-stu-id="36cc5-119">-Rule</span></span>
<span data-ttu-id="36cc5-120">Az útválasztási szűrő szabályait tartalmazó objektumok tömbjét adja meg az útvonal-szűrőhöz társítva.</span><span class="sxs-lookup"><span data-stu-id="36cc5-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cc5-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="36cc5-121">-Tag</span></span>
<span data-ttu-id="36cc5-122">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="36cc5-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36cc5-123">Példa:</span><span class="sxs-lookup"><span data-stu-id="36cc5-123">For example:</span></span>

<span data-ttu-id="36cc5-124">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="36cc5-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36cc5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36cc5-125">-Confirm</span></span>
<span data-ttu-id="36cc5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36cc5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36cc5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36cc5-127">-WhatIf</span></span>
<span data-ttu-id="36cc5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36cc5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36cc5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36cc5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36cc5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cc5-130">-DefaultProfile</span></span>
<span data-ttu-id="36cc5-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36cc5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36cc5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cc5-132">CommonParameters</span></span>
<span data-ttu-id="36cc5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36cc5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cc5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cc5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cc5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36cc5-135">INPUTS</span></span>

## <span data-ttu-id="36cc5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36cc5-136">OUTPUTS</span></span>

### <span data-ttu-id="36cc5-137">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="36cc5-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="36cc5-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36cc5-138">NOTES</span></span>
<span data-ttu-id="36cc5-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="36cc5-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="36cc5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36cc5-140">RELATED LINKS</span></span>

[<span data-ttu-id="36cc5-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="36cc5-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="36cc5-142">Új – AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36cc5-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="36cc5-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="36cc5-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="36cc5-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="36cc5-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
