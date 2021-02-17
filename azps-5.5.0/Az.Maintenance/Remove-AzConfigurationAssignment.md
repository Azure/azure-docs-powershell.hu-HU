---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147570"
---
# <span data-ttu-id="58e6d-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="58e6d-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="58e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="58e6d-103">Erőforrás konfigurációjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="58e6d-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="58e6d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58e6d-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e6d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="58e6d-106">Erőforrás konfigurációjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="58e6d-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="58e6d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="58e6d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="58e6d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="58e6d-109">Erőforrás konfigurációjának regisztrációjának a regisztrációját.</span><span class="sxs-lookup"><span data-stu-id="58e6d-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="58e6d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e6d-110">PARAMETERS</span></span>

### <span data-ttu-id="58e6d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58e6d-111">-AsJob</span></span>
<span data-ttu-id="58e6d-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="58e6d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58e6d-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="58e6d-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="58e6d-114">A konfigurációs hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="58e6d-114">The configuration assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e6d-115">-DefaultProfile</span></span>
<span data-ttu-id="58e6d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58e6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e6d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="58e6d-117">-Force</span></span>
<span data-ttu-id="58e6d-118">Eltávolítás kényszerítés megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="58e6d-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="58e6d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58e6d-119">-PassThru</span></span>
<span data-ttu-id="58e6d-120">Az Eltávolítás művelet állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="58e6d-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="58e6d-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="58e6d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58e6d-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="58e6d-122">-ProviderName</span></span>
<span data-ttu-id="58e6d-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="58e6d-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="58e6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="58e6d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58e6d-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="58e6d-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58e6d-126">-ResourceName</span></span>
<span data-ttu-id="58e6d-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="58e6d-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e6d-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="58e6d-128">-ResourceParentName</span></span>
<span data-ttu-id="58e6d-129">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="58e6d-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e6d-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="58e6d-130">-ResourceParentType</span></span>
<span data-ttu-id="58e6d-131">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="58e6d-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e6d-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="58e6d-132">-ResourceType</span></span>
<span data-ttu-id="58e6d-133">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="58e6d-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e6d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e6d-134">-Confirm</span></span>
<span data-ttu-id="58e6d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58e6d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e6d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e6d-136">-WhatIf</span></span>
<span data-ttu-id="58e6d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58e6d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e6d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58e6d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e6d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e6d-139">CommonParameters</span></span>
<span data-ttu-id="58e6d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e6d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e6d-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58e6d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e6d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58e6d-142">INPUTS</span></span>

### <span data-ttu-id="58e6d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="58e6d-143">System.String</span></span>

## <span data-ttu-id="58e6d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58e6d-144">OUTPUTS</span></span>

### <span data-ttu-id="58e6d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58e6d-145">System.Boolean</span></span>

## <span data-ttu-id="58e6d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58e6d-146">NOTES</span></span>

## <span data-ttu-id="58e6d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58e6d-147">RELATED LINKS</span></span>
