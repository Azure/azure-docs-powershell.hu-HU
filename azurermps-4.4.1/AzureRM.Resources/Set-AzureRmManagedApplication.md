---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494696"
---
# <span data-ttu-id="fb8ba-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="fb8ba-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="fb8ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8ba-103">A felügyelt alkalmazások frissítése</span><span class="sxs-lookup"><span data-stu-id="fb8ba-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb8ba-104">SYNTAX</span></span>

### <span data-ttu-id="fb8ba-105">A felügyelt alkalmazásnév paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-105">The managed application name parameter set.</span></span> <span data-ttu-id="fb8ba-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fb8ba-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8ba-107">A felügyelt alkalmazásspecifikus azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb8ba-108">DESCRIPTION</span></span>
<span data-ttu-id="fb8ba-109">A **set-AzureRmManagedApplication** parancsmag frissíti a felügyelt alkalmazásokat</span><span class="sxs-lookup"><span data-stu-id="fb8ba-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="fb8ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb8ba-110">EXAMPLES</span></span>

### <span data-ttu-id="fb8ba-111">1. példa: a felügyelt alkalmazás definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="fb8ba-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="fb8ba-112">Ez a parancs frissíti a felügyelt alkalmazás leírását.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-112">This command updates the managed application description</span></span>

## <span data-ttu-id="fb8ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb8ba-113">PARAMETERS</span></span>

### <span data-ttu-id="fb8ba-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb8ba-114">-ApiVersion</span></span>
<span data-ttu-id="fb8ba-115">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb8ba-116">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fb8ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8ba-117">-DefaultProfile</span></span>
<span data-ttu-id="fb8ba-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8ba-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="fb8ba-119">-Kind</span></span>
<span data-ttu-id="fb8ba-120">A felügyelt alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-120">The managed application kind.</span></span>
<span data-ttu-id="fb8ba-121">A piactér vagy a servicecatalog egyike</span><span class="sxs-lookup"><span data-stu-id="fb8ba-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="fb8ba-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fb8ba-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="fb8ba-123">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="fb8ba-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8ba-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fb8ba-125">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="fb8ba-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb8ba-126">-Name</span></span>
<span data-ttu-id="fb8ba-127">A felügyelt alkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8ba-128">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="fb8ba-128">-Parameter</span></span>
<span data-ttu-id="fb8ba-129">A felügyelt alkalmazás paramétereinek formázott karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="fb8ba-130">Ez lehet az elérési út a paramétereket tartalmazó fájlnév vagy URI-azonosítók, illetve a paraméterek karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="fb8ba-131">-Terv</span><span class="sxs-lookup"><span data-stu-id="fb8ba-131">-Plan</span></span>
<span data-ttu-id="fb8ba-132">Egy kivonatoló táblázat, amely A felügyelt alkalmazási terv tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-132">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8ba-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb8ba-133">-Pre</span></span>
<span data-ttu-id="fb8ba-134">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb8ba-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8ba-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb8ba-136">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8ba-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="fb8ba-137">-Tag</span></span>
<span data-ttu-id="fb8ba-138">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="fb8ba-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb8ba-139">-Confirm</span></span>
<span data-ttu-id="fb8ba-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8ba-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8ba-141">-WhatIf</span></span>
<span data-ttu-id="fb8ba-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8ba-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb8ba-144">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fb8ba-144">-Id</span></span>
<span data-ttu-id="fb8ba-145">A teljes mértékben minősített felügyelt alkalmazásspecifikus azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="fb8ba-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="fb8ba-146">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fb8ba-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8ba-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8ba-147">CommonParameters</span></span>
<span data-ttu-id="fb8ba-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb8ba-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8ba-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8ba-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8ba-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb8ba-150">INPUTS</span></span>

### <span data-ttu-id="fb8ba-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fb8ba-151">System.String</span></span>
<span data-ttu-id="fb8ba-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb8ba-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb8ba-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb8ba-153">OUTPUTS</span></span>

### <span data-ttu-id="fb8ba-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fb8ba-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fb8ba-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb8ba-155">NOTES</span></span>

## <span data-ttu-id="fb8ba-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb8ba-156">RELATED LINKS</span></span>

