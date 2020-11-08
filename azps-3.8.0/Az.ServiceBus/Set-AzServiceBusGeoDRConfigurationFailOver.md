---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011090"
---
# <span data-ttu-id="cc8e9-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="cc8e9-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="cc8e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc8e9-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8e9-103">A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="cc8e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc8e9-104">SYNTAX</span></span>

### <span data-ttu-id="cc8e9-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc8e9-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc8e9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc8e9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc8e9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc8e9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc8e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc8e9-108">DESCRIPTION</span></span>
<span data-ttu-id="cc8e9-109">A **set-AzServiceBusGeoDRConfigurationFailOver** PARANCSMAG a Geo Dr feladatátvételt hívja meg, és átadja a másodlagos névtérre mutató aliast.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="cc8e9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cc8e9-110">EXAMPLES</span></span>

### <span data-ttu-id="cc8e9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc8e9-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="cc8e9-112">A feladatátvételt a "SampleDRConfigName" aliasra hívja, átirányítja, majd a másodlagos névtér "SampleNamespace_Secondary" elemre mutat.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="cc8e9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc8e9-113">PARAMETERS</span></span>

### <span data-ttu-id="cc8e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8e9-114">-DefaultProfile</span></span>
<span data-ttu-id="cc8e9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc8e9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc8e9-116">-InputObject</span></span>
<span data-ttu-id="cc8e9-117">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="cc8e9-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="cc8e9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc8e9-118">-Name</span></span>
<span data-ttu-id="cc8e9-119">DR konfigurációs név – alias</span><span class="sxs-lookup"><span data-stu-id="cc8e9-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="cc8e9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc8e9-120">-Namespace</span></span>
<span data-ttu-id="cc8e9-121">Névtér neve – másodlagos névtér</span><span class="sxs-lookup"><span data-stu-id="cc8e9-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="cc8e9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc8e9-122">-PassThru</span></span>
<span data-ttu-id="cc8e9-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc8e9-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc8e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc8e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc8e9-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cc8e9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cc8e9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc8e9-127">-ResourceId</span></span>
<span data-ttu-id="cc8e9-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cc8e9-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="cc8e9-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc8e9-129">-Confirm</span></span>
<span data-ttu-id="cc8e9-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc8e9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc8e9-131">-WhatIf</span></span>
<span data-ttu-id="cc8e9-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc8e9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc8e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8e9-134">CommonParameters</span></span>
<span data-ttu-id="cc8e9-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc8e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8e9-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc8e9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8e9-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc8e9-137">INPUTS</span></span>

### <span data-ttu-id="cc8e9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc8e9-138">System.String</span></span>

### <span data-ttu-id="cc8e9-139">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cc8e9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cc8e9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc8e9-140">OUTPUTS</span></span>

### <span data-ttu-id="cc8e9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc8e9-141">System.Boolean</span></span>

## <span data-ttu-id="cc8e9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc8e9-142">NOTES</span></span>

## <span data-ttu-id="cc8e9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc8e9-143">RELATED LINKS</span></span>
