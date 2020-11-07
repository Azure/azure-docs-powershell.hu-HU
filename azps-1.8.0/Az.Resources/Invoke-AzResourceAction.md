---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669409"
---
# <span data-ttu-id="7427f-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="7427f-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="7427f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7427f-102">SYNOPSIS</span></span>
<span data-ttu-id="7427f-103">Egy erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="7427f-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="7427f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7427f-104">SYNTAX</span></span>

### <span data-ttu-id="7427f-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7427f-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7427f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7427f-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7427f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7427f-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7427f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7427f-108">DESCRIPTION</span></span>
<span data-ttu-id="7427f-109">A **meghívó-AzResourceAction** parancsmag egy megadott Azure-erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="7427f-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="7427f-110">A támogatott műveletek listáját az Azure Resource Explorer eszköz segítségével szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="7427f-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="7427f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7427f-111">EXAMPLES</span></span>

## <span data-ttu-id="7427f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7427f-112">PARAMETERS</span></span>

### <span data-ttu-id="7427f-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="7427f-113">-Action</span></span>
<span data-ttu-id="7427f-114">Annak a tevékenységnek a nevét adja meg, amelyre hivatkozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="7427f-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7427f-115">-ApiVersion</span></span>
<span data-ttu-id="7427f-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7427f-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7427f-117">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7427f-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7427f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7427f-118">-DefaultProfile</span></span>
<span data-ttu-id="7427f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7427f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7427f-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7427f-120">-ExtensionResourceName</span></span>
<span data-ttu-id="7427f-121">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7427f-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7427f-122">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="7427f-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7427f-123">-ExtensionResourceType</span></span>
<span data-ttu-id="7427f-124">A bővítmény erőforrásának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7427f-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="7427f-125">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="7427f-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7427f-126">-Force</span></span>
<span data-ttu-id="7427f-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7427f-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7427f-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7427f-128">-ODataQuery</span></span>
<span data-ttu-id="7427f-129">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="7427f-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7427f-130">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="7427f-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7427f-131">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="7427f-131">-Parameters</span></span>
<span data-ttu-id="7427f-132">A parancsmag által megjelenő műveletek esetében a paramétereket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="7427f-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="7427f-133">-Pre</span></span>
<span data-ttu-id="7427f-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7427f-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7427f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7427f-135">-ResourceGroupName</span></span>
<span data-ttu-id="7427f-136">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7427f-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7427f-137">-ResourceId</span></span>
<span data-ttu-id="7427f-138">Annak az erőforrásnak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7427f-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7427f-139">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7427f-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7427f-140">-ResourceName</span></span>
<span data-ttu-id="7427f-141">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7427f-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7427f-142">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7427f-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7427f-143">-ResourceType</span></span>
<span data-ttu-id="7427f-144">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7427f-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="7427f-145">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="7427f-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7427f-146">-TenantLevel</span></span>
<span data-ttu-id="7427f-147">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="7427f-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7427f-148">-Confirm</span></span>
<span data-ttu-id="7427f-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7427f-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7427f-150">-WhatIf</span></span>
<span data-ttu-id="7427f-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7427f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7427f-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7427f-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7427f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7427f-153">CommonParameters</span></span>
<span data-ttu-id="7427f-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7427f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7427f-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7427f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7427f-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7427f-156">INPUTS</span></span>

### <span data-ttu-id="7427f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7427f-157">System.String</span></span>

## <span data-ttu-id="7427f-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7427f-158">OUTPUTS</span></span>

### <span data-ttu-id="7427f-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7427f-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7427f-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7427f-160">NOTES</span></span>

## <span data-ttu-id="7427f-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7427f-161">RELATED LINKS</span></span>
