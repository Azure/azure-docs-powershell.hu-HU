---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 8fb6c2d299799849d1e9f2183621e9fc31cc0acd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848649"
---
# <span data-ttu-id="2ea89-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="2ea89-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="2ea89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ea89-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea89-103">A felügyelt alkalmazások frissítése</span><span class="sxs-lookup"><span data-stu-id="2ea89-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ea89-104">SYNTAX</span></span>

### <span data-ttu-id="2ea89-105">SetByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ea89-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea89-106">SetById</span><span class="sxs-lookup"><span data-stu-id="2ea89-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea89-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ea89-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea89-108">A **set-AzureRmManagedApplication** parancsmag frissíti a felügyelt alkalmazásokat</span><span class="sxs-lookup"><span data-stu-id="2ea89-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="2ea89-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2ea89-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea89-110">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="2ea89-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="2ea89-111">Ez a parancs frissíti a felügyelt alkalmazás leírását.</span><span class="sxs-lookup"><span data-stu-id="2ea89-111">This command updates the managed application description</span></span>

## <span data-ttu-id="2ea89-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ea89-112">PARAMETERS</span></span>

### <span data-ttu-id="2ea89-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2ea89-113">-ApiVersion</span></span>
<span data-ttu-id="2ea89-114">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ea89-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2ea89-115">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2ea89-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2ea89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea89-116">-DefaultProfile</span></span>
<span data-ttu-id="2ea89-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ea89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea89-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2ea89-118">-Id</span></span>
<span data-ttu-id="2ea89-119">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="2ea89-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="2ea89-120">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea89-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="2ea89-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="2ea89-121">-Kind</span></span>
<span data-ttu-id="2ea89-122">A felügyelt alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="2ea89-122">The managed application kind.</span></span>
<span data-ttu-id="2ea89-123">A piactér vagy a servicecatalog egyike</span><span class="sxs-lookup"><span data-stu-id="2ea89-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="2ea89-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2ea89-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="2ea89-125">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ea89-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="2ea89-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea89-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="2ea89-127">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ea89-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="2ea89-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ea89-128">-Name</span></span>
<span data-ttu-id="2ea89-129">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="2ea89-129">The managed application name.</span></span>

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

### <span data-ttu-id="2ea89-130">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="2ea89-130">-Parameter</span></span>
<span data-ttu-id="2ea89-131">A felügyelt alkalmazás paramétereinek formázott karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="2ea89-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="2ea89-132">Ez lehet az elérési út a paramétereket tartalmazó fájlnév vagy URI-azonosítók, illetve a paraméterek karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2ea89-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="2ea89-133">-Terv</span><span class="sxs-lookup"><span data-stu-id="2ea89-133">-Plan</span></span>
<span data-ttu-id="2ea89-134">Egy kivonatoló táblázat, amely A felügyelt alkalmazási terv tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2ea89-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea89-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="2ea89-135">-Pre</span></span>
<span data-ttu-id="2ea89-136">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2ea89-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2ea89-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea89-137">-ResourceGroupName</span></span>
<span data-ttu-id="2ea89-138">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ea89-138">The resource group name.</span></span>

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

### <span data-ttu-id="2ea89-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="2ea89-139">-Tag</span></span>
<span data-ttu-id="2ea89-140">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="2ea89-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2ea89-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ea89-141">-Confirm</span></span>
<span data-ttu-id="2ea89-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ea89-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea89-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea89-143">-WhatIf</span></span>
<span data-ttu-id="2ea89-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ea89-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea89-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ea89-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea89-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea89-146">CommonParameters</span></span>
<span data-ttu-id="2ea89-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ea89-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea89-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea89-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea89-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea89-149">INPUTS</span></span>

### <span data-ttu-id="2ea89-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea89-150">System.String</span></span>
<span data-ttu-id="2ea89-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ea89-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ea89-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea89-152">OUTPUTS</span></span>

### <span data-ttu-id="2ea89-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2ea89-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2ea89-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ea89-154">NOTES</span></span>

## <span data-ttu-id="2ea89-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ea89-155">RELATED LINKS</span></span>
