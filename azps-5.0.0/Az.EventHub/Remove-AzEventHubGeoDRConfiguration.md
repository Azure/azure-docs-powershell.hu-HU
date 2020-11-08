---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194782"
---
# <span data-ttu-id="6d605-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d605-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="6d605-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d605-102">SYNOPSIS</span></span>
<span data-ttu-id="6d605-103">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="6d605-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6d605-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d605-104">SYNTAX</span></span>

### <span data-ttu-id="6d605-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d605-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d605-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6d605-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d605-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d605-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d605-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d605-108">DESCRIPTION</span></span>
<span data-ttu-id="6d605-109">A **Remove-AzEventHubGeoDRConfiguration** parancsmag egy aliast töröl (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="6d605-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6d605-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6d605-110">EXAMPLES</span></span>

### <span data-ttu-id="6d605-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6d605-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="6d605-112">Alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="6d605-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6d605-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d605-113">PARAMETERS</span></span>

### <span data-ttu-id="6d605-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d605-114">-AsJob</span></span>
<span data-ttu-id="6d605-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6d605-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d605-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d605-116">-DefaultProfile</span></span>
<span data-ttu-id="6d605-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d605-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d605-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d605-118">-InputObject</span></span>
<span data-ttu-id="6d605-119">Eventhub GeoDR konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="6d605-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="6d605-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d605-120">-Name</span></span>
<span data-ttu-id="6d605-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="6d605-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="6d605-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d605-122">-Namespace</span></span>
<span data-ttu-id="6d605-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6d605-123">Namespace Name</span></span>

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

### <span data-ttu-id="6d605-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d605-124">-PassThru</span></span>
<span data-ttu-id="6d605-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6d605-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6d605-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6d605-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6d605-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d605-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d605-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6d605-128">Resource Group Name</span></span>

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

### <span data-ttu-id="6d605-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d605-129">-ResourceId</span></span>
<span data-ttu-id="6d605-130">GeoDRConfiguration erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="6d605-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="6d605-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d605-131">-Confirm</span></span>
<span data-ttu-id="6d605-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d605-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d605-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d605-133">-WhatIf</span></span>
<span data-ttu-id="6d605-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d605-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d605-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d605-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d605-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d605-136">CommonParameters</span></span>
<span data-ttu-id="6d605-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d605-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d605-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d605-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d605-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d605-139">INPUTS</span></span>

### <span data-ttu-id="6d605-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d605-140">System.String</span></span>

### <span data-ttu-id="6d605-141">Microsoft. Azure. Command. EventHub. models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6d605-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="6d605-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d605-142">OUTPUTS</span></span>

### <span data-ttu-id="6d605-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d605-143">System.Boolean</span></span>

## <span data-ttu-id="6d605-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d605-144">NOTES</span></span>

## <span data-ttu-id="6d605-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d605-145">RELATED LINKS</span></span>