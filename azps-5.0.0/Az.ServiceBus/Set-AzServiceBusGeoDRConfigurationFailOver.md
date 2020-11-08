---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186714"
---
# <span data-ttu-id="e034b-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="e034b-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="e034b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e034b-102">SYNOPSIS</span></span>
<span data-ttu-id="e034b-103">A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.</span><span class="sxs-lookup"><span data-stu-id="e034b-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e034b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e034b-104">SYNTAX</span></span>

### <span data-ttu-id="e034b-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e034b-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e034b-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e034b-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e034b-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e034b-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e034b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e034b-108">DESCRIPTION</span></span>
<span data-ttu-id="e034b-109">A **set-AzServiceBusGeoDRConfigurationFailOver** PARANCSMAG a Geo Dr feladatátvételt hívja meg, és átadja a másodlagos névtérre mutató aliast.</span><span class="sxs-lookup"><span data-stu-id="e034b-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e034b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e034b-110">EXAMPLES</span></span>

### <span data-ttu-id="e034b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e034b-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e034b-112">A feladatátvételt a "SampleDRConfigName" aliasra hívja, átirányítja, majd a másodlagos névtér "SampleNamespace_Secondary" elemre mutat.</span><span class="sxs-lookup"><span data-stu-id="e034b-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e034b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e034b-113">PARAMETERS</span></span>

### <span data-ttu-id="e034b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e034b-114">-DefaultProfile</span></span>
<span data-ttu-id="e034b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e034b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e034b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e034b-116">-InputObject</span></span>
<span data-ttu-id="e034b-117">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="e034b-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e034b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e034b-118">-Name</span></span>
<span data-ttu-id="e034b-119">DR konfigurációs név – alias</span><span class="sxs-lookup"><span data-stu-id="e034b-119">DR Configuration Name - Alias</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e034b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e034b-120">-Namespace</span></span>
<span data-ttu-id="e034b-121">Névtér neve – másodlagos névtér</span><span class="sxs-lookup"><span data-stu-id="e034b-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e034b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e034b-122">-PassThru</span></span>
<span data-ttu-id="e034b-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e034b-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e034b-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e034b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e034b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e034b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e034b-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e034b-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e034b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e034b-127">-ResourceId</span></span>
<span data-ttu-id="e034b-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e034b-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e034b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e034b-129">-Confirm</span></span>
<span data-ttu-id="e034b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e034b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e034b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e034b-131">-WhatIf</span></span>
<span data-ttu-id="e034b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e034b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e034b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e034b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e034b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e034b-134">CommonParameters</span></span>
<span data-ttu-id="e034b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e034b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e034b-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e034b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e034b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e034b-137">INPUTS</span></span>

### <span data-ttu-id="e034b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e034b-138">System.String</span></span>

### <span data-ttu-id="e034b-139">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e034b-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e034b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e034b-140">OUTPUTS</span></span>

### <span data-ttu-id="e034b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e034b-141">System.Boolean</span></span>

## <span data-ttu-id="e034b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e034b-142">NOTES</span></span>

## <span data-ttu-id="e034b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e034b-143">RELATED LINKS</span></span>
