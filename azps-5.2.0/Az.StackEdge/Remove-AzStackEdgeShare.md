---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358719"
---
# <span data-ttu-id="fb759-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fb759-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="fb759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb759-102">SYNOPSIS</span></span>
<span data-ttu-id="fb759-103">Eltávolít egy megosztást az eszközről.</span><span class="sxs-lookup"><span data-stu-id="fb759-103">Removes a share from the device.</span></span>

## <span data-ttu-id="fb759-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb759-104">SYNTAX</span></span>

### <span data-ttu-id="fb759-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb759-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb759-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb759-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb759-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb759-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb759-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb759-108">DESCRIPTION</span></span>
<span data-ttu-id="fb759-109">A **Remove-AzStackEdgeEdgeShare** parancsmag eltávolítja a stack edge-hez tartozó szegélymegosztásokat.</span><span class="sxs-lookup"><span data-stu-id="fb759-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="fb759-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb759-110">EXAMPLES</span></span>

### <span data-ttu-id="fb759-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fb759-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="fb759-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb759-112">PARAMETERS</span></span>

### <span data-ttu-id="fb759-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb759-113">-AsJob</span></span>
<span data-ttu-id="fb759-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb759-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb759-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb759-115">-DefaultProfile</span></span>
<span data-ttu-id="fb759-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb759-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb759-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb759-117">-DeviceName</span></span>
<span data-ttu-id="fb759-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="fb759-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb759-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb759-119">-InputObject</span></span>
<span data-ttu-id="fb759-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="fb759-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb759-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fb759-121">-Name</span></span>
<span data-ttu-id="fb759-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fb759-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb759-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb759-123">-PassThru</span></span>
<span data-ttu-id="fb759-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="fb759-124">returns true if successful</span></span>

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

### <span data-ttu-id="fb759-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb759-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb759-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fb759-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb759-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb759-127">-ResourceId</span></span>
<span data-ttu-id="fb759-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb759-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb759-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb759-129">-Confirm</span></span>
<span data-ttu-id="fb759-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fb759-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb759-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb759-131">-WhatIf</span></span>
<span data-ttu-id="fb759-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fb759-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb759-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb759-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb759-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb759-134">CommonParameters</span></span>
<span data-ttu-id="fb759-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb759-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb759-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb759-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb759-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb759-137">INPUTS</span></span>

### <span data-ttu-id="fb759-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fb759-138">System.String</span></span>

### <span data-ttu-id="fb759-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fb759-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="fb759-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb759-140">OUTPUTS</span></span>

### <span data-ttu-id="fb759-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb759-141">System.Boolean</span></span>

## <span data-ttu-id="fb759-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb759-142">NOTES</span></span>

## <span data-ttu-id="fb759-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb759-143">RELATED LINKS</span></span>
