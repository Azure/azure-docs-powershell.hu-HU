---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678943"
---
# <span data-ttu-id="5563a-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="5563a-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="5563a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5563a-102">SYNOPSIS</span></span>
<span data-ttu-id="5563a-103">Egy erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="5563a-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5563a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5563a-104">SYNTAX</span></span>

### <span data-ttu-id="5563a-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5563a-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5563a-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5563a-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5563a-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5563a-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5563a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5563a-108">DESCRIPTION</span></span>
<span data-ttu-id="5563a-109">A **meghívó-AzureRmResourceAction** parancsmag egy megadott Azure-erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="5563a-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="5563a-110">A támogatott műveletek listáját az Azure Resource Explorer eszköz segítségével szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5563a-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="5563a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5563a-111">EXAMPLES</span></span>

## <span data-ttu-id="5563a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5563a-112">PARAMETERS</span></span>

### <span data-ttu-id="5563a-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="5563a-113">-Action</span></span>
<span data-ttu-id="5563a-114">Annak a tevékenységnek a nevét adja meg, amelyre hivatkozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="5563a-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5563a-115">-ApiVersion</span></span>
<span data-ttu-id="5563a-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5563a-117">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5563a-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5563a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5563a-118">-DefaultProfile</span></span>
<span data-ttu-id="5563a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5563a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5563a-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5563a-120">-ExtensionResourceName</span></span>
<span data-ttu-id="5563a-121">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5563a-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="5563a-122">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="5563a-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="5563a-123">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="5563a-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5563a-124">-ExtensionResourceType</span></span>
<span data-ttu-id="5563a-125">A bővítmény erőforrásának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="5563a-126">Például:</span><span class="sxs-lookup"><span data-stu-id="5563a-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5563a-127">-Force</span></span>
<span data-ttu-id="5563a-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5563a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5563a-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5563a-129">-InformationAction</span></span>
<span data-ttu-id="5563a-130">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5563a-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5563a-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5563a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5563a-132">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5563a-132">Continue</span></span>
- <span data-ttu-id="5563a-133">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5563a-133">Ignore</span></span>
- <span data-ttu-id="5563a-134">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5563a-134">Inquire</span></span>
- <span data-ttu-id="5563a-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5563a-135">SilentlyContinue</span></span>
- <span data-ttu-id="5563a-136">állj</span><span class="sxs-lookup"><span data-stu-id="5563a-136">Stop</span></span>
- <span data-ttu-id="5563a-137">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5563a-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5563a-138">-InformationVariable</span></span>
<span data-ttu-id="5563a-139">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5563a-140">-ODataQuery</span></span>
<span data-ttu-id="5563a-141">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="5563a-142">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="5563a-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5563a-143">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="5563a-143">-Parameters</span></span>
<span data-ttu-id="5563a-144">A parancsmag által megjelenő műveletek esetében a paramétereket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="5563a-145">-Pre</span></span>
<span data-ttu-id="5563a-146">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5563a-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5563a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5563a-147">-ResourceGroupName</span></span>
<span data-ttu-id="5563a-148">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5563a-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5563a-149">-ResourceId</span></span>
<span data-ttu-id="5563a-150">Annak az erőforrásnak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5563a-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="5563a-151">Az azonosító tartalmazza az előfizetést, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="5563a-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="5563a-152">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5563a-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5563a-153">-ResourceName</span></span>
<span data-ttu-id="5563a-154">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5563a-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="5563a-155">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="5563a-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5563a-156">-ResourceType</span></span>
<span data-ttu-id="5563a-157">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5563a-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="5563a-158">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="5563a-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5563a-159">-TenantLevel</span></span>
<span data-ttu-id="5563a-160">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="5563a-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5563a-161">-Confirm</span></span>
<span data-ttu-id="5563a-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5563a-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5563a-163">-WhatIf</span></span>
<span data-ttu-id="5563a-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5563a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5563a-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5563a-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5563a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5563a-166">CommonParameters</span></span>
<span data-ttu-id="5563a-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5563a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5563a-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5563a-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5563a-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5563a-169">INPUTS</span></span>

### <span data-ttu-id="5563a-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="5563a-170">None</span></span>
<span data-ttu-id="5563a-171">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5563a-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5563a-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5563a-172">OUTPUTS</span></span>

### <span data-ttu-id="5563a-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5563a-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5563a-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5563a-174">NOTES</span></span>

## <span data-ttu-id="5563a-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5563a-175">RELATED LINKS</span></span>
