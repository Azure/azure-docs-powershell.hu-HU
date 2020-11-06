---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500119"
---
# <span data-ttu-id="3b5f6-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="3b5f6-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="3b5f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5f6-103">Azure Search szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3b5f6-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b5f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b5f6-104">SYNTAX</span></span>

### <span data-ttu-id="3b5f6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b5f6-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5f6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b5f6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5f6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b5f6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b5f6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b5f6-108">DESCRIPTION</span></span>
<span data-ttu-id="3b5f6-109">A **Remove-AzureRmSearchService** parancsmag eltávolítja az Azure Search szolgáltatást a megadott paramters.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="3b5f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3b5f6-110">EXAMPLES</span></span>

### <span data-ttu-id="3b5f6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b5f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="3b5f6-112">A példa eltávolítja az Azure Search szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="3b5f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b5f6-113">PARAMETERS</span></span>

### <span data-ttu-id="3b5f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5f6-114">-DefaultProfile</span></span>
<span data-ttu-id="3b5f6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b5f6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3b5f6-116">-Force</span></span>
<span data-ttu-id="3b5f6-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3b5f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b5f6-118">-InputObject</span></span>
<span data-ttu-id="3b5f6-119">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3b5f6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b5f6-120">-Name</span></span>
<span data-ttu-id="3b5f6-121">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="3b5f6-121">Search Service name.</span></span>

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

### <span data-ttu-id="3b5f6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b5f6-122">-PassThru</span></span>
<span data-ttu-id="3b5f6-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3b5f6-124">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3b5f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b5f6-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-126">Resource Group name.</span></span>

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

### <span data-ttu-id="3b5f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b5f6-127">-ResourceId</span></span>
<span data-ttu-id="3b5f6-128">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3b5f6-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3b5f6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b5f6-129">-Confirm</span></span>
<span data-ttu-id="3b5f6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5f6-131">-WhatIf</span></span>
<span data-ttu-id="3b5f6-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b5f6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b5f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5f6-134">CommonParameters</span></span>
<span data-ttu-id="3b5f6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b5f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5f6-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5f6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5f6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b5f6-137">INPUTS</span></span>

### <span data-ttu-id="3b5f6-138">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3b5f6-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="3b5f6-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b5f6-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3b5f6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5f6-140">System.String</span></span>

## <span data-ttu-id="3b5f6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b5f6-141">OUTPUTS</span></span>

### <span data-ttu-id="3b5f6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b5f6-142">System.Boolean</span></span>

## <span data-ttu-id="3b5f6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b5f6-143">NOTES</span></span>

## <span data-ttu-id="3b5f6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b5f6-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b5f6-145">Új – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="3b5f6-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="3b5f6-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="3b5f6-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="3b5f6-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="3b5f6-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

