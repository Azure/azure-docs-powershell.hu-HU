---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185563"
---
# <span data-ttu-id="a1348-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a1348-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="a1348-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1348-102">SYNOPSIS</span></span>
<span data-ttu-id="a1348-103">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="a1348-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a1348-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1348-104">SYNTAX</span></span>

### <span data-ttu-id="a1348-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1348-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1348-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1348-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1348-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1348-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1348-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1348-108">DESCRIPTION</span></span>
<span data-ttu-id="a1348-109">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="a1348-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a1348-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a1348-110">EXAMPLES</span></span>

### <span data-ttu-id="a1348-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1348-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="a1348-112">Törölje a devSpaceControllerName nevű DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="a1348-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="a1348-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1348-113">PARAMETERS</span></span>

### <span data-ttu-id="a1348-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1348-114">-AsJob</span></span>
<span data-ttu-id="a1348-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1348-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1348-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1348-116">-DefaultProfile</span></span>
<span data-ttu-id="a1348-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1348-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1348-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1348-118">-InputObject</span></span>
<span data-ttu-id="a1348-119">Egy PSController objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a1348-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1348-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1348-120">-Name</span></span>
<span data-ttu-id="a1348-121">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="a1348-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a1348-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1348-122">-PassThru</span></span>
<span data-ttu-id="a1348-123">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="a1348-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="a1348-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1348-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1348-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a1348-125">Resource group name</span></span>

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

### <span data-ttu-id="a1348-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1348-126">-ResourceId</span></span>
<span data-ttu-id="a1348-127">A DevSpaces erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a1348-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="a1348-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1348-128">-Confirm</span></span>
<span data-ttu-id="a1348-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1348-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1348-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1348-130">-WhatIf</span></span>
<span data-ttu-id="a1348-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1348-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1348-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1348-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1348-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1348-133">CommonParameters</span></span>
<span data-ttu-id="a1348-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1348-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1348-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1348-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1348-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1348-136">INPUTS</span></span>

### <span data-ttu-id="a1348-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a1348-137">System.String</span></span>

### <span data-ttu-id="a1348-138">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="a1348-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a1348-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1348-139">OUTPUTS</span></span>

### <span data-ttu-id="a1348-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1348-140">System.Boolean</span></span>

## <span data-ttu-id="a1348-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1348-141">NOTES</span></span>

## <span data-ttu-id="a1348-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1348-142">RELATED LINKS</span></span>
