---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493370"
---
# <span data-ttu-id="62484-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="62484-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="62484-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62484-102">SYNOPSIS</span></span>
<span data-ttu-id="62484-103">A felügyelt alkalmazások definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="62484-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62484-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62484-104">SYNTAX</span></span>

### <span data-ttu-id="62484-105">A Managed Application Definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="62484-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="62484-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="62484-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62484-107">A felügyelt alkalmazás-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="62484-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62484-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="62484-108">DESCRIPTION</span></span>
<span data-ttu-id="62484-109">A **set-AzureRmManagedApplicationDefinition** parancsmag frissíti a felügyelt alkalmazás-definíciókat</span><span class="sxs-lookup"><span data-stu-id="62484-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="62484-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62484-110">EXAMPLES</span></span>

### <span data-ttu-id="62484-111">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="62484-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="62484-112">Ez a parancs frissíti a felügyelt alkalmazás definíciójának leírását.</span><span class="sxs-lookup"><span data-stu-id="62484-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="62484-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62484-113">PARAMETERS</span></span>

### <span data-ttu-id="62484-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62484-114">-ApiVersion</span></span>
<span data-ttu-id="62484-115">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62484-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="62484-116">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="62484-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="62484-117">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="62484-117">-Authorization</span></span>
<span data-ttu-id="62484-118">A felügyelt alkalmazás definíciós engedélye.</span><span class="sxs-lookup"><span data-stu-id="62484-118">The managed application definition authorization.</span></span>
<span data-ttu-id="62484-119">Vesszővel elválasztott engedélyezési párok a következő formátumban \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="62484-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="62484-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62484-120">-DefaultProfile</span></span>
<span data-ttu-id="62484-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62484-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62484-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="62484-122">-Description</span></span>
<span data-ttu-id="62484-123">A felügyelt alkalmazás definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="62484-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="62484-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="62484-124">-DisplayName</span></span>
<span data-ttu-id="62484-125">A felügyelt alkalmazás definícióját megjelenítő név.</span><span class="sxs-lookup"><span data-stu-id="62484-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="62484-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62484-126">-Name</span></span>
<span data-ttu-id="62484-127">A felügyelt alkalmazás definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="62484-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62484-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="62484-128">-PackageFileUri</span></span>
<span data-ttu-id="62484-129">A felügyelt alkalmazás-definíciós csomagfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="62484-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="62484-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="62484-130">-Pre</span></span>
<span data-ttu-id="62484-131">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="62484-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="62484-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62484-132">-ResourceGroupName</span></span>
<span data-ttu-id="62484-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="62484-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62484-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="62484-134">-Tag</span></span>
<span data-ttu-id="62484-135">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="62484-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="62484-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62484-136">-Confirm</span></span>
<span data-ttu-id="62484-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62484-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62484-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62484-138">-WhatIf</span></span>
<span data-ttu-id="62484-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62484-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62484-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62484-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62484-141">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="62484-141">-Id</span></span>
<span data-ttu-id="62484-142">A teljes mértékben minősített felügyelt alkalmazás-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="62484-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="62484-143">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="62484-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62484-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62484-144">CommonParameters</span></span>
<span data-ttu-id="62484-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62484-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62484-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62484-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62484-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62484-147">INPUTS</span></span>

### <span data-ttu-id="62484-148">System. String</span><span class="sxs-lookup"><span data-stu-id="62484-148">System.String</span></span>
<span data-ttu-id="62484-149">System. string [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62484-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="62484-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62484-150">OUTPUTS</span></span>

### <span data-ttu-id="62484-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="62484-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="62484-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62484-152">NOTES</span></span>

## <span data-ttu-id="62484-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62484-153">RELATED LINKS</span></span>

