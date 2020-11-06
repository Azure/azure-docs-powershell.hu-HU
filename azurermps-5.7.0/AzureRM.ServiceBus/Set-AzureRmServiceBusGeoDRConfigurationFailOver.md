---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 1a6fc5bca4c31afe08591190c111649495555cde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498807"
---
# <span data-ttu-id="1e0e1-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="1e0e1-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="1e0e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0e1-103">A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e0e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e0e1-104">SYNTAX</span></span>

### <span data-ttu-id="1e0e1-105">GeoDRBreakPairFailOverPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e0e1-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e0e1-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e0e1-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e0e1-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e0e1-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e0e1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e0e1-108">DESCRIPTION</span></span>
<span data-ttu-id="1e0e1-109">A **set-AzureRmServiceBusGeoDRConfigurationFailOver** PARANCSMAG ENVOKES geo Dr feladatátvételi lehetőséget, és átállíthatja az aliast, hogy a másodlagos névtérre mutasson</span><span class="sxs-lookup"><span data-stu-id="1e0e1-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="1e0e1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e0e1-110">EXAMPLES</span></span>

### <span data-ttu-id="1e0e1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e0e1-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="1e0e1-112">A feladatátvételt a "SampleDRCongifName" aliasra hívja, átirányítja, majd a másodlagos névtér "SampleNamespace_Secondary" elemre mutat.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="1e0e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e0e1-113">PARAMETERS</span></span>

### <span data-ttu-id="1e0e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0e1-114">-DefaultProfile</span></span>
<span data-ttu-id="1e0e1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e0e1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e0e1-116">-InputObject</span></span>
<span data-ttu-id="1e0e1-117">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="1e0e1-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0e1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e0e1-118">-Name</span></span>
<span data-ttu-id="1e0e1-119">DR konfigurációs név – alias</span><span class="sxs-lookup"><span data-stu-id="1e0e1-119">DR Configuration Name - Alias</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0e1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e0e1-120">-Namespace</span></span>
<span data-ttu-id="1e0e1-121">Névtér neve – másodlagos névtér</span><span class="sxs-lookup"><span data-stu-id="1e0e1-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0e1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e0e1-122">-PassThru</span></span>
<span data-ttu-id="1e0e1-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1e0e1-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1e0e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="1e0e1-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1e0e1-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0e1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e0e1-127">-ResourceId</span></span>
<span data-ttu-id="1e0e1-128">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="1e0e1-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0e1-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e0e1-129">-Confirm</span></span>
<span data-ttu-id="1e0e1-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e0e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0e1-131">-WhatIf</span></span>
<span data-ttu-id="1e0e1-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e0e1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e0e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e0e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0e1-134">CommonParameters</span></span>
<span data-ttu-id="1e0e1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e0e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1e0e1-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e0e1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0e1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e0e1-137">INPUTS</span></span>

### <span data-ttu-id="1e0e1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1e0e1-138">System.String</span></span>
<span data-ttu-id="1e0e1-139">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1e0e1-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="1e0e1-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e0e1-140">OUTPUTS</span></span>

### <span data-ttu-id="1e0e1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e0e1-141">System.Boolean</span></span>


## <span data-ttu-id="1e0e1-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e0e1-142">NOTES</span></span>

## <span data-ttu-id="1e0e1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e0e1-143">RELATED LINKS</span></span>
