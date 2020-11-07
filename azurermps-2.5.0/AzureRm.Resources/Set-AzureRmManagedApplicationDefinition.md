---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848646"
---
# <span data-ttu-id="49c39-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="49c39-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="49c39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49c39-102">SYNOPSIS</span></span>
<span data-ttu-id="49c39-103">A felügyelt alkalmazások definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="49c39-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49c39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49c39-104">SYNTAX</span></span>

### <span data-ttu-id="49c39-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49c39-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49c39-106">SetById</span><span class="sxs-lookup"><span data-stu-id="49c39-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c39-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="49c39-107">DESCRIPTION</span></span>
<span data-ttu-id="49c39-108">A **set-AzureRmManagedApplicationDefinition** parancsmag frissíti a felügyelt alkalmazás-definíciókat</span><span class="sxs-lookup"><span data-stu-id="49c39-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="49c39-109">Példák</span><span class="sxs-lookup"><span data-stu-id="49c39-109">EXAMPLES</span></span>

### <span data-ttu-id="49c39-110">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="49c39-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="49c39-111">Ez a parancs frissíti a felügyelt alkalmazás definíciójának leírását.</span><span class="sxs-lookup"><span data-stu-id="49c39-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="49c39-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49c39-112">PARAMETERS</span></span>

### <span data-ttu-id="49c39-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49c39-113">-ApiVersion</span></span>
<span data-ttu-id="49c39-114">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49c39-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="49c39-115">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="49c39-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="49c39-116">-Authorization</span></span>
<span data-ttu-id="49c39-117">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="49c39-117">The managed application definition authorization.</span></span>
<span data-ttu-id="49c39-118">Vesszővel elválasztott engedélyezési párok a következő formátumban \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="49c39-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c39-119">-DefaultProfile</span></span>
<span data-ttu-id="49c39-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49c39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="49c39-121">-Description</span></span>
<span data-ttu-id="49c39-122">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="49c39-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49c39-123">-DisplayName</span></span>
<span data-ttu-id="49c39-124">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="49c39-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="49c39-125">-Id</span></span>
<span data-ttu-id="49c39-126">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="49c39-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="49c39-127">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c39-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49c39-128">-Name</span></span>
<span data-ttu-id="49c39-129">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="49c39-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="49c39-130">-PackageFileUri</span></span>
<span data-ttu-id="49c39-131">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="49c39-131">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="49c39-132">-Pre</span></span>
<span data-ttu-id="49c39-133">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="49c39-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c39-134">-ResourceGroupName</span></span>
<span data-ttu-id="49c39-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="49c39-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="49c39-136">-Tag</span></span>
<span data-ttu-id="49c39-137">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="49c39-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49c39-138">-Confirm</span></span>
<span data-ttu-id="49c39-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49c39-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c39-140">-WhatIf</span></span>
<span data-ttu-id="49c39-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49c39-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c39-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49c39-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c39-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c39-143">CommonParameters</span></span>
<span data-ttu-id="49c39-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49c39-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c39-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c39-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c39-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49c39-146">INPUTS</span></span>

### <span data-ttu-id="49c39-147">System. String</span><span class="sxs-lookup"><span data-stu-id="49c39-147">System.String</span></span>
<span data-ttu-id="49c39-148">System. string [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="49c39-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="49c39-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49c39-149">OUTPUTS</span></span>

### <span data-ttu-id="49c39-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="49c39-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="49c39-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49c39-151">NOTES</span></span>

## <span data-ttu-id="49c39-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49c39-152">RELATED LINKS</span></span>
