---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999718"
---
# <span data-ttu-id="d4d7e-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4d7e-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d4d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d7e-103">Alias törlése(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="d4d7e-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d4d7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4d7e-104">SYNTAX</span></span>

### <span data-ttu-id="d4d7e-105">GeoDRPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4d7e-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d7e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4d7e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d7e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d7e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d7e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4d7e-108">DESCRIPTION</span></span>
<span data-ttu-id="d4d7e-109">A **Remove-AzServiceBusGeoDRConfiguration** parancsmag töröl egy aliast(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="d4d7e-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d4d7e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="d4d7e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4d7e-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="d4d7e-112">Alias törlése(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="d4d7e-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d4d7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d7e-113">PARAMETERS</span></span>

### <span data-ttu-id="d4d7e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4d7e-114">-AsJob</span></span>
<span data-ttu-id="d4d7e-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4d7e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4d7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d7e-116">-DefaultProfile</span></span>
<span data-ttu-id="d4d7e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d7e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4d7e-118">-InputObject</span></span>
<span data-ttu-id="d4d7e-119">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="d4d7e-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="d4d7e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d4d7e-120">-Name</span></span>
<span data-ttu-id="d4d7e-121">Alias (GeoDR) Neve</span><span class="sxs-lookup"><span data-stu-id="d4d7e-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="d4d7e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4d7e-122">-Namespace</span></span>
<span data-ttu-id="d4d7e-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d4d7e-123">Namespace Name</span></span>

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

### <span data-ttu-id="d4d7e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4d7e-124">-PassThru</span></span>
<span data-ttu-id="d4d7e-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4d7e-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d4d7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4d7e-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d4d7e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d4d7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d7e-129">-ResourceId</span></span>
<span data-ttu-id="d4d7e-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="d4d7e-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="d4d7e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4d7e-131">-Confirm</span></span>
<span data-ttu-id="d4d7e-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d7e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d7e-133">-WhatIf</span></span>
<span data-ttu-id="d4d7e-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d7e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d7e-136">CommonParameters</span></span>
<span data-ttu-id="d4d7e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d7e-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d7e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d7e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4d7e-139">INPUTS</span></span>

### <span data-ttu-id="d4d7e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d4d7e-140">System.String</span></span>

### <span data-ttu-id="d4d7e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d4d7e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d4d7e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4d7e-142">OUTPUTS</span></span>

### <span data-ttu-id="d4d7e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4d7e-143">System.Boolean</span></span>

## <span data-ttu-id="d4d7e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4d7e-144">NOTES</span></span>

## <span data-ttu-id="d4d7e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4d7e-145">RELATED LINKS</span></span>
