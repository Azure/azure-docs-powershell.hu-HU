---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930017"
---
# <span data-ttu-id="79238-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="79238-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="79238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79238-102">SYNOPSIS</span></span>
<span data-ttu-id="79238-103">Adatgyűjtési szabály törlése</span><span class="sxs-lookup"><span data-stu-id="79238-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="79238-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79238-104">SYNTAX</span></span>

### <span data-ttu-id="79238-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79238-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="79238-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79238-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="79238-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79238-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="79238-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79238-108">DESCRIPTION</span></span>
<span data-ttu-id="79238-109">A **Remove-AzDataCollectionRule** parancsmag töröl egy adatgyűjtési szabályt.</span><span class="sxs-lookup"><span data-stu-id="79238-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="79238-110">Az adatgyűjtési szabályok (DCR) definiálják az Azure Monitorra érkező adatokat, és meghatározzák, hogy hová kell küldeni vagy tárolni az adatokat.</span><span class="sxs-lookup"><span data-stu-id="79238-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="79238-111">Az alábbi teljes [áttekintést nyújtjuk a DCR-ről.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="79238-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="79238-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79238-112">EXAMPLES</span></span>

### <span data-ttu-id="79238-113">1. példa: A név- és erőforráscsoport-paramétereket is tartalmazó adatgyűjtési szabály törlése</span><span class="sxs-lookup"><span data-stu-id="79238-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="79238-114">2. példa: Az adatgyűjtési szabály törlése névvel és erőforráscsoporttal</span><span class="sxs-lookup"><span data-stu-id="79238-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="79238-115">3. példa: Adatgyűjtési szabály törlése az InputObjectből</span><span class="sxs-lookup"><span data-stu-id="79238-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="79238-116">4. példa: Adatgyűjtési szabály törlése az erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="79238-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="79238-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79238-117">PARAMETERS</span></span>

### <span data-ttu-id="79238-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79238-118">-DefaultProfile</span></span>
<span data-ttu-id="79238-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79238-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79238-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79238-120">-ResourceGroupName</span></span>
<span data-ttu-id="79238-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="79238-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79238-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="79238-122">-RuleName</span></span>
<span data-ttu-id="79238-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="79238-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79238-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="79238-124">-RuleId</span></span>
<span data-ttu-id="79238-125">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="79238-125">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79238-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79238-126">-Confirm</span></span>
<span data-ttu-id="79238-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79238-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79238-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79238-128">-WhatIf</span></span>
<span data-ttu-id="79238-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79238-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79238-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79238-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79238-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79238-131">CommonParameters</span></span>
<span data-ttu-id="79238-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79238-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79238-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79238-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79238-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79238-134">INPUTS</span></span>

### <span data-ttu-id="79238-135">System.String</span><span class="sxs-lookup"><span data-stu-id="79238-135">System.String</span></span>

## <span data-ttu-id="79238-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79238-136">OUTPUTS</span></span>

### <span data-ttu-id="79238-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="79238-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="79238-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79238-138">NOTES</span></span>

## <span data-ttu-id="79238-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79238-139">RELATED LINKS</span></span>

<span data-ttu-id="79238-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="79238-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>