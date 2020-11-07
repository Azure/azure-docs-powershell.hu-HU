---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 981ef70f711cf418a92d8fb0caaae22c114f96b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850377"
---
# <span data-ttu-id="dd994-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd994-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="dd994-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd994-102">SYNOPSIS</span></span>
<span data-ttu-id="dd994-103">Új útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dd994-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd994-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd994-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd994-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd994-105">DESCRIPTION</span></span>
<span data-ttu-id="dd994-106">Az New-AzureRmRouteFilter parancsmag egy Azure-útvonal-szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dd994-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="dd994-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd994-107">EXAMPLES</span></span>

### <span data-ttu-id="dd994-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd994-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="dd994-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="dd994-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="dd994-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd994-110">PARAMETERS</span></span>

### <span data-ttu-id="dd994-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd994-111">-AsJob</span></span>
<span data-ttu-id="dd994-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd994-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd994-113">-DefaultProfile</span></span>
<span data-ttu-id="dd994-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd994-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dd994-115">-Force</span></span>
<span data-ttu-id="dd994-116">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útvonal-szűrő.</span><span class="sxs-lookup"><span data-stu-id="dd994-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="dd994-117">-Location</span></span>
<span data-ttu-id="dd994-118">Azt az Azure-területet adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="dd994-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd994-119">-Name</span></span>
<span data-ttu-id="dd994-120">Az útvonal-szűrő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd994-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd994-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd994-122">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útvonal-szűrőt.</span><span class="sxs-lookup"><span data-stu-id="dd994-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-123">-Szabály</span><span class="sxs-lookup"><span data-stu-id="dd994-123">-Rule</span></span>
<span data-ttu-id="dd994-124">Az útválasztási szűrő szabályait tartalmazó objektumok tömbjét adja meg az útvonal-szűrőhöz társítva.</span><span class="sxs-lookup"><span data-stu-id="dd994-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="dd994-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="dd994-125">-Tag</span></span>
<span data-ttu-id="dd994-126">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="dd994-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dd994-127">Példa:</span><span class="sxs-lookup"><span data-stu-id="dd994-127">For example:</span></span>

<span data-ttu-id="dd994-128">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="dd994-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd994-129">-Confirm</span></span>
<span data-ttu-id="dd994-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd994-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd994-131">-WhatIf</span></span>
<span data-ttu-id="dd994-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd994-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd994-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd994-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd994-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd994-134">CommonParameters</span></span>
<span data-ttu-id="dd994-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd994-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd994-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd994-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd994-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd994-137">INPUTS</span></span>

## <span data-ttu-id="dd994-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd994-138">OUTPUTS</span></span>

### <span data-ttu-id="dd994-139">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd994-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="dd994-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd994-140">NOTES</span></span>
<span data-ttu-id="dd994-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="dd994-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dd994-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd994-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd994-143">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd994-143">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="dd994-144">Új – AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd994-144">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="dd994-145">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd994-145">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="dd994-146">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd994-146">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
