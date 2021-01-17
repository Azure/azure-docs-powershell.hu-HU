---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387182"
---
# <span data-ttu-id="9a4c6-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="9a4c6-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="9a4c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4c6-103">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="9a4c6-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="9a4c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a4c6-104">SYNTAX</span></span>

### <span data-ttu-id="9a4c6-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a4c6-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4c6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a4c6-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4c6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a4c6-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4c6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a4c6-108">DESCRIPTION</span></span>
<span data-ttu-id="9a4c6-109">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="9a4c6-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="9a4c6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a4c6-110">EXAMPLES</span></span>

### <span data-ttu-id="9a4c6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9a4c6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="9a4c6-112">Töröljön egy devSpaceControllerName nevű DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="9a4c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a4c6-113">PARAMETERS</span></span>

### <span data-ttu-id="9a4c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a4c6-114">-AsJob</span></span>
<span data-ttu-id="9a4c6-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a4c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a4c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4c6-116">-DefaultProfile</span></span>
<span data-ttu-id="9a4c6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4c6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a4c6-118">-InputObject</span></span>
<span data-ttu-id="9a4c6-119">Egy PSController-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a4c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a4c6-120">-Name</span></span>
<span data-ttu-id="9a4c6-121">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="9a4c6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a4c6-122">-PassThru</span></span>
<span data-ttu-id="9a4c6-123">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="9a4c6-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="9a4c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a4c6-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9a4c6-125">Resource group name</span></span>

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

### <span data-ttu-id="9a4c6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a4c6-126">-ResourceId</span></span>
<span data-ttu-id="9a4c6-127">A DevSpaces erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="9a4c6-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="9a4c6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a4c6-128">-Confirm</span></span>
<span data-ttu-id="9a4c6-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4c6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4c6-130">-WhatIf</span></span>
<span data-ttu-id="9a4c6-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a4c6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4c6-133">CommonParameters</span></span>
<span data-ttu-id="9a4c6-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4c6-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4c6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4c6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a4c6-136">INPUTS</span></span>

### <span data-ttu-id="9a4c6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4c6-137">System.String</span></span>

### <span data-ttu-id="9a4c6-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="9a4c6-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="9a4c6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a4c6-139">OUTPUTS</span></span>

### <span data-ttu-id="9a4c6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a4c6-140">System.Boolean</span></span>

## <span data-ttu-id="9a4c6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a4c6-141">NOTES</span></span>

## <span data-ttu-id="9a4c6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a4c6-142">RELATED LINKS</span></span>
