---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 097248e06acd081582ecc34a863658b2b073ef60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004213"
---
# <span data-ttu-id="4b50b-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="4b50b-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="4b50b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b50b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b50b-103">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="4b50b-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="4b50b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b50b-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b50b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b50b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b50b-106">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="4b50b-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="4b50b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b50b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b50b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4b50b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4b50b-109">DevSpaces-vezérlő létrehozása az resourcegroup devSpaceResourceGroup csoportban devSpaceName néven.</span><span class="sxs-lookup"><span data-stu-id="4b50b-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="4b50b-110">Használja a clusterName fürtöt a vezérlő céljaként.</span><span class="sxs-lookup"><span data-stu-id="4b50b-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="4b50b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b50b-111">PARAMETERS</span></span>

### <span data-ttu-id="4b50b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b50b-112">-AsJob</span></span>
<span data-ttu-id="4b50b-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4b50b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b50b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b50b-114">-DefaultProfile</span></span>
<span data-ttu-id="4b50b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b50b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b50b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4b50b-116">-Name</span></span>
<span data-ttu-id="4b50b-117">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="4b50b-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b50b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b50b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b50b-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b50b-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b50b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b50b-120">-Tag</span></span>
<span data-ttu-id="4b50b-121">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="4b50b-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4b50b-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="4b50b-122">-TargetClusterName</span></span>
<span data-ttu-id="4b50b-123">Célcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b50b-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b50b-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b50b-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="4b50b-125">Célerőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b50b-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b50b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b50b-126">-Confirm</span></span>
<span data-ttu-id="4b50b-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b50b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b50b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b50b-128">-WhatIf</span></span>
<span data-ttu-id="4b50b-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b50b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b50b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b50b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b50b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b50b-131">CommonParameters</span></span>
<span data-ttu-id="4b50b-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b50b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b50b-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b50b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b50b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b50b-134">INPUTS</span></span>

### <span data-ttu-id="4b50b-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="4b50b-135">None</span></span>

## <span data-ttu-id="4b50b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b50b-136">OUTPUTS</span></span>

### <span data-ttu-id="4b50b-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="4b50b-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4b50b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b50b-138">NOTES</span></span>

## <span data-ttu-id="4b50b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b50b-139">RELATED LINKS</span></span>
