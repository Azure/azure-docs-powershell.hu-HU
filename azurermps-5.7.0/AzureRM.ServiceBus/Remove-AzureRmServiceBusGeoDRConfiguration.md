---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498815"
---
# <span data-ttu-id="0f008-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f008-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="0f008-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f008-102">SYNOPSIS</span></span>
<span data-ttu-id="0f008-103">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="0f008-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f008-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f008-104">SYNTAX</span></span>

### <span data-ttu-id="0f008-105">GeoDRBreakPairFailOverPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f008-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f008-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f008-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f008-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f008-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f008-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f008-108">DESCRIPTION</span></span>
<span data-ttu-id="0f008-109">A **Remove-AzureRmServiceBusGeoDRConfiguration** parancsmag egy aliast töröl (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="0f008-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0f008-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f008-110">EXAMPLES</span></span>

### <span data-ttu-id="0f008-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f008-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="0f008-112">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="0f008-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0f008-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f008-113">PARAMETERS</span></span>

### <span data-ttu-id="0f008-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f008-114">-AsJob</span></span>
<span data-ttu-id="0f008-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f008-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f008-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f008-116">-DefaultProfile</span></span>
<span data-ttu-id="0f008-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f008-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f008-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f008-118">-InputObject</span></span>
<span data-ttu-id="0f008-119">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="0f008-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0f008-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f008-120">-Name</span></span>
<span data-ttu-id="0f008-121">Alias (GeoDR) neve</span><span class="sxs-lookup"><span data-stu-id="0f008-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="0f008-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f008-122">-Namespace</span></span>
<span data-ttu-id="0f008-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0f008-123">Namespace Name</span></span>

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

### <span data-ttu-id="0f008-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f008-124">-PassThru</span></span>
<span data-ttu-id="0f008-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0f008-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f008-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0f008-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f008-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f008-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f008-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0f008-128">Resource Group Name</span></span>

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

### <span data-ttu-id="0f008-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f008-129">-ResourceId</span></span>
<span data-ttu-id="0f008-130">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0f008-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0f008-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f008-131">-Confirm</span></span>
<span data-ttu-id="0f008-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f008-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f008-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f008-133">-WhatIf</span></span>
<span data-ttu-id="0f008-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f008-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f008-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f008-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f008-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f008-136">CommonParameters</span></span>
<span data-ttu-id="0f008-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f008-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0f008-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f008-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f008-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f008-139">INPUTS</span></span>

### <span data-ttu-id="0f008-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0f008-140">System.String</span></span>
<span data-ttu-id="0f008-141">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0f008-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="0f008-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f008-142">OUTPUTS</span></span>

### <span data-ttu-id="0f008-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f008-143">System.Boolean</span></span>


## <span data-ttu-id="0f008-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f008-144">NOTES</span></span>

## <span data-ttu-id="0f008-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f008-145">RELATED LINKS</span></span>
