---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163067"
---
# <span data-ttu-id="c55da-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c55da-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="c55da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c55da-102">SYNOPSIS</span></span>
<span data-ttu-id="c55da-103">Eltávolít egy felhasználót egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="c55da-103">Removes a user on a device.</span></span>

## <span data-ttu-id="c55da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c55da-104">SYNTAX</span></span>

### <span data-ttu-id="c55da-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c55da-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55da-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c55da-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55da-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c55da-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c55da-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c55da-108">DESCRIPTION</span></span>
<span data-ttu-id="c55da-109">A **Remove-AzStackEdgeUser** parancsmag eltávolítja a felhasználót a Stack Edge eszközön.</span><span class="sxs-lookup"><span data-stu-id="c55da-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="c55da-110">Csak a típusú felhasználók `Share` létrehozása támogatott.</span><span class="sxs-lookup"><span data-stu-id="c55da-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c55da-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c55da-111">EXAMPLES</span></span>

### <span data-ttu-id="c55da-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c55da-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="c55da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c55da-113">PARAMETERS</span></span>

### <span data-ttu-id="c55da-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c55da-114">-AsJob</span></span>
<span data-ttu-id="c55da-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c55da-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c55da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55da-116">-DefaultProfile</span></span>
<span data-ttu-id="c55da-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c55da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c55da-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c55da-118">-DeviceName</span></span>
<span data-ttu-id="c55da-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="c55da-119">Device Name</span></span>

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

### <span data-ttu-id="c55da-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c55da-120">-InputObject</span></span>
<span data-ttu-id="c55da-121">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="c55da-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55da-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c55da-122">-Name</span></span>
<span data-ttu-id="c55da-123">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c55da-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55da-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c55da-124">-PassThru</span></span>
<span data-ttu-id="c55da-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="c55da-125">returns true if successful</span></span>

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

### <span data-ttu-id="c55da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55da-126">-ResourceGroupName</span></span>
<span data-ttu-id="c55da-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c55da-127">Resource Group Name</span></span>

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

### <span data-ttu-id="c55da-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c55da-128">-ResourceId</span></span>
<span data-ttu-id="c55da-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c55da-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="c55da-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c55da-130">-Confirm</span></span>
<span data-ttu-id="c55da-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c55da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c55da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c55da-132">-WhatIf</span></span>
<span data-ttu-id="c55da-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c55da-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c55da-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c55da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c55da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55da-135">CommonParameters</span></span>
<span data-ttu-id="c55da-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55da-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c55da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55da-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c55da-138">INPUTS</span></span>

### <span data-ttu-id="c55da-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c55da-139">System.String</span></span>

### <span data-ttu-id="c55da-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c55da-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="c55da-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c55da-141">OUTPUTS</span></span>

### <span data-ttu-id="c55da-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c55da-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c55da-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c55da-143">NOTES</span></span>

## <span data-ttu-id="c55da-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c55da-144">RELATED LINKS</span></span>
