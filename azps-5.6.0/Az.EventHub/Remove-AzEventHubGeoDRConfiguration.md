---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2de5501c63ebbdd8842acb6cbfa40ec51893cbf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939561"
---
# <span data-ttu-id="2decc-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2decc-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="2decc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2decc-102">SYNOPSIS</span></span>
<span data-ttu-id="2decc-103">Alias törlése(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2decc-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2decc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2decc-104">SYNTAX</span></span>

### <span data-ttu-id="2decc-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2decc-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2decc-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2decc-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2decc-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2decc-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2decc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2decc-108">DESCRIPTION</span></span>
<span data-ttu-id="2decc-109">A **Remove-AzEventHubGeoDRConfiguration** parancsmag töröl egy aliast(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2decc-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2decc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2decc-110">EXAMPLES</span></span>

### <span data-ttu-id="2decc-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2decc-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="2decc-112">Egy alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="2decc-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2decc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2decc-113">PARAMETERS</span></span>

### <span data-ttu-id="2decc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2decc-114">-AsJob</span></span>
<span data-ttu-id="2decc-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2decc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2decc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2decc-116">-DefaultProfile</span></span>
<span data-ttu-id="2decc-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2decc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2decc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2decc-118">-InputObject</span></span>
<span data-ttu-id="2decc-119">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="2decc-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="2decc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2decc-120">-Name</span></span>
<span data-ttu-id="2decc-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="2decc-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="2decc-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2decc-122">-Namespace</span></span>
<span data-ttu-id="2decc-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2decc-123">Namespace Name</span></span>

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

### <span data-ttu-id="2decc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2decc-124">-PassThru</span></span>
<span data-ttu-id="2decc-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2decc-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2decc-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2decc-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2decc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2decc-127">-ResourceGroupName</span></span>
<span data-ttu-id="2decc-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2decc-128">Resource Group Name</span></span>

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

### <span data-ttu-id="2decc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2decc-129">-ResourceId</span></span>
<span data-ttu-id="2decc-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="2decc-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="2decc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2decc-131">-Confirm</span></span>
<span data-ttu-id="2decc-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2decc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2decc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2decc-133">-WhatIf</span></span>
<span data-ttu-id="2decc-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2decc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2decc-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2decc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2decc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2decc-136">CommonParameters</span></span>
<span data-ttu-id="2decc-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2decc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2decc-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2decc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2decc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2decc-139">INPUTS</span></span>

### <span data-ttu-id="2decc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2decc-140">System.String</span></span>

### <span data-ttu-id="2decc-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2decc-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="2decc-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2decc-142">OUTPUTS</span></span>

### <span data-ttu-id="2decc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2decc-143">System.Boolean</span></span>

## <span data-ttu-id="2decc-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2decc-144">NOTES</span></span>

## <span data-ttu-id="2decc-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2decc-145">RELATED LINKS</span></span>
