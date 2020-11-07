---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3d6a5488e7e101c904e90d056c8b2ffc03e786fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843206"
---
# <span data-ttu-id="18d70-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="18d70-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="18d70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18d70-102">SYNOPSIS</span></span>
<span data-ttu-id="18d70-103">A felügyelt alkalmazások definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="18d70-103">Updates managed application definition</span></span>

## <span data-ttu-id="18d70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18d70-104">SYNTAX</span></span>

### <span data-ttu-id="18d70-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18d70-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18d70-106">SetById</span><span class="sxs-lookup"><span data-stu-id="18d70-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18d70-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18d70-107">DESCRIPTION</span></span>
<span data-ttu-id="18d70-108">A **set-AzManagedApplicationDefinition** parancsmag frissíti a felügyelt alkalmazás-definíciókat</span><span class="sxs-lookup"><span data-stu-id="18d70-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="18d70-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18d70-109">EXAMPLES</span></span>

### <span data-ttu-id="18d70-110">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="18d70-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="18d70-111">Ez a parancs frissíti a felügyelt alkalmazás definíciójának leírását.</span><span class="sxs-lookup"><span data-stu-id="18d70-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="18d70-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18d70-112">PARAMETERS</span></span>

### <span data-ttu-id="18d70-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18d70-113">-ApiVersion</span></span>
<span data-ttu-id="18d70-114">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18d70-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="18d70-115">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="18d70-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="18d70-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="18d70-116">-Authorization</span></span>
<span data-ttu-id="18d70-117">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="18d70-117">The managed application definition authorization.</span></span>
<span data-ttu-id="18d70-118">Vesszővel elválasztott engedélyezési párok a \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="18d70-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="18d70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d70-119">-DefaultProfile</span></span>
<span data-ttu-id="18d70-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18d70-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d70-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="18d70-121">-Description</span></span>
<span data-ttu-id="18d70-122">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="18d70-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="18d70-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="18d70-123">-DisplayName</span></span>
<span data-ttu-id="18d70-124">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="18d70-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="18d70-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="18d70-125">-Id</span></span>
<span data-ttu-id="18d70-126">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="18d70-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="18d70-127">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d70-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="18d70-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18d70-128">-Name</span></span>
<span data-ttu-id="18d70-129">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="18d70-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="18d70-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="18d70-130">-PackageFileUri</span></span>
<span data-ttu-id="18d70-131">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="18d70-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="18d70-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="18d70-132">-Pre</span></span>
<span data-ttu-id="18d70-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="18d70-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="18d70-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d70-134">-ResourceGroupName</span></span>
<span data-ttu-id="18d70-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="18d70-135">The resource group name.</span></span>

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

### <span data-ttu-id="18d70-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="18d70-136">-Tag</span></span>
<span data-ttu-id="18d70-137">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="18d70-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="18d70-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18d70-138">-Confirm</span></span>
<span data-ttu-id="18d70-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18d70-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18d70-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18d70-140">-WhatIf</span></span>
<span data-ttu-id="18d70-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18d70-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18d70-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18d70-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18d70-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d70-143">CommonParameters</span></span>
<span data-ttu-id="18d70-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18d70-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d70-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d70-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d70-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d70-146">INPUTS</span></span>

### <span data-ttu-id="18d70-147">System. String</span><span class="sxs-lookup"><span data-stu-id="18d70-147">System.String</span></span>

### <span data-ttu-id="18d70-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="18d70-148">System.String[]</span></span>

### <span data-ttu-id="18d70-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18d70-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18d70-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d70-150">OUTPUTS</span></span>

### <span data-ttu-id="18d70-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="18d70-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="18d70-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18d70-152">NOTES</span></span>

## <span data-ttu-id="18d70-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18d70-153">RELATED LINKS</span></span>
