---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341069"
---
# <span data-ttu-id="02a05-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="02a05-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="02a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a05-102">SYNOPSIS</span></span>
<span data-ttu-id="02a05-103">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="02a05-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="02a05-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02a05-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a05-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02a05-105">DESCRIPTION</span></span>
<span data-ttu-id="02a05-106">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="02a05-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="02a05-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02a05-107">EXAMPLES</span></span>

### <span data-ttu-id="02a05-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="02a05-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="02a05-109">DevSpaces-vezérlő létrehozása az resourcegroup devSpaceResourceGroup csoportban devSpaceName néven.</span><span class="sxs-lookup"><span data-stu-id="02a05-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="02a05-110">Használja a clusterName fürtöt a vezérlő céljaként.</span><span class="sxs-lookup"><span data-stu-id="02a05-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="02a05-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a05-111">PARAMETERS</span></span>

### <span data-ttu-id="02a05-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02a05-112">-AsJob</span></span>
<span data-ttu-id="02a05-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="02a05-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02a05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a05-114">-DefaultProfile</span></span>
<span data-ttu-id="02a05-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02a05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a05-116">-Name</span><span class="sxs-lookup"><span data-stu-id="02a05-116">-Name</span></span>
<span data-ttu-id="02a05-117">DevSpaces-vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="02a05-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="02a05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a05-118">-ResourceGroupName</span></span>
<span data-ttu-id="02a05-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02a05-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="02a05-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="02a05-120">-Tag</span></span>
<span data-ttu-id="02a05-121">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="02a05-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="02a05-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="02a05-122">-TargetClusterName</span></span>
<span data-ttu-id="02a05-123">Célcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02a05-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="02a05-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a05-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="02a05-125">Célerőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="02a05-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="02a05-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a05-126">-Confirm</span></span>
<span data-ttu-id="02a05-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02a05-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a05-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a05-128">-WhatIf</span></span>
<span data-ttu-id="02a05-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02a05-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a05-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02a05-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a05-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a05-131">CommonParameters</span></span>
<span data-ttu-id="02a05-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a05-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a05-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a05-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a05-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02a05-134">INPUTS</span></span>

### <span data-ttu-id="02a05-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="02a05-135">None</span></span>

## <span data-ttu-id="02a05-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02a05-136">OUTPUTS</span></span>

### <span data-ttu-id="02a05-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="02a05-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="02a05-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02a05-138">NOTES</span></span>

## <span data-ttu-id="02a05-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02a05-139">RELATED LINKS</span></span>
