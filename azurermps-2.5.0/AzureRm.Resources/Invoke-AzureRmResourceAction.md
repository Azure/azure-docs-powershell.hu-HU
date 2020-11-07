---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
ms.openlocfilehash: e29dda3fc5d2b62196d0cc5897ba7a7c9b047a8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849913"
---
# <span data-ttu-id="76492-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="76492-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="76492-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76492-102">SYNOPSIS</span></span>
<span data-ttu-id="76492-103">Egy erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="76492-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76492-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76492-104">SYNTAX</span></span>

### <span data-ttu-id="76492-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76492-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76492-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="76492-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76492-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="76492-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76492-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76492-108">DESCRIPTION</span></span>
<span data-ttu-id="76492-109">A **meghívó-AzureRmResourceAction** parancsmag egy megadott Azure-erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="76492-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="76492-110">A támogatott műveletek listáját az Azure Resource Explorer eszköz segítségével szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="76492-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="76492-111">Példák</span><span class="sxs-lookup"><span data-stu-id="76492-111">EXAMPLES</span></span>

## <span data-ttu-id="76492-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76492-112">PARAMETERS</span></span>

### <span data-ttu-id="76492-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="76492-113">-Action</span></span>
<span data-ttu-id="76492-114">Annak a tevékenységnek a nevét adja meg, amelyre hivatkozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="76492-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="76492-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76492-115">-ApiVersion</span></span>
<span data-ttu-id="76492-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76492-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="76492-117">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="76492-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="76492-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76492-118">-DefaultProfile</span></span>
<span data-ttu-id="76492-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76492-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76492-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="76492-120">-ExtensionResourceName</span></span>
<span data-ttu-id="76492-121">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="76492-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="76492-122">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="76492-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="76492-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="76492-123">-ExtensionResourceType</span></span>
<span data-ttu-id="76492-124">A bővítmény erőforrásának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76492-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="76492-125">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="76492-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="76492-126">-Force</span><span class="sxs-lookup"><span data-stu-id="76492-126">-Force</span></span>
<span data-ttu-id="76492-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="76492-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76492-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76492-128">-InformationAction</span></span>
<span data-ttu-id="76492-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="76492-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="76492-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76492-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76492-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="76492-131">Continue</span></span>
- <span data-ttu-id="76492-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="76492-132">Ignore</span></span>
- <span data-ttu-id="76492-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="76492-133">Inquire</span></span>
- <span data-ttu-id="76492-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76492-134">SilentlyContinue</span></span>
- <span data-ttu-id="76492-135">állj</span><span class="sxs-lookup"><span data-stu-id="76492-135">Stop</span></span>
- <span data-ttu-id="76492-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="76492-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76492-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76492-137">-InformationVariable</span></span>
<span data-ttu-id="76492-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="76492-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76492-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="76492-139">-ODataQuery</span></span>
<span data-ttu-id="76492-140">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="76492-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="76492-141">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="76492-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="76492-142">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="76492-142">-Parameters</span></span>
<span data-ttu-id="76492-143">A parancsmag által megjelenő műveletek esetében a paramétereket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="76492-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="76492-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="76492-144">-Pre</span></span>
<span data-ttu-id="76492-145">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="76492-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="76492-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76492-146">-ResourceGroupName</span></span>
<span data-ttu-id="76492-147">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="76492-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="76492-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76492-148">-ResourceId</span></span>
<span data-ttu-id="76492-149">Annak az erőforrásnak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="76492-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="76492-150">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="76492-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="76492-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="76492-151">-ResourceName</span></span>
<span data-ttu-id="76492-152">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="76492-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="76492-153">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="76492-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="76492-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="76492-154">-ResourceType</span></span>
<span data-ttu-id="76492-155">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76492-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="76492-156">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="76492-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="76492-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="76492-157">-TenantLevel</span></span>
<span data-ttu-id="76492-158">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="76492-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="76492-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76492-159">-Confirm</span></span>
<span data-ttu-id="76492-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76492-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76492-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76492-161">-WhatIf</span></span>
<span data-ttu-id="76492-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76492-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76492-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76492-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76492-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76492-164">CommonParameters</span></span>
<span data-ttu-id="76492-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76492-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76492-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76492-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76492-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76492-167">INPUTS</span></span>

## <span data-ttu-id="76492-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76492-168">OUTPUTS</span></span>

## <span data-ttu-id="76492-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76492-169">NOTES</span></span>

## <span data-ttu-id="76492-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76492-170">RELATED LINKS</span></span>
