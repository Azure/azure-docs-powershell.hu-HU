---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358020"
---
# <span data-ttu-id="6562f-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6562f-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="6562f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6562f-102">SYNOPSIS</span></span>
<span data-ttu-id="6562f-103">Felügyelt alkalmazásdefiníciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6562f-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="6562f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6562f-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6562f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6562f-105">DESCRIPTION</span></span>
<span data-ttu-id="6562f-106">A **New-AzManagedApplicationDefinition parancsmag** létrehoz egy felügyelt alkalmazásdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="6562f-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="6562f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6562f-107">EXAMPLES</span></span>

### <span data-ttu-id="6562f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6562f-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="6562f-109">Ez a parancs felügyelt alkalmazásdefiníciót hoz létre</span><span class="sxs-lookup"><span data-stu-id="6562f-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="6562f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6562f-110">PARAMETERS</span></span>

### <span data-ttu-id="6562f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6562f-111">-ApiVersion</span></span>
<span data-ttu-id="6562f-112">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="6562f-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6562f-113">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6562f-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6562f-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="6562f-114">-Authorization</span></span>
<span data-ttu-id="6562f-115">A felügyelt alkalmazásdefiníció engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="6562f-115">The managed application definition authorization.</span></span>
<span data-ttu-id="6562f-116">Vesszővel elválasztott engedélyezési párok a következő \<principalId\> formátumban:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="6562f-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6562f-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="6562f-117">-CreateUiDefinition</span></span>
<span data-ttu-id="6562f-118">The managed application definition create ui definition</span><span class="sxs-lookup"><span data-stu-id="6562f-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="6562f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6562f-119">-DefaultProfile</span></span>
<span data-ttu-id="6562f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6562f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6562f-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6562f-121">-Description</span></span>
<span data-ttu-id="6562f-122">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="6562f-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="6562f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6562f-123">-DisplayName</span></span>
<span data-ttu-id="6562f-124">A felügyelt alkalmazásdefiníció megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="6562f-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="6562f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="6562f-125">-Location</span></span>
<span data-ttu-id="6562f-126">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6562f-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6562f-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="6562f-127">-LockLevel</span></span>
<span data-ttu-id="6562f-128">A felügyelt alkalmazásdefiníció zárolási szintje.</span><span class="sxs-lookup"><span data-stu-id="6562f-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6562f-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="6562f-129">-MainTemplate</span></span>
<span data-ttu-id="6562f-130">A felügyelt alkalmazás definíciójának fősablonja</span><span class="sxs-lookup"><span data-stu-id="6562f-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="6562f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6562f-131">-Name</span></span>
<span data-ttu-id="6562f-132">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="6562f-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="6562f-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="6562f-133">-PackageFileUri</span></span>
<span data-ttu-id="6562f-134">A felügyelt alkalmazásdefiníciós csomag uri.</span><span class="sxs-lookup"><span data-stu-id="6562f-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="6562f-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6562f-135">-Pre</span></span>
<span data-ttu-id="6562f-136">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6562f-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6562f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6562f-137">-ResourceGroupName</span></span>
<span data-ttu-id="6562f-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6562f-138">The resource group name.</span></span>

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

### <span data-ttu-id="6562f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6562f-139">-Tag</span></span>
<span data-ttu-id="6562f-140">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="6562f-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6562f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6562f-141">-Confirm</span></span>
<span data-ttu-id="6562f-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6562f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6562f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6562f-143">-WhatIf</span></span>
<span data-ttu-id="6562f-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6562f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6562f-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6562f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6562f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6562f-146">CommonParameters</span></span>
<span data-ttu-id="6562f-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6562f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6562f-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6562f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6562f-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6562f-149">INPUTS</span></span>

### <span data-ttu-id="6562f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6562f-150">System.String</span></span>

### <span data-ttu-id="6562f-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="6562f-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="6562f-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6562f-152">System.String[]</span></span>

### <span data-ttu-id="6562f-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6562f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6562f-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6562f-154">OUTPUTS</span></span>

### <span data-ttu-id="6562f-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6562f-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6562f-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6562f-156">NOTES</span></span>

## <span data-ttu-id="6562f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6562f-157">RELATED LINKS</span></span>
