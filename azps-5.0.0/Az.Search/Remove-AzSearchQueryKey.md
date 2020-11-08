---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188188"
---
# <span data-ttu-id="a0291-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="a0291-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="a0291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0291-102">SYNOPSIS</span></span>
<span data-ttu-id="a0291-103">Távolítsa el a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a0291-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0291-104">SYNTAX</span></span>

### <span data-ttu-id="a0291-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0291-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0291-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0291-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0291-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0291-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0291-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0291-108">DESCRIPTION</span></span>
<span data-ttu-id="a0291-109">A **Remove-AzSearchQueryKey** parancsmag eltávolítja a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a0291-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0291-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a0291-110">EXAMPLES</span></span>

### <span data-ttu-id="a0291-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0291-111">Example 1</span></span>
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

<span data-ttu-id="a0291-112">A példa eltávolítja a Query billentyűt az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a0291-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0291-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0291-113">PARAMETERS</span></span>

### <span data-ttu-id="a0291-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0291-114">-DefaultProfile</span></span>
<span data-ttu-id="a0291-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0291-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0291-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a0291-116">-Force</span></span>
<span data-ttu-id="a0291-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0291-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0291-118">-Érték</span><span class="sxs-lookup"><span data-stu-id="a0291-118">-KeyValue</span></span>
<span data-ttu-id="a0291-119">Keresési szolgáltatás lekérdezési kulcsának értéke</span><span class="sxs-lookup"><span data-stu-id="a0291-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="a0291-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a0291-120">-ParentObject</span></span>
<span data-ttu-id="a0291-121">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="a0291-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a0291-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a0291-122">-ParentResourceId</span></span>
<span data-ttu-id="a0291-123">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a0291-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a0291-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0291-124">-PassThru</span></span>
<span data-ttu-id="a0291-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="a0291-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a0291-126">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="a0291-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a0291-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0291-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0291-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a0291-128">Resource Group name.</span></span>

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

### <span data-ttu-id="a0291-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a0291-129">-ServiceName</span></span>
<span data-ttu-id="a0291-130">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="a0291-130">Search Service name.</span></span>

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

### <span data-ttu-id="a0291-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0291-131">-Confirm</span></span>
<span data-ttu-id="a0291-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0291-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0291-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0291-133">-WhatIf</span></span>
<span data-ttu-id="a0291-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0291-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0291-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0291-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0291-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0291-136">CommonParameters</span></span>
<span data-ttu-id="a0291-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0291-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0291-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0291-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0291-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0291-139">INPUTS</span></span>

### <span data-ttu-id="a0291-140">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a0291-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a0291-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a0291-141">System.String</span></span>

## <span data-ttu-id="a0291-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0291-142">OUTPUTS</span></span>

### <span data-ttu-id="a0291-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0291-143">System.Boolean</span></span>

## <span data-ttu-id="a0291-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0291-144">NOTES</span></span>

## <span data-ttu-id="a0291-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0291-145">RELATED LINKS</span></span>

[<span data-ttu-id="a0291-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a0291-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="a0291-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a0291-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)