---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210006"
---
# <span data-ttu-id="6d2dc-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6d2dc-101">Remove-AzHost</span></span>

## <span data-ttu-id="6d2dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2dc-103">Eltávolít egy állomást.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-103">Removes a host.</span></span>

## <span data-ttu-id="6d2dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d2dc-104">SYNTAX</span></span>

### <span data-ttu-id="6d2dc-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d2dc-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d2dc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6d2dc-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d2dc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6d2dc-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d2dc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d2dc-108">DESCRIPTION</span></span>
<span data-ttu-id="6d2dc-109">Ez a parancsmag töröl egy állomást</span><span class="sxs-lookup"><span data-stu-id="6d2dc-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="6d2dc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d2dc-110">EXAMPLES</span></span>

### <span data-ttu-id="6d2dc-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d2dc-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="6d2dc-112">Ez a parancs be- és eltávolítja az adott állomást.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="6d2dc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6d2dc-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="6d2dc-114">Ez a parancs eltávolítja az adott állomást.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-114">This command removes the given host.</span></span>

## <span data-ttu-id="6d2dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d2dc-115">PARAMETERS</span></span>

### <span data-ttu-id="6d2dc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d2dc-116">-AsJob</span></span>
<span data-ttu-id="6d2dc-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6d2dc-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d2dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2dc-118">-DefaultProfile</span></span>
<span data-ttu-id="6d2dc-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2dc-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2dc-120">-HostGroupName</span></span>
<span data-ttu-id="6d2dc-121">A gazdacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2dc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d2dc-122">-InputObject</span></span>
<span data-ttu-id="6d2dc-123">Az állomás helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6d2dc-124">-Name</span></span>
<span data-ttu-id="6d2dc-125">Az állomás neve.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d2dc-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2dc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d2dc-128">-ResourceId</span></span>
<span data-ttu-id="6d2dc-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2dc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d2dc-130">-Confirm</span></span>
<span data-ttu-id="6d2dc-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2dc-132">-WhatIf</span></span>
<span data-ttu-id="6d2dc-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d2dc-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2dc-135">CommonParameters</span></span>
<span data-ttu-id="6d2dc-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2dc-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d2dc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2dc-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d2dc-138">INPUTS</span></span>

### <span data-ttu-id="6d2dc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6d2dc-139">System.String</span></span>

### <span data-ttu-id="6d2dc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="6d2dc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="6d2dc-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d2dc-141">OUTPUTS</span></span>

### <span data-ttu-id="6d2dc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6d2dc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6d2dc-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d2dc-143">NOTES</span></span>

## <span data-ttu-id="6d2dc-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d2dc-144">RELATED LINKS</span></span>
