---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377088"
---
# <span data-ttu-id="b89ed-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b89ed-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="b89ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b89ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b89ed-103">eltávolít egy eseményindítót</span><span class="sxs-lookup"><span data-stu-id="b89ed-103">removes a trigger</span></span>

## <span data-ttu-id="b89ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b89ed-104">SYNTAX</span></span>

### <span data-ttu-id="b89ed-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b89ed-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b89ed-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89ed-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89ed-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89ed-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b89ed-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b89ed-108">DESCRIPTION</span></span>
<span data-ttu-id="b89ed-109">Az **Remove-AzDataShareTrigger** parancsmag eltávolít egy adatmegosztási eseményindítót</span><span class="sxs-lookup"><span data-stu-id="b89ed-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="b89ed-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b89ed-110">EXAMPLES</span></span>

### <span data-ttu-id="b89ed-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b89ed-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b89ed-112">Ez a parancs eltávolítja az AdsTrigger nevű eseményindítót a share subscription AdsShareSubscription szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="b89ed-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="b89ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b89ed-113">PARAMETERS</span></span>

### <span data-ttu-id="b89ed-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b89ed-114">-AccountName</span></span>
<span data-ttu-id="b89ed-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="b89ed-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b89ed-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b89ed-116">-AsJob</span></span>
<span data-ttu-id="b89ed-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="b89ed-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b89ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89ed-118">-DefaultProfile</span></span>
<span data-ttu-id="b89ed-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b89ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b89ed-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b89ed-120">-InputObject</span></span>
<span data-ttu-id="b89ed-121">Azure data share trigger object</span><span class="sxs-lookup"><span data-stu-id="b89ed-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="b89ed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b89ed-122">-Name</span></span>
<span data-ttu-id="b89ed-123">Azure data share trigger name</span><span class="sxs-lookup"><span data-stu-id="b89ed-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b89ed-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b89ed-124">-PassThru</span></span>
<span data-ttu-id="b89ed-125">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="b89ed-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="b89ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="b89ed-127">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="b89ed-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b89ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b89ed-128">-ResourceId</span></span>
<span data-ttu-id="b89ed-129">Az Azure-adatok megosztására vonatkozó eseményindító erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b89ed-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="b89ed-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b89ed-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="b89ed-131">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="b89ed-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b89ed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b89ed-132">-Confirm</span></span>
<span data-ttu-id="b89ed-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b89ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89ed-134">-WhatIf</span></span>
<span data-ttu-id="b89ed-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b89ed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b89ed-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b89ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89ed-137">CommonParameters</span></span>
<span data-ttu-id="b89ed-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89ed-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b89ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89ed-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b89ed-140">INPUTS</span></span>

### <span data-ttu-id="b89ed-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b89ed-141">System.String</span></span>

### <span data-ttu-id="b89ed-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b89ed-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="b89ed-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b89ed-143">OUTPUTS</span></span>

### <span data-ttu-id="b89ed-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b89ed-144">System.Boolean</span></span>

## <span data-ttu-id="b89ed-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b89ed-145">NOTES</span></span>

## <span data-ttu-id="b89ed-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b89ed-146">RELATED LINKS</span></span>
