---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679845"
---
# <span data-ttu-id="46370-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="46370-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="46370-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46370-102">SYNOPSIS</span></span>
<span data-ttu-id="46370-103">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="46370-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46370-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46370-104">SYNTAX</span></span>

### <span data-ttu-id="46370-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46370-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46370-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46370-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46370-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46370-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46370-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46370-108">DESCRIPTION</span></span>
<span data-ttu-id="46370-109">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="46370-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="46370-110">Példák</span><span class="sxs-lookup"><span data-stu-id="46370-110">EXAMPLES</span></span>

### <span data-ttu-id="46370-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46370-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="46370-112">Törölje a devSpaceControllerName nevű DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="46370-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="46370-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46370-113">PARAMETERS</span></span>

### <span data-ttu-id="46370-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46370-114">-AsJob</span></span>
<span data-ttu-id="46370-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46370-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46370-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46370-116">-DefaultProfile</span></span>
<span data-ttu-id="46370-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46370-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46370-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46370-118">-InputObject</span></span>
<span data-ttu-id="46370-119">Egy PSController objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="46370-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46370-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46370-120">-Name</span></span>
<span data-ttu-id="46370-121">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="46370-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46370-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46370-122">-PassThru</span></span>
<span data-ttu-id="46370-123">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="46370-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="46370-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46370-124">-ResourceGroupName</span></span>
<span data-ttu-id="46370-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="46370-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46370-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46370-126">-ResourceId</span></span>
<span data-ttu-id="46370-127">A DevSpaces erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="46370-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46370-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46370-128">-Confirm</span></span>
<span data-ttu-id="46370-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46370-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46370-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46370-130">-WhatIf</span></span>
<span data-ttu-id="46370-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46370-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46370-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46370-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46370-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46370-133">CommonParameters</span></span>
<span data-ttu-id="46370-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46370-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46370-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46370-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46370-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46370-136">INPUTS</span></span>

### <span data-ttu-id="46370-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46370-137">System.String</span></span>

### <span data-ttu-id="46370-138">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="46370-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="46370-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46370-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="46370-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46370-140">OUTPUTS</span></span>

### <span data-ttu-id="46370-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46370-141">System.Boolean</span></span>

## <span data-ttu-id="46370-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46370-142">NOTES</span></span>

## <span data-ttu-id="46370-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46370-143">RELATED LINKS</span></span>
