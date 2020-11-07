---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 85f6373cad3c6c42bbefa0aba9aac14d3699b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672614"
---
# <span data-ttu-id="f634b-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f634b-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f634b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f634b-102">SYNOPSIS</span></span>
<span data-ttu-id="f634b-103">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f634b-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f634b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f634b-104">SYNTAX</span></span>

### <span data-ttu-id="f634b-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f634b-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f634b-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f634b-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f634b-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f634b-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f634b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f634b-108">DESCRIPTION</span></span>
<span data-ttu-id="f634b-109">A **Remove-AzureRmEventHubGeoDRConfiguration** parancsmag egy aliast töröl (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f634b-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f634b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f634b-110">EXAMPLES</span></span>

### <span data-ttu-id="f634b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f634b-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="f634b-112">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="f634b-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f634b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f634b-113">PARAMETERS</span></span>

### <span data-ttu-id="f634b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f634b-114">-AsJob</span></span>
<span data-ttu-id="f634b-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f634b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f634b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f634b-116">-DefaultProfile</span></span>
<span data-ttu-id="f634b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f634b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f634b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f634b-118">-InputObject</span></span>
<span data-ttu-id="f634b-119">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="f634b-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f634b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f634b-120">-Name</span></span>
<span data-ttu-id="f634b-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="f634b-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f634b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f634b-122">-Namespace</span></span>
<span data-ttu-id="f634b-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f634b-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f634b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f634b-124">-PassThru</span></span>
<span data-ttu-id="f634b-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f634b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f634b-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f634b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f634b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f634b-127">-ResourceGroupName</span></span>
<span data-ttu-id="f634b-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f634b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f634b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f634b-129">-ResourceId</span></span>
<span data-ttu-id="f634b-130">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f634b-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f634b-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f634b-131">-Confirm</span></span>
<span data-ttu-id="f634b-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f634b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f634b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f634b-133">-WhatIf</span></span>
<span data-ttu-id="f634b-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f634b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f634b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f634b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f634b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f634b-136">CommonParameters</span></span>
<span data-ttu-id="f634b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f634b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f634b-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f634b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f634b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f634b-139">INPUTS</span></span>

### <span data-ttu-id="f634b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f634b-140">System.String</span></span>

### <span data-ttu-id="f634b-141">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f634b-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="f634b-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f634b-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f634b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f634b-143">OUTPUTS</span></span>

### <span data-ttu-id="f634b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f634b-144">System.Boolean</span></span>

## <span data-ttu-id="f634b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f634b-145">NOTES</span></span>

## <span data-ttu-id="f634b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f634b-146">RELATED LINKS</span></span>
