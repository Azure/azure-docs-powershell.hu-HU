---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144858"
---
# <span data-ttu-id="03174-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="03174-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="03174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03174-102">SYNOPSIS</span></span>
<span data-ttu-id="03174-103">Eltávolít egy tárolószolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="03174-103">Removes a container service.</span></span>

## <span data-ttu-id="03174-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03174-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03174-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03174-105">DESCRIPTION</span></span>
<span data-ttu-id="03174-106">A **Remove-AzContainerService** parancsmag eltávolít egy tárolószolgáltatást az Azure-fiókjából.</span><span class="sxs-lookup"><span data-stu-id="03174-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="03174-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03174-107">EXAMPLES</span></span>

### <span data-ttu-id="03174-108">1. példa: Tárolószolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="03174-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="03174-109">Ez a parancs eltávolítja a CSResourceGroup17 nevű tárolószolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="03174-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="03174-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03174-110">PARAMETERS</span></span>

### <span data-ttu-id="03174-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03174-111">-AsJob</span></span>
<span data-ttu-id="03174-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="03174-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="03174-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03174-113">-DefaultProfile</span></span>
<span data-ttu-id="03174-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03174-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03174-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03174-115">-Force</span></span>
<span data-ttu-id="03174-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="03174-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03174-117">-Name</span><span class="sxs-lookup"><span data-stu-id="03174-117">-Name</span></span>
<span data-ttu-id="03174-118">Annak a tárolószolgáltatásnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="03174-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03174-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03174-119">-ResourceGroupName</span></span>
<span data-ttu-id="03174-120">A parancsmag által eltávolított tárolószolgáltatás erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03174-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03174-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03174-121">-Confirm</span></span>
<span data-ttu-id="03174-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03174-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03174-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03174-123">-WhatIf</span></span>
<span data-ttu-id="03174-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03174-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03174-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03174-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03174-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03174-126">CommonParameters</span></span>
<span data-ttu-id="03174-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03174-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03174-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03174-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03174-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03174-129">INPUTS</span></span>

### <span data-ttu-id="03174-130">System.String</span><span class="sxs-lookup"><span data-stu-id="03174-130">System.String</span></span>

## <span data-ttu-id="03174-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03174-131">OUTPUTS</span></span>

### <span data-ttu-id="03174-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="03174-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="03174-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03174-133">NOTES</span></span>

## <span data-ttu-id="03174-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03174-134">RELATED LINKS</span></span>

[<span data-ttu-id="03174-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="03174-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="03174-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="03174-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="03174-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="03174-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


