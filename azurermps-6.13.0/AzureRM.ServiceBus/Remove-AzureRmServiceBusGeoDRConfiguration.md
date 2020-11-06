---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494912"
---
# <span data-ttu-id="bc124-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc124-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="bc124-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc124-102">SYNOPSIS</span></span>
<span data-ttu-id="bc124-103">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="bc124-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc124-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc124-104">SYNTAX</span></span>

### <span data-ttu-id="bc124-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc124-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc124-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bc124-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc124-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc124-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc124-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc124-108">DESCRIPTION</span></span>
<span data-ttu-id="bc124-109">A **Remove-AzureRmServiceBusGeoDRConfiguration** parancsmag egy aliast töröl (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="bc124-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="bc124-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bc124-110">EXAMPLES</span></span>

### <span data-ttu-id="bc124-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc124-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="bc124-112">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="bc124-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="bc124-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc124-113">PARAMETERS</span></span>

### <span data-ttu-id="bc124-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc124-114">-AsJob</span></span>
<span data-ttu-id="bc124-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bc124-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc124-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc124-116">-DefaultProfile</span></span>
<span data-ttu-id="bc124-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc124-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc124-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc124-118">-InputObject</span></span>
<span data-ttu-id="bc124-119">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="bc124-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="bc124-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc124-120">-Name</span></span>
<span data-ttu-id="bc124-121">Alias (GeoDR) neve</span><span class="sxs-lookup"><span data-stu-id="bc124-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="bc124-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bc124-122">-Namespace</span></span>
<span data-ttu-id="bc124-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="bc124-123">Namespace Name</span></span>

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

### <span data-ttu-id="bc124-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc124-124">-PassThru</span></span>
<span data-ttu-id="bc124-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bc124-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc124-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="bc124-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bc124-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc124-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc124-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bc124-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bc124-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc124-129">-ResourceId</span></span>
<span data-ttu-id="bc124-130">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="bc124-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="bc124-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc124-131">-Confirm</span></span>
<span data-ttu-id="bc124-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc124-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc124-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc124-133">-WhatIf</span></span>
<span data-ttu-id="bc124-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc124-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc124-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc124-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc124-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc124-136">CommonParameters</span></span>
<span data-ttu-id="bc124-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc124-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc124-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc124-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc124-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc124-139">INPUTS</span></span>

### <span data-ttu-id="bc124-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bc124-140">System.String</span></span>

### <span data-ttu-id="bc124-141">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bc124-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="bc124-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc124-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bc124-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc124-143">OUTPUTS</span></span>

### <span data-ttu-id="bc124-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc124-144">System.Boolean</span></span>

## <span data-ttu-id="bc124-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc124-145">NOTES</span></span>

## <span data-ttu-id="bc124-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc124-146">RELATED LINKS</span></span>
