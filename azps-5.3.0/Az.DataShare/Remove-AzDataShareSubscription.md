---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377102"
---
# <span data-ttu-id="bfe57-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="bfe57-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="bfe57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe57-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe57-103">eltávolít egy megosztási előfizetést</span><span class="sxs-lookup"><span data-stu-id="bfe57-103">removes a share subscription</span></span>

## <span data-ttu-id="bfe57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfe57-104">SYNTAX</span></span>

### <span data-ttu-id="bfe57-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfe57-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe57-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfe57-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe57-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfe57-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe57-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfe57-108">DESCRIPTION</span></span>
<span data-ttu-id="bfe57-109">A **Remove-AzDataShareSubscription** parancsmag eltávolítja a megosztási előfizetést</span><span class="sxs-lookup"><span data-stu-id="bfe57-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="bfe57-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfe57-110">EXAMPLES</span></span>

### <span data-ttu-id="bfe57-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bfe57-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bfe57-112">Ez a parancs eltávolítja az AdsShareSubscription nevű megosztási indexet a wikiad-fiókokból.</span><span class="sxs-lookup"><span data-stu-id="bfe57-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="bfe57-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfe57-113">PARAMETERS</span></span>

### <span data-ttu-id="bfe57-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bfe57-114">-AccountName</span></span>
<span data-ttu-id="bfe57-115">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="bfe57-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="bfe57-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfe57-116">-AsJob</span></span>
<span data-ttu-id="bfe57-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="bfe57-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="bfe57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe57-118">-DefaultProfile</span></span>
<span data-ttu-id="bfe57-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfe57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfe57-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfe57-120">-InputObject</span></span>
<span data-ttu-id="bfe57-121">Azure data share subscription object</span><span class="sxs-lookup"><span data-stu-id="bfe57-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe57-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bfe57-122">-Name</span></span>
<span data-ttu-id="bfe57-123">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="bfe57-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="bfe57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe57-124">-PassThru</span></span>
<span data-ttu-id="bfe57-125">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="bfe57-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="bfe57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe57-126">-ResourceGroupName</span></span>
<span data-ttu-id="bfe57-127">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="bfe57-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bfe57-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfe57-128">-ResourceId</span></span>
<span data-ttu-id="bfe57-129">Az Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bfe57-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="bfe57-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfe57-130">-Confirm</span></span>
<span data-ttu-id="bfe57-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bfe57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe57-132">-WhatIf</span></span>
<span data-ttu-id="bfe57-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bfe57-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe57-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfe57-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe57-135">CommonParameters</span></span>
<span data-ttu-id="bfe57-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe57-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfe57-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe57-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfe57-138">INPUTS</span></span>

### <span data-ttu-id="bfe57-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bfe57-139">System.String</span></span>

### <span data-ttu-id="bfe57-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="bfe57-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="bfe57-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfe57-141">OUTPUTS</span></span>

### <span data-ttu-id="bfe57-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfe57-142">System.Boolean</span></span>

## <span data-ttu-id="bfe57-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfe57-143">NOTES</span></span>

## <span data-ttu-id="bfe57-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfe57-144">RELATED LINKS</span></span>
