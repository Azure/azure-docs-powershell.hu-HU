---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 3d4610f83b348864fc57cf6894db1ab7455a8485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205942"
---
# <span data-ttu-id="4c838-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="4c838-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="4c838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c838-102">SYNOPSIS</span></span>
<span data-ttu-id="4c838-103">Távolítsa el a lekérdezéskulcsot az Azure Kognitív keresés szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="4c838-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4c838-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c838-104">SYNTAX</span></span>

### <span data-ttu-id="4c838-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c838-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c838-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c838-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c838-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c838-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c838-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c838-108">DESCRIPTION</span></span>
<span data-ttu-id="4c838-109">A **Remove-AzSearchQueryKey** parancsmag eltávolítja a lekérdezéskulcsot az Azure Kognitív keresés szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="4c838-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4c838-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c838-110">EXAMPLES</span></span>

### <span data-ttu-id="4c838-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4c838-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="4c838-112">A példa eltávolítja a lekérdezéskulcsot az Azure Kognitív keresés szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="4c838-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4c838-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c838-113">PARAMETERS</span></span>

### <span data-ttu-id="4c838-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c838-114">-DefaultProfile</span></span>
<span data-ttu-id="4c838-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c838-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c838-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4c838-116">-Force</span></span>
<span data-ttu-id="4c838-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c838-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4c838-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="4c838-118">-KeyValue</span></span>
<span data-ttu-id="4c838-119">Az Azure Kognitív keresési szolgáltatás lekérdezéskulcsának értéke.</span><span class="sxs-lookup"><span data-stu-id="4c838-119">Azure Cognitive Search Service query key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c838-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c838-120">-ParentObject</span></span>
<span data-ttu-id="4c838-121">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="4c838-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c838-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c838-122">-ParentResourceId</span></span>
<span data-ttu-id="4c838-123">Azure Kognitív keresési szolgáltatás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c838-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c838-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c838-124">-PassThru</span></span>
<span data-ttu-id="4c838-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4c838-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4c838-126">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="4c838-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4c838-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c838-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c838-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4c838-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c838-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4c838-129">-ServiceName</span></span>
<span data-ttu-id="4c838-130">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="4c838-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c838-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c838-131">-Confirm</span></span>
<span data-ttu-id="4c838-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4c838-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c838-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c838-133">-WhatIf</span></span>
<span data-ttu-id="4c838-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4c838-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c838-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c838-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c838-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c838-136">CommonParameters</span></span>
<span data-ttu-id="4c838-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c838-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c838-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c838-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c838-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c838-139">INPUTS</span></span>

### <span data-ttu-id="4c838-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4c838-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4c838-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4c838-141">System.String</span></span>

## <span data-ttu-id="4c838-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c838-142">OUTPUTS</span></span>

### <span data-ttu-id="4c838-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c838-143">System.Boolean</span></span>

## <span data-ttu-id="4c838-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c838-144">NOTES</span></span>

## <span data-ttu-id="4c838-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c838-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c838-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4c838-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="4c838-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4c838-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
