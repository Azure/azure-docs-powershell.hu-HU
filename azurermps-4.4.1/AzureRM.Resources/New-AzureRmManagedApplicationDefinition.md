---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504748"
---
# <span data-ttu-id="8cf94-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="8cf94-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="8cf94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cf94-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf94-103">Felügyelt alkalmazás-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cf94-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cf94-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cf94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cf94-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf94-106">A **New-AzureRmManagedApplicationDefinition** parancsmag létrehoz egy felügyelt alkalmazás-definíciót.</span><span class="sxs-lookup"><span data-stu-id="8cf94-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="8cf94-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8cf94-107">EXAMPLES</span></span>

### <span data-ttu-id="8cf94-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cf94-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="8cf94-109">Ez a parancs felügyelt alkalmazás-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cf94-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="8cf94-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cf94-110">PARAMETERS</span></span>

### <span data-ttu-id="8cf94-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cf94-111">-ApiVersion</span></span>
<span data-ttu-id="8cf94-112">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf94-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8cf94-113">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8cf94-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8cf94-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="8cf94-114">-Authorization</span></span>
<span data-ttu-id="8cf94-115">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="8cf94-115">The managed application definition authorization.</span></span>
<span data-ttu-id="8cf94-116">Vesszővel elválasztott engedélyezési párok a következő formátumban \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="8cf94-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="8cf94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf94-117">-DefaultProfile</span></span>
<span data-ttu-id="8cf94-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cf94-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf94-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8cf94-119">-Description</span></span>
<span data-ttu-id="8cf94-120">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="8cf94-120">The managed application definition description.</span></span>

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

### <span data-ttu-id="8cf94-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8cf94-121">-DisplayName</span></span>
<span data-ttu-id="8cf94-122">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="8cf94-122">The managed application definition display name.</span></span>

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

### <span data-ttu-id="8cf94-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="8cf94-123">-Location</span></span>
<span data-ttu-id="8cf94-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8cf94-124">The resource location.</span></span>

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

### <span data-ttu-id="8cf94-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="8cf94-125">-LockLevel</span></span>
<span data-ttu-id="8cf94-126">A felügyelt alkalmazás definíciójának zárolási szintje.</span><span class="sxs-lookup"><span data-stu-id="8cf94-126">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="8cf94-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cf94-127">-Name</span></span>
<span data-ttu-id="8cf94-128">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="8cf94-128">The managed application definition name.</span></span>

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

### <span data-ttu-id="8cf94-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="8cf94-129">-PackageFileUri</span></span>
<span data-ttu-id="8cf94-130">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="8cf94-130">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="8cf94-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="8cf94-131">-Pre</span></span>
<span data-ttu-id="8cf94-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8cf94-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8cf94-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf94-133">-ResourceGroupName</span></span>
<span data-ttu-id="8cf94-134">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8cf94-134">The resource group name.</span></span>

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

### <span data-ttu-id="8cf94-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="8cf94-135">-Tag</span></span>
<span data-ttu-id="8cf94-136">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8cf94-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8cf94-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8cf94-137">-Confirm</span></span>
<span data-ttu-id="8cf94-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8cf94-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf94-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf94-139">-WhatIf</span></span>
<span data-ttu-id="8cf94-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8cf94-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf94-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cf94-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf94-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="8cf94-142">-CreateUiDefinition</span></span>
<span data-ttu-id="8cf94-143">A felügyelt alkalmazás definíciója: a felhasználói felület definíciójának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="8cf94-143">The managed application definition create ui definition.</span></span>

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

### <span data-ttu-id="8cf94-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="8cf94-144">-MainTemplate</span></span>
<span data-ttu-id="8cf94-145">A felügyelt alkalmazás-definíciós fő sablon.</span><span class="sxs-lookup"><span data-stu-id="8cf94-145">The managed application definition main template.</span></span>

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

### <span data-ttu-id="8cf94-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf94-146">CommonParameters</span></span>
<span data-ttu-id="8cf94-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cf94-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf94-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf94-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf94-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf94-149">INPUTS</span></span>

### <span data-ttu-id="8cf94-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8cf94-150">System.String</span></span>
<span data-ttu-id="8cf94-151">Microsoft. Azure. Command. ResourceManager. Parancsmags. jogalanyok. Application. ApplicationLockLevel System. string [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8cf94-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="8cf94-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf94-152">OUTPUTS</span></span>

### <span data-ttu-id="8cf94-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8cf94-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8cf94-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cf94-154">NOTES</span></span>

## <span data-ttu-id="8cf94-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cf94-155">RELATED LINKS</span></span>

