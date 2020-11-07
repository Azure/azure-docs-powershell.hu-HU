---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 1c59b6aba1a839086bb923556c86e3b93b80365a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669392"
---
# <span data-ttu-id="de470-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="de470-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="de470-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de470-102">SYNOPSIS</span></span>
<span data-ttu-id="de470-103">Felügyelt alkalmazás-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de470-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="de470-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de470-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de470-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de470-105">DESCRIPTION</span></span>
<span data-ttu-id="de470-106">A **New-AzManagedApplicationDefinition** parancsmag létrehoz egy felügyelt alkalmazás-definíciót.</span><span class="sxs-lookup"><span data-stu-id="de470-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="de470-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de470-107">EXAMPLES</span></span>

### <span data-ttu-id="de470-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de470-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="de470-109">Ez a parancs felügyelt alkalmazás-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de470-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="de470-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de470-110">PARAMETERS</span></span>

### <span data-ttu-id="de470-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de470-111">-ApiVersion</span></span>
<span data-ttu-id="de470-112">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="de470-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="de470-113">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="de470-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="de470-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="de470-114">-Authorization</span></span>
<span data-ttu-id="de470-115">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="de470-115">The managed application definition authorization.</span></span>
<span data-ttu-id="de470-116">Vesszővel elválasztott engedélyezési párok a \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="de470-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="de470-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="de470-117">-CreateUiDefinition</span></span>
<span data-ttu-id="de470-118">A felügyelt alkalmazás definíciója a felhasználói felület definícióját hozza létre</span><span class="sxs-lookup"><span data-stu-id="de470-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="de470-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de470-119">-DefaultProfile</span></span>
<span data-ttu-id="de470-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de470-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de470-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="de470-121">-Description</span></span>
<span data-ttu-id="de470-122">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="de470-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="de470-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de470-123">-DisplayName</span></span>
<span data-ttu-id="de470-124">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="de470-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="de470-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="de470-125">-Location</span></span>
<span data-ttu-id="de470-126">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="de470-126">The resource location.</span></span>

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

### <span data-ttu-id="de470-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="de470-127">-LockLevel</span></span>
<span data-ttu-id="de470-128">A felügyelt alkalmazás definíciójának zárolási szintje.</span><span class="sxs-lookup"><span data-stu-id="de470-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="de470-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="de470-129">-MainTemplate</span></span>
<span data-ttu-id="de470-130">A felügyelt alkalmazás-definíciós fő sablon</span><span class="sxs-lookup"><span data-stu-id="de470-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="de470-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de470-131">-Name</span></span>
<span data-ttu-id="de470-132">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="de470-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="de470-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="de470-133">-PackageFileUri</span></span>
<span data-ttu-id="de470-134">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="de470-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="de470-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="de470-135">-Pre</span></span>
<span data-ttu-id="de470-136">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="de470-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de470-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de470-137">-ResourceGroupName</span></span>
<span data-ttu-id="de470-138">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de470-138">The resource group name.</span></span>

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

### <span data-ttu-id="de470-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="de470-139">-Tag</span></span>
<span data-ttu-id="de470-140">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="de470-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="de470-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de470-141">-Confirm</span></span>
<span data-ttu-id="de470-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de470-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de470-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de470-143">-WhatIf</span></span>
<span data-ttu-id="de470-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de470-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de470-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de470-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de470-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de470-146">CommonParameters</span></span>
<span data-ttu-id="de470-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de470-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de470-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de470-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de470-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de470-149">INPUTS</span></span>

### <span data-ttu-id="de470-150">System. String</span><span class="sxs-lookup"><span data-stu-id="de470-150">System.String</span></span>

### <span data-ttu-id="de470-151">Microsoft. Azure. Command. ResourceManager. Parancsmags. jogalanyok. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="de470-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="de470-152">System. string []</span><span class="sxs-lookup"><span data-stu-id="de470-152">System.String[]</span></span>

### <span data-ttu-id="de470-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de470-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de470-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de470-154">OUTPUTS</span></span>

### <span data-ttu-id="de470-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="de470-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="de470-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de470-156">NOTES</span></span>

## <span data-ttu-id="de470-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de470-157">RELATED LINKS</span></span>
