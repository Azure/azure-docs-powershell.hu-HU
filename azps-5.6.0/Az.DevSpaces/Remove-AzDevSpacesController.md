---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927225"
---
# <span data-ttu-id="6fbf9-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6fbf9-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="6fbf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbf9-103">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="6fbf9-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6fbf9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fbf9-104">SYNTAX</span></span>

### <span data-ttu-id="6fbf9-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fbf9-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbf9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf9-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbf9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf9-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbf9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fbf9-108">DESCRIPTION</span></span>
<span data-ttu-id="6fbf9-109">DevSpaces-vezérlő törlése</span><span class="sxs-lookup"><span data-stu-id="6fbf9-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6fbf9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fbf9-110">EXAMPLES</span></span>

### <span data-ttu-id="6fbf9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6fbf9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="6fbf9-112">Töröljön egy devSpaceControllerName nevű DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="6fbf9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fbf9-113">PARAMETERS</span></span>

### <span data-ttu-id="6fbf9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fbf9-114">-AsJob</span></span>
<span data-ttu-id="6fbf9-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6fbf9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fbf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbf9-116">-DefaultProfile</span></span>
<span data-ttu-id="6fbf9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbf9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbf9-118">-InputObject</span></span>
<span data-ttu-id="6fbf9-119">Egy PSController-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6fbf9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6fbf9-120">-Name</span></span>
<span data-ttu-id="6fbf9-121">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6fbf9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fbf9-122">-PassThru</span></span>
<span data-ttu-id="6fbf9-123">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="6fbf9-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="6fbf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fbf9-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6fbf9-125">Resource group name</span></span>

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

### <span data-ttu-id="6fbf9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fbf9-126">-ResourceId</span></span>
<span data-ttu-id="6fbf9-127">A DevSpaces erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="6fbf9-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="6fbf9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fbf9-128">-Confirm</span></span>
<span data-ttu-id="6fbf9-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbf9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbf9-130">-WhatIf</span></span>
<span data-ttu-id="6fbf9-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbf9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbf9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbf9-133">CommonParameters</span></span>
<span data-ttu-id="6fbf9-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbf9-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbf9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbf9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbf9-136">INPUTS</span></span>

### <span data-ttu-id="6fbf9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6fbf9-137">System.String</span></span>

### <span data-ttu-id="6fbf9-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="6fbf9-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6fbf9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fbf9-139">OUTPUTS</span></span>

### <span data-ttu-id="6fbf9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fbf9-140">System.Boolean</span></span>

## <span data-ttu-id="6fbf9-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fbf9-141">NOTES</span></span>

## <span data-ttu-id="6fbf9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fbf9-142">RELATED LINKS</span></span>
