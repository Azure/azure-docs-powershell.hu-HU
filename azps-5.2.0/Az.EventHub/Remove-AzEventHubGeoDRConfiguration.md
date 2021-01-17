---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353118"
---
# <span data-ttu-id="8c803-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c803-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="8c803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c803-102">SYNOPSIS</span></span>
<span data-ttu-id="8c803-103">Alias törlése(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="8c803-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8c803-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c803-104">SYNTAX</span></span>

### <span data-ttu-id="8c803-105">GeoDRParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c803-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c803-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c803-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c803-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c803-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c803-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c803-108">DESCRIPTION</span></span>
<span data-ttu-id="8c803-109">A **Remove-AzEventHubGeoDRConfiguration** parancsmag töröl egy aliast(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="8c803-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8c803-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c803-110">EXAMPLES</span></span>

### <span data-ttu-id="8c803-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c803-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="8c803-112">Egy alias törlése (katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="8c803-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8c803-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c803-113">PARAMETERS</span></span>

### <span data-ttu-id="8c803-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c803-114">-AsJob</span></span>
<span data-ttu-id="8c803-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8c803-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c803-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c803-116">-DefaultProfile</span></span>
<span data-ttu-id="8c803-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c803-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c803-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c803-118">-InputObject</span></span>
<span data-ttu-id="8c803-119">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="8c803-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="8c803-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8c803-120">-Name</span></span>
<span data-ttu-id="8c803-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="8c803-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="8c803-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c803-122">-Namespace</span></span>
<span data-ttu-id="8c803-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="8c803-123">Namespace Name</span></span>

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

### <span data-ttu-id="8c803-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c803-124">-PassThru</span></span>
<span data-ttu-id="8c803-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8c803-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c803-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8c803-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c803-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c803-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c803-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8c803-128">Resource Group Name</span></span>

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

### <span data-ttu-id="8c803-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c803-129">-ResourceId</span></span>
<span data-ttu-id="8c803-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="8c803-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="8c803-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c803-131">-Confirm</span></span>
<span data-ttu-id="8c803-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c803-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c803-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c803-133">-WhatIf</span></span>
<span data-ttu-id="8c803-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c803-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c803-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c803-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c803-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c803-136">CommonParameters</span></span>
<span data-ttu-id="8c803-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c803-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c803-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c803-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c803-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c803-139">INPUTS</span></span>

### <span data-ttu-id="8c803-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c803-140">System.String</span></span>

### <span data-ttu-id="8c803-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8c803-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="8c803-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c803-142">OUTPUTS</span></span>

### <span data-ttu-id="8c803-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c803-143">System.Boolean</span></span>

## <span data-ttu-id="8c803-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c803-144">NOTES</span></span>

## <span data-ttu-id="8c803-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c803-145">RELATED LINKS</span></span>
