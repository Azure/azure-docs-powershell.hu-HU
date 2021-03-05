---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012182"
---
# <span data-ttu-id="73787-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="73787-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="73787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73787-102">SYNOPSIS</span></span>
<span data-ttu-id="73787-103">Frissítse a DevSpaces-vezérlőt címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="73787-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="73787-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73787-104">SYNTAX</span></span>

### <span data-ttu-id="73787-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73787-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73787-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73787-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73787-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73787-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73787-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73787-108">DESCRIPTION</span></span>
<span data-ttu-id="73787-109">Frissítse a DevSpaces-vezérlőt címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="73787-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="73787-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73787-110">EXAMPLES</span></span>

### <span data-ttu-id="73787-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="73787-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="73787-112">DevSpaces-vezérlő címkézése.</span><span class="sxs-lookup"><span data-stu-id="73787-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="73787-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73787-113">PARAMETERS</span></span>

### <span data-ttu-id="73787-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73787-114">-DefaultProfile</span></span>
<span data-ttu-id="73787-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73787-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73787-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73787-116">-InputObject</span></span>
<span data-ttu-id="73787-117">Egy PSController-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="73787-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="73787-118">-Name</span><span class="sxs-lookup"><span data-stu-id="73787-118">-Name</span></span>
<span data-ttu-id="73787-119">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="73787-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="73787-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73787-120">-ResourceGroupName</span></span>
<span data-ttu-id="73787-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="73787-121">Resource group name</span></span>

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

### <span data-ttu-id="73787-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73787-122">-ResourceId</span></span>
<span data-ttu-id="73787-123">A DevSpaces erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="73787-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="73787-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="73787-124">-Tag</span></span>
<span data-ttu-id="73787-125">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="73787-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73787-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73787-126">-Confirm</span></span>
<span data-ttu-id="73787-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73787-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73787-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73787-128">-WhatIf</span></span>
<span data-ttu-id="73787-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73787-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73787-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73787-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73787-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73787-131">CommonParameters</span></span>
<span data-ttu-id="73787-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73787-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73787-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73787-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73787-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73787-134">INPUTS</span></span>

### <span data-ttu-id="73787-135">System.String</span><span class="sxs-lookup"><span data-stu-id="73787-135">System.String</span></span>

### <span data-ttu-id="73787-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="73787-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="73787-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73787-137">OUTPUTS</span></span>

### <span data-ttu-id="73787-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="73787-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="73787-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73787-139">NOTES</span></span>

## <span data-ttu-id="73787-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73787-140">RELATED LINKS</span></span>
