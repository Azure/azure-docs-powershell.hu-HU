---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188187"
---
# <span data-ttu-id="cf01a-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cf01a-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="cf01a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf01a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf01a-103">Azure Search szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cf01a-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="cf01a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf01a-104">SYNTAX</span></span>

### <span data-ttu-id="cf01a-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf01a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf01a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf01a-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf01a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf01a-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf01a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf01a-108">DESCRIPTION</span></span>
<span data-ttu-id="cf01a-109">A **Remove-AzSearchService** parancsmag a megadott paraméterekkel eltávolít egy Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cf01a-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="cf01a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cf01a-110">EXAMPLES</span></span>

### <span data-ttu-id="cf01a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf01a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="cf01a-112">A példa eltávolítja az Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cf01a-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="cf01a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf01a-113">PARAMETERS</span></span>

### <span data-ttu-id="cf01a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf01a-114">-DefaultProfile</span></span>
<span data-ttu-id="cf01a-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf01a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf01a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cf01a-116">-Force</span></span>
<span data-ttu-id="cf01a-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf01a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf01a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf01a-118">-InputObject</span></span>
<span data-ttu-id="cf01a-119">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="cf01a-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf01a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf01a-120">-Name</span></span>
<span data-ttu-id="cf01a-121">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="cf01a-121">Search Service name.</span></span>

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

### <span data-ttu-id="cf01a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf01a-122">-PassThru</span></span>
<span data-ttu-id="cf01a-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="cf01a-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="cf01a-124">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="cf01a-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cf01a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf01a-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf01a-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cf01a-126">Resource Group name.</span></span>

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

### <span data-ttu-id="cf01a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf01a-127">-ResourceId</span></span>
<span data-ttu-id="cf01a-128">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cf01a-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf01a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf01a-129">-Confirm</span></span>
<span data-ttu-id="cf01a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf01a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf01a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf01a-131">-WhatIf</span></span>
<span data-ttu-id="cf01a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf01a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf01a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf01a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf01a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf01a-134">CommonParameters</span></span>
<span data-ttu-id="cf01a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf01a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf01a-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf01a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf01a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf01a-137">INPUTS</span></span>

### <span data-ttu-id="cf01a-138">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="cf01a-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="cf01a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cf01a-139">System.String</span></span>

## <span data-ttu-id="cf01a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf01a-140">OUTPUTS</span></span>

### <span data-ttu-id="cf01a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf01a-141">System.Boolean</span></span>

## <span data-ttu-id="cf01a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf01a-142">NOTES</span></span>

## <span data-ttu-id="cf01a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf01a-143">RELATED LINKS</span></span>

[<span data-ttu-id="cf01a-144">Új – AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cf01a-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="cf01a-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cf01a-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="cf01a-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="cf01a-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

