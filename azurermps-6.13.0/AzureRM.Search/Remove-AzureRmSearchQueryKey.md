---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
ms.openlocfilehash: 1dbdf342335ca204287ccfd2efea737f2eb747fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500124"
---
# <span data-ttu-id="fa502-101">Remove-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fa502-101">Remove-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="fa502-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa502-102">SYNOPSIS</span></span>
<span data-ttu-id="fa502-103">Távolítsa el a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="fa502-103">Remove the query key from the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa502-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa502-104">SYNTAX</span></span>

### <span data-ttu-id="fa502-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa502-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa502-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa502-106">ParentObjectParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa502-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa502-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa502-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa502-108">DESCRIPTION</span></span>
<span data-ttu-id="fa502-109">A **Remove-AzureRmSearchQueryKey** parancsmag eltávolítja a lekérdezési kulcsot az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="fa502-109">The **Remove-AzureRmSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="fa502-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa502-110">EXAMPLES</span></span>

### <span data-ttu-id="fa502-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa502-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="fa502-112">A példa eltávolítja a Query billentyűt az Azure Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="fa502-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="fa502-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa502-113">PARAMETERS</span></span>

### <span data-ttu-id="fa502-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa502-114">-DefaultProfile</span></span>
<span data-ttu-id="fa502-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa502-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa502-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fa502-116">-Force</span></span>
<span data-ttu-id="fa502-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa502-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fa502-118">-Érték</span><span class="sxs-lookup"><span data-stu-id="fa502-118">-KeyValue</span></span>
<span data-ttu-id="fa502-119">Keresési szolgáltatás lekérdezési kulcsának értéke</span><span class="sxs-lookup"><span data-stu-id="fa502-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="fa502-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa502-120">-ParentObject</span></span>
<span data-ttu-id="fa502-121">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="fa502-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="fa502-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fa502-122">-ParentResourceId</span></span>
<span data-ttu-id="fa502-123">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fa502-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="fa502-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa502-124">-PassThru</span></span>
<span data-ttu-id="fa502-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="fa502-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fa502-126">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="fa502-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fa502-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa502-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa502-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fa502-128">Resource Group name.</span></span>

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

### <span data-ttu-id="fa502-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fa502-129">-ServiceName</span></span>
<span data-ttu-id="fa502-130">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="fa502-130">Search Service name.</span></span>

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

### <span data-ttu-id="fa502-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa502-131">-Confirm</span></span>
<span data-ttu-id="fa502-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa502-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa502-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa502-133">-WhatIf</span></span>
<span data-ttu-id="fa502-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa502-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa502-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa502-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa502-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa502-136">CommonParameters</span></span>
<span data-ttu-id="fa502-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa502-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa502-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa502-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa502-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa502-139">INPUTS</span></span>

### <span data-ttu-id="fa502-140">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fa502-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="fa502-141">Paraméterek: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa502-141">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="fa502-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fa502-142">System.String</span></span>

## <span data-ttu-id="fa502-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa502-143">OUTPUTS</span></span>

### <span data-ttu-id="fa502-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa502-144">System.Boolean</span></span>

## <span data-ttu-id="fa502-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa502-145">NOTES</span></span>

## <span data-ttu-id="fa502-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa502-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa502-147">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fa502-147">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="fa502-148">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fa502-148">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)
