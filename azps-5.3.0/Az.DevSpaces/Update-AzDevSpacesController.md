---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467850"
---
# <span data-ttu-id="0a5f7-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="0a5f7-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="0a5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5f7-103">Frissítse a DevSpaces-vezérlőt címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="0a5f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a5f7-104">SYNTAX</span></span>

### <span data-ttu-id="0a5f7-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a5f7-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a5f7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a5f7-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a5f7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a5f7-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5f7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a5f7-108">DESCRIPTION</span></span>
<span data-ttu-id="0a5f7-109">Frissítse a DevSpaces-vezérlőt címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="0a5f7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a5f7-110">EXAMPLES</span></span>

### <span data-ttu-id="0a5f7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a5f7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="0a5f7-112">DevSpaces-vezérlő címkézése.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="0a5f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5f7-113">PARAMETERS</span></span>

### <span data-ttu-id="0a5f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5f7-114">-DefaultProfile</span></span>
<span data-ttu-id="0a5f7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5f7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a5f7-116">-InputObject</span></span>
<span data-ttu-id="0a5f7-117">Egy PSController-objektum, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a5f7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0a5f7-118">-Name</span></span>
<span data-ttu-id="0a5f7-119">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="0a5f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a5f7-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0a5f7-121">Resource group name</span></span>

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

### <span data-ttu-id="0a5f7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a5f7-122">-ResourceId</span></span>
<span data-ttu-id="0a5f7-123">A DevSpaces erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="0a5f7-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="0a5f7-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a5f7-124">-Tag</span></span>
<span data-ttu-id="0a5f7-125">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0a5f7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5f7-126">-Confirm</span></span>
<span data-ttu-id="0a5f7-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5f7-128">-WhatIf</span></span>
<span data-ttu-id="0a5f7-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5f7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5f7-131">CommonParameters</span></span>
<span data-ttu-id="0a5f7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5f7-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5f7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5f7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a5f7-134">INPUTS</span></span>

### <span data-ttu-id="0a5f7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0a5f7-135">System.String</span></span>

### <span data-ttu-id="0a5f7-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="0a5f7-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="0a5f7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a5f7-137">OUTPUTS</span></span>

### <span data-ttu-id="0a5f7-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="0a5f7-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="0a5f7-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a5f7-139">NOTES</span></span>

## <span data-ttu-id="0a5f7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a5f7-140">RELATED LINKS</span></span>
