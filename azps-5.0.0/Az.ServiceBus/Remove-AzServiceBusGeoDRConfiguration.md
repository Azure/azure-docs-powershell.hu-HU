---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186540"
---
# <span data-ttu-id="f5ac3-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5ac3-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f5ac3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ac3-103">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f5ac3-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5ac3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5ac3-104">SYNTAX</span></span>

### <span data-ttu-id="f5ac3-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5ac3-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ac3-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5ac3-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ac3-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5ac3-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ac3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5ac3-108">DESCRIPTION</span></span>
<span data-ttu-id="f5ac3-109">A **Remove-AzServiceBusGeoDRConfiguration** parancsmag egy aliast töröl (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f5ac3-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5ac3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5ac3-110">EXAMPLES</span></span>

### <span data-ttu-id="f5ac3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5ac3-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f5ac3-112">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f5ac3-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f5ac3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5ac3-113">PARAMETERS</span></span>

### <span data-ttu-id="f5ac3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5ac3-114">-AsJob</span></span>
<span data-ttu-id="f5ac3-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5ac3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5ac3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ac3-116">-DefaultProfile</span></span>
<span data-ttu-id="f5ac3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ac3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ac3-118">-InputObject</span></span>
<span data-ttu-id="f5ac3-119">A Service Bus GeoDR konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="f5ac3-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="f5ac3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5ac3-120">-Name</span></span>
<span data-ttu-id="f5ac3-121">Alias (GeoDR) neve</span><span class="sxs-lookup"><span data-stu-id="f5ac3-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="f5ac3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5ac3-122">-Namespace</span></span>
<span data-ttu-id="f5ac3-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f5ac3-123">Namespace Name</span></span>

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

### <span data-ttu-id="f5ac3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5ac3-124">-PassThru</span></span>
<span data-ttu-id="f5ac3-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5ac3-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5ac3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ac3-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5ac3-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f5ac3-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f5ac3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ac3-129">-ResourceId</span></span>
<span data-ttu-id="f5ac3-130">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f5ac3-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f5ac3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5ac3-131">-Confirm</span></span>
<span data-ttu-id="f5ac3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ac3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ac3-133">-WhatIf</span></span>
<span data-ttu-id="f5ac3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ac3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5ac3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ac3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ac3-136">CommonParameters</span></span>
<span data-ttu-id="f5ac3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5ac3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ac3-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ac3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ac3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ac3-139">INPUTS</span></span>

### <span data-ttu-id="f5ac3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5ac3-140">System.String</span></span>

### <span data-ttu-id="f5ac3-141">Microsoft. Azure. Command. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f5ac3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f5ac3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ac3-142">OUTPUTS</span></span>

### <span data-ttu-id="f5ac3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5ac3-143">System.Boolean</span></span>

## <span data-ttu-id="f5ac3-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5ac3-144">NOTES</span></span>

## <span data-ttu-id="f5ac3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5ac3-145">RELATED LINKS</span></span>
