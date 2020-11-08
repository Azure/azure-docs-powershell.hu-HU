---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: aa9f743e8500450245bed96305138f4bf6e25c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011739"
---
# <span data-ttu-id="f0b6e-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f0b6e-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="f0b6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b6e-103">A felügyelt alkalmazások definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f0b6e-103">Updates managed application definition</span></span>

## <span data-ttu-id="f0b6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0b6e-104">SYNTAX</span></span>

### <span data-ttu-id="f0b6e-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0b6e-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0b6e-106">SetById</span><span class="sxs-lookup"><span data-stu-id="f0b6e-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b6e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0b6e-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b6e-108">A **set-AzManagedApplicationDefinition** parancsmag frissíti a felügyelt alkalmazás-definíciókat</span><span class="sxs-lookup"><span data-stu-id="f0b6e-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="f0b6e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f0b6e-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b6e-110">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f0b6e-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="f0b6e-111">Ez a parancs frissíti a felügyelt alkalmazás definíciójának leírását.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="f0b6e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0b6e-112">PARAMETERS</span></span>

### <span data-ttu-id="f0b6e-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0b6e-113">-ApiVersion</span></span>
<span data-ttu-id="f0b6e-114">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0b6e-115">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f0b6e-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="f0b6e-116">-Authorization</span></span>
<span data-ttu-id="f0b6e-117">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-117">The managed application definition authorization.</span></span>
<span data-ttu-id="f0b6e-118">Vesszővel elválasztott engedélyezési párok a \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="f0b6e-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b6e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b6e-119">-DefaultProfile</span></span>
<span data-ttu-id="f0b6e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0b6e-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f0b6e-121">-Description</span></span>
<span data-ttu-id="f0b6e-122">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="f0b6e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f0b6e-123">-DisplayName</span></span>
<span data-ttu-id="f0b6e-124">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="f0b6e-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f0b6e-125">-Id</span></span>
<span data-ttu-id="f0b6e-126">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="f0b6e-127">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b6e-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b6e-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0b6e-128">-Name</span></span>
<span data-ttu-id="f0b6e-129">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b6e-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f0b6e-130">-PackageFileUri</span></span>
<span data-ttu-id="f0b6e-131">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f0b6e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0b6e-132">-Pre</span></span>
<span data-ttu-id="f0b6e-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f0b6e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b6e-134">-ResourceGroupName</span></span>
<span data-ttu-id="f0b6e-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b6e-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="f0b6e-136">-Tag</span></span>
<span data-ttu-id="f0b6e-137">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f0b6e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0b6e-138">-Confirm</span></span>
<span data-ttu-id="f0b6e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b6e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b6e-140">-WhatIf</span></span>
<span data-ttu-id="f0b6e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b6e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b6e-143">CommonParameters</span></span>
<span data-ttu-id="f0b6e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0b6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b6e-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b6e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0b6e-146">INPUTS</span></span>

### <span data-ttu-id="f0b6e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b6e-147">System.String</span></span>

### <span data-ttu-id="f0b6e-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="f0b6e-148">System.String[]</span></span>

### <span data-ttu-id="f0b6e-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0b6e-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0b6e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0b6e-150">OUTPUTS</span></span>

### <span data-ttu-id="f0b6e-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f0b6e-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f0b6e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0b6e-152">NOTES</span></span>

## <span data-ttu-id="f0b6e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0b6e-153">RELATED LINKS</span></span>
