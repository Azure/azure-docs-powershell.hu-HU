---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672197"
---
# <span data-ttu-id="b51e3-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="b51e3-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="b51e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b51e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b51e3-103">Egy erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="b51e3-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b51e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b51e3-104">SYNTAX</span></span>

### <span data-ttu-id="b51e3-105">Az erőforrás azonosítója. (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b51e3-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b51e3-106">Az előfizetési szinten található erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b51e3-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b51e3-107">A bérlői szinten lakóhellyel rendelkező erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b51e3-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b51e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b51e3-108">DESCRIPTION</span></span>
<span data-ttu-id="b51e3-109">A **meghívó-AzureRmResourceAction** parancsmag egy megadott Azure-erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="b51e3-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="b51e3-110">A támogatott műveletek listáját az Azure Resource Explorer eszköz segítségével szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="b51e3-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="b51e3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b51e3-111">EXAMPLES</span></span>

## <span data-ttu-id="b51e3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b51e3-112">PARAMETERS</span></span>

### <span data-ttu-id="b51e3-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="b51e3-113">-Action</span></span>
<span data-ttu-id="b51e3-114">Annak a tevékenységnek a nevét adja meg, amelyre hivatkozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="b51e3-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="b51e3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b51e3-115">-ApiVersion</span></span>
<span data-ttu-id="b51e3-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b51e3-117">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b51e3-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b51e3-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b51e3-118">-ExtensionResourceName</span></span>
<span data-ttu-id="b51e3-119">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b51e3-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b51e3-120">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="b51e3-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="b51e3-121">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="b51e3-121">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b51e3-122">-ExtensionResourceType</span></span>
<span data-ttu-id="b51e3-123">A bővítmény erőforrásának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="b51e3-124">Például:</span><span class="sxs-lookup"><span data-stu-id="b51e3-124">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b51e3-125">-Force</span></span>
<span data-ttu-id="b51e3-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b51e3-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b51e3-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b51e3-127">-InformationAction</span></span>
<span data-ttu-id="b51e3-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b51e3-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b51e3-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b51e3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b51e3-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b51e3-130">Continue</span></span>
- <span data-ttu-id="b51e3-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b51e3-131">Ignore</span></span>
- <span data-ttu-id="b51e3-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b51e3-132">Inquire</span></span>
- <span data-ttu-id="b51e3-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b51e3-133">SilentlyContinue</span></span>
- <span data-ttu-id="b51e3-134">állj</span><span class="sxs-lookup"><span data-stu-id="b51e3-134">Stop</span></span>
- <span data-ttu-id="b51e3-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b51e3-135">Suspend</span></span>

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

### <span data-ttu-id="b51e3-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b51e3-136">-InformationVariable</span></span>
<span data-ttu-id="b51e3-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b51e3-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b51e3-138">-ODataQuery</span></span>
<span data-ttu-id="b51e3-139">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b51e3-140">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="b51e3-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b51e3-141">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="b51e3-141">-Parameters</span></span>
<span data-ttu-id="b51e3-142">A parancsmag által megjelenő műveletek esetében a paramétereket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="b51e3-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="b51e3-143">-Pre</span></span>
<span data-ttu-id="b51e3-144">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b51e3-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b51e3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51e3-145">-ResourceGroupName</span></span>
<span data-ttu-id="b51e3-146">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b51e3-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b51e3-147">-ResourceId</span></span>
<span data-ttu-id="b51e3-148">Annak az erőforrásnak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b51e3-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b51e3-149">Az azonosító tartalmazza az előfizetést, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="b51e3-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="b51e3-150">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b51e3-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b51e3-151">-ResourceName</span></span>
<span data-ttu-id="b51e3-152">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b51e3-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b51e3-153">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="b51e3-153">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b51e3-154">-ResourceType</span></span>
<span data-ttu-id="b51e3-155">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51e3-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="b51e3-156">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="b51e3-156">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b51e3-157">-TenantLevel</span></span>
<span data-ttu-id="b51e3-158">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="b51e3-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b51e3-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b51e3-159">-Confirm</span></span>
<span data-ttu-id="b51e3-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b51e3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b51e3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b51e3-161">-WhatIf</span></span>
<span data-ttu-id="b51e3-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b51e3-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b51e3-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b51e3-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b51e3-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51e3-164">-DefaultProfile</span></span>
<span data-ttu-id="b51e3-165">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b51e3-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b51e3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51e3-166">CommonParameters</span></span>
<span data-ttu-id="b51e3-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b51e3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51e3-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b51e3-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51e3-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51e3-169">INPUTS</span></span>

## <span data-ttu-id="b51e3-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51e3-170">OUTPUTS</span></span>

### <span data-ttu-id="b51e3-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b51e3-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b51e3-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b51e3-172">NOTES</span></span>

## <span data-ttu-id="b51e3-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b51e3-173">RELATED LINKS</span></span>

