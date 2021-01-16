---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466381"
---
# <span data-ttu-id="7325f-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7325f-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="7325f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7325f-102">SYNOPSIS</span></span>
<span data-ttu-id="7325f-103">Távolítson el egy Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7325f-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="7325f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7325f-104">SYNTAX</span></span>

### <span data-ttu-id="7325f-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7325f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7325f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7325f-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7325f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7325f-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7325f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7325f-108">DESCRIPTION</span></span>
<span data-ttu-id="7325f-109">A **Remove-AzSearchService** parancsmag eltávolítja a megadott paraméterekkel megadott Azure Search-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7325f-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="7325f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7325f-110">EXAMPLES</span></span>

### <span data-ttu-id="7325f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7325f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="7325f-112">A példa eltávolítja az Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7325f-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="7325f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7325f-113">PARAMETERS</span></span>

### <span data-ttu-id="7325f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7325f-114">-DefaultProfile</span></span>
<span data-ttu-id="7325f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7325f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7325f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7325f-116">-Force</span></span>
<span data-ttu-id="7325f-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7325f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7325f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7325f-118">-InputObject</span></span>
<span data-ttu-id="7325f-119">Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="7325f-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="7325f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7325f-120">-Name</span></span>
<span data-ttu-id="7325f-121">Keresés a szolgáltatásnévben</span><span class="sxs-lookup"><span data-stu-id="7325f-121">Search Service name.</span></span>

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

### <span data-ttu-id="7325f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7325f-122">-PassThru</span></span>
<span data-ttu-id="7325f-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="7325f-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7325f-124">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="7325f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7325f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7325f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7325f-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7325f-126">Resource Group name.</span></span>

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

### <span data-ttu-id="7325f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7325f-127">-ResourceId</span></span>
<span data-ttu-id="7325f-128">Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="7325f-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7325f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7325f-129">-Confirm</span></span>
<span data-ttu-id="7325f-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7325f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7325f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7325f-131">-WhatIf</span></span>
<span data-ttu-id="7325f-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7325f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7325f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7325f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7325f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7325f-134">CommonParameters</span></span>
<span data-ttu-id="7325f-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7325f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7325f-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7325f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7325f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7325f-137">INPUTS</span></span>

### <span data-ttu-id="7325f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7325f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7325f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7325f-139">System.String</span></span>

## <span data-ttu-id="7325f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7325f-140">OUTPUTS</span></span>

### <span data-ttu-id="7325f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7325f-141">System.Boolean</span></span>

## <span data-ttu-id="7325f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7325f-142">NOTES</span></span>

## <span data-ttu-id="7325f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7325f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7325f-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7325f-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="7325f-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7325f-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7325f-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7325f-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

