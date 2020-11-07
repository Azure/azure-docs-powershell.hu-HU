---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: ae781b4c53e373cdbd8338f4db75d6913c863bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669275"
---
# <span data-ttu-id="a851d-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="a851d-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="a851d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a851d-102">SYNOPSIS</span></span>
<span data-ttu-id="a851d-103">Távolítsa el a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a851d-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a851d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a851d-104">SYNTAX</span></span>

### <span data-ttu-id="a851d-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a851d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a851d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a851d-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a851d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a851d-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a851d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a851d-108">DESCRIPTION</span></span>
<span data-ttu-id="a851d-109">A **Remove-AzSearchQueryKey** parancsmag eltávolítja a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a851d-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a851d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a851d-110">EXAMPLES</span></span>

### <span data-ttu-id="a851d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a851d-111">Example 1</span></span>
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

<span data-ttu-id="a851d-112">A példa eltávolítja a Query billentyűt az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a851d-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a851d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a851d-113">PARAMETERS</span></span>

### <span data-ttu-id="a851d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a851d-114">-DefaultProfile</span></span>
<span data-ttu-id="a851d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a851d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a851d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a851d-116">-Force</span></span>
<span data-ttu-id="a851d-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a851d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a851d-118">-Érték</span><span class="sxs-lookup"><span data-stu-id="a851d-118">-KeyValue</span></span>
<span data-ttu-id="a851d-119">Keresési szolgáltatás lekérdezési kulcsának értéke</span><span class="sxs-lookup"><span data-stu-id="a851d-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="a851d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a851d-120">-ParentObject</span></span>
<span data-ttu-id="a851d-121">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="a851d-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a851d-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a851d-122">-ParentResourceId</span></span>
<span data-ttu-id="a851d-123">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a851d-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a851d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a851d-124">-PassThru</span></span>
<span data-ttu-id="a851d-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="a851d-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a851d-126">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="a851d-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a851d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a851d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a851d-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a851d-128">Resource Group name.</span></span>

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

### <span data-ttu-id="a851d-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a851d-129">-ServiceName</span></span>
<span data-ttu-id="a851d-130">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="a851d-130">Search Service name.</span></span>

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

### <span data-ttu-id="a851d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a851d-131">-Confirm</span></span>
<span data-ttu-id="a851d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a851d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a851d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a851d-133">-WhatIf</span></span>
<span data-ttu-id="a851d-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a851d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a851d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a851d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a851d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a851d-136">CommonParameters</span></span>
<span data-ttu-id="a851d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a851d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a851d-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a851d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a851d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a851d-139">INPUTS</span></span>

### <span data-ttu-id="a851d-140">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a851d-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a851d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a851d-141">System.String</span></span>

## <span data-ttu-id="a851d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a851d-142">OUTPUTS</span></span>

### <span data-ttu-id="a851d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a851d-143">System.Boolean</span></span>

## <span data-ttu-id="a851d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a851d-144">NOTES</span></span>

## <span data-ttu-id="a851d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a851d-145">RELATED LINKS</span></span>

[<span data-ttu-id="a851d-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a851d-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="a851d-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a851d-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
