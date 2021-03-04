---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925881"
---
# <span data-ttu-id="bebe7-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bebe7-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="bebe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bebe7-102">SYNOPSIS</span></span>
<span data-ttu-id="bebe7-103">eltávolít egy eseményindítót</span><span class="sxs-lookup"><span data-stu-id="bebe7-103">removes a trigger</span></span>

## <span data-ttu-id="bebe7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bebe7-104">SYNTAX</span></span>

### <span data-ttu-id="bebe7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bebe7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bebe7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bebe7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bebe7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bebe7-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bebe7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bebe7-108">DESCRIPTION</span></span>
<span data-ttu-id="bebe7-109">A **Remove-AzDataShareTrigger** parancsmag eltávolít egy adatmegosztási eseményindítót</span><span class="sxs-lookup"><span data-stu-id="bebe7-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="bebe7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bebe7-110">EXAMPLES</span></span>

### <span data-ttu-id="bebe7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bebe7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bebe7-112">Ez a parancs eltávolítja az AdsTrigger nevű eseményindítót a share subscription AdsShareSubscription szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="bebe7-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="bebe7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bebe7-113">PARAMETERS</span></span>

### <span data-ttu-id="bebe7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bebe7-114">-AccountName</span></span>
<span data-ttu-id="bebe7-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="bebe7-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bebe7-116">-AsJob</span></span>
<span data-ttu-id="bebe7-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="bebe7-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="bebe7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebe7-118">-DefaultProfile</span></span>
<span data-ttu-id="bebe7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bebe7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bebe7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bebe7-120">-InputObject</span></span>
<span data-ttu-id="bebe7-121">Azure data share trigger object</span><span class="sxs-lookup"><span data-stu-id="bebe7-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bebe7-122">-Name</span></span>
<span data-ttu-id="bebe7-123">Azure data share trigger name</span><span class="sxs-lookup"><span data-stu-id="bebe7-123">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bebe7-124">-PassThru</span></span>
<span data-ttu-id="bebe7-125">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="bebe7-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="bebe7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bebe7-126">-ResourceGroupName</span></span>
<span data-ttu-id="bebe7-127">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="bebe7-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bebe7-128">-ResourceId</span></span>
<span data-ttu-id="bebe7-129">Az Azure-adatok megosztására vonatkozó eseményindító erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bebe7-129">The resource id of azure data share trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bebe7-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="bebe7-131">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="bebe7-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bebe7-132">-Confirm</span></span>
<span data-ttu-id="bebe7-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bebe7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bebe7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bebe7-134">-WhatIf</span></span>
<span data-ttu-id="bebe7-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bebe7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bebe7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bebe7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bebe7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebe7-137">CommonParameters</span></span>
<span data-ttu-id="bebe7-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bebe7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebe7-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bebe7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebe7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bebe7-140">INPUTS</span></span>

### <span data-ttu-id="bebe7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bebe7-141">System.String</span></span>

### <span data-ttu-id="bebe7-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bebe7-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="bebe7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bebe7-143">OUTPUTS</span></span>

### <span data-ttu-id="bebe7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bebe7-144">System.Boolean</span></span>

## <span data-ttu-id="bebe7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bebe7-145">NOTES</span></span>

## <span data-ttu-id="bebe7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bebe7-146">RELATED LINKS</span></span>
