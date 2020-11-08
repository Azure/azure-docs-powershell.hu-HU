---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184679"
---
# <span data-ttu-id="177f7-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="177f7-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="177f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="177f7-102">SYNOPSIS</span></span>
<span data-ttu-id="177f7-103">Egy erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="177f7-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="177f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="177f7-104">SYNTAX</span></span>

### <span data-ttu-id="177f7-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="177f7-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="177f7-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="177f7-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177f7-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="177f7-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="177f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="177f7-108">DESCRIPTION</span></span>
<span data-ttu-id="177f7-109">A **meghívó-AzResourceAction** parancsmag egy megadott Azure-erőforrás műveletét hívja fel.</span><span class="sxs-lookup"><span data-stu-id="177f7-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="177f7-110">A támogatott műveletek listáját az Azure Resource Explorer eszköz segítségével szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="177f7-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="177f7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="177f7-111">EXAMPLES</span></span>

### <span data-ttu-id="177f7-112">1. példa: a VM indítása a ResourceId</span><span class="sxs-lookup"><span data-stu-id="177f7-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="177f7-113">A következő parancs elindítja a virtuális gépet: {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="177f7-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="177f7-114">2. példa: a VM kiváltása a ResourceName</span><span class="sxs-lookup"><span data-stu-id="177f7-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="177f7-115">Ez a parancs az {ResourceId} végződésű virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="177f7-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="177f7-116">A parancs az *erő* paramétert adja meg, ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="177f7-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="177f7-117">3. példa: egy erőforrás-szolgáltató regisztrációjának meghívása a ResourceId-val</span><span class="sxs-lookup"><span data-stu-id="177f7-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="177f7-118">Ez a parancs egy erőforrás-szolgáltatót regisztrál a Microsoft. hálózatban.</span><span class="sxs-lookup"><span data-stu-id="177f7-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="177f7-119">A parancs az *erő* paramétert adja meg, ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="177f7-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="177f7-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="177f7-120">PARAMETERS</span></span>

### <span data-ttu-id="177f7-121">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="177f7-121">-Action</span></span>
<span data-ttu-id="177f7-122">Annak a tevékenységnek a nevét adja meg, amelyre hivatkozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="177f7-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="177f7-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="177f7-123">-ApiVersion</span></span>
<span data-ttu-id="177f7-124">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="177f7-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="177f7-125">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="177f7-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="177f7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177f7-126">-DefaultProfile</span></span>
<span data-ttu-id="177f7-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="177f7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="177f7-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="177f7-128">-ExtensionResourceName</span></span>
<span data-ttu-id="177f7-129">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="177f7-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="177f7-130">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="177f7-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="177f7-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="177f7-131">-ExtensionResourceType</span></span>
<span data-ttu-id="177f7-132">A bővítmény erőforrásának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="177f7-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="177f7-133">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="177f7-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="177f7-134">-Force</span><span class="sxs-lookup"><span data-stu-id="177f7-134">-Force</span></span>
<span data-ttu-id="177f7-135">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="177f7-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="177f7-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="177f7-136">-ODataQuery</span></span>
<span data-ttu-id="177f7-137">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="177f7-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="177f7-138">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="177f7-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="177f7-139">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="177f7-139">-Parameters</span></span>
<span data-ttu-id="177f7-140">A parancsmag által megjelenő műveletek esetében a paramétereket a hash-táblázatként adja meg.</span><span class="sxs-lookup"><span data-stu-id="177f7-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="177f7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="177f7-141">-Pre</span></span>
<span data-ttu-id="177f7-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="177f7-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="177f7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177f7-143">-ResourceGroupName</span></span>
<span data-ttu-id="177f7-144">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="177f7-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="177f7-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="177f7-145">-ResourceId</span></span>
<span data-ttu-id="177f7-146">Annak az erőforrásnak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="177f7-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="177f7-147">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="177f7-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="177f7-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="177f7-148">-ResourceName</span></span>
<span data-ttu-id="177f7-149">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag egy műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="177f7-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="177f7-150">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="177f7-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="177f7-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="177f7-151">-ResourceType</span></span>
<span data-ttu-id="177f7-152">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="177f7-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="177f7-153">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="177f7-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="177f7-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="177f7-154">-TenantLevel</span></span>
<span data-ttu-id="177f7-155">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="177f7-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="177f7-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="177f7-156">-Confirm</span></span>
<span data-ttu-id="177f7-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="177f7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177f7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177f7-158">-WhatIf</span></span>
<span data-ttu-id="177f7-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="177f7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177f7-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="177f7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177f7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177f7-161">CommonParameters</span></span>
<span data-ttu-id="177f7-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="177f7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177f7-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="177f7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177f7-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="177f7-164">INPUTS</span></span>

### <span data-ttu-id="177f7-165">System. String</span><span class="sxs-lookup"><span data-stu-id="177f7-165">System.String</span></span>

## <span data-ttu-id="177f7-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="177f7-166">OUTPUTS</span></span>

### <span data-ttu-id="177f7-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="177f7-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="177f7-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="177f7-168">NOTES</span></span>

## <span data-ttu-id="177f7-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="177f7-169">RELATED LINKS</span></span>
