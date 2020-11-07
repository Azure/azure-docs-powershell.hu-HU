---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679831"
---
# <span data-ttu-id="e1963-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="e1963-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1963-102">SYNOPSIS</span></span>
<span data-ttu-id="e1963-103">Eltávolít egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e1963-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1963-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1963-104">SYNTAX</span></span>

### <span data-ttu-id="e1963-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1963-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1963-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e1963-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1963-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e1963-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1963-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1963-108">DESCRIPTION</span></span>
<span data-ttu-id="e1963-109">A **Remove-AzureRmResource** parancsmag eltávolítja az Azure-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e1963-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="e1963-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e1963-110">EXAMPLES</span></span>

### <span data-ttu-id="e1963-111">1. példa: webhely-erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e1963-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="e1963-112">Ez a parancs eltávolítja a ContosoSite nevű webhely-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e1963-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="e1963-113">A példa az előfizetés AZONOSÍTÓjának helyőrző értékét használja.</span><span class="sxs-lookup"><span data-stu-id="e1963-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="e1963-114">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e1963-115">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1963-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e1963-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1963-116">PARAMETERS</span></span>

### <span data-ttu-id="e1963-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1963-117">-ApiVersion</span></span>
<span data-ttu-id="e1963-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e1963-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e1963-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e1963-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1963-120">-AsJob</span></span>
<span data-ttu-id="e1963-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e1963-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1963-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1963-122">-DefaultProfile</span></span>
<span data-ttu-id="e1963-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e1963-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1963-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e1963-124">-ExtensionResourceName</span></span>
<span data-ttu-id="e1963-125">A parancsmag által eltávolított erőforrás mellék-erőforrásának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e1963-126">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="e1963-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e1963-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e1963-127">-ExtensionResourceType</span></span>
<span data-ttu-id="e1963-128">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e1963-129">Az erőforráshoz tartozó mellék-erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="e1963-130">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e1963-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e1963-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e1963-131">-Force</span></span>
<span data-ttu-id="e1963-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e1963-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1963-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e1963-133">-ODataQuery</span></span>
<span data-ttu-id="e1963-134">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e1963-135">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="e1963-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e1963-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1963-136">-Pre</span></span>
<span data-ttu-id="e1963-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e1963-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1963-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1963-138">-ResourceGroupName</span></span>
<span data-ttu-id="e1963-139">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e1963-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="e1963-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1963-140">-ResourceId</span></span>
<span data-ttu-id="e1963-141">A parancsmag által eltávolított erőforrás teljesen minősített erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e1963-142">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e1963-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e1963-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e1963-143">-ResourceName</span></span>
<span data-ttu-id="e1963-144">A parancsmag által eltávolított erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e1963-145">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e1963-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e1963-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e1963-146">-ResourceType</span></span>
<span data-ttu-id="e1963-147">A parancsmag által eltávolított erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1963-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e1963-148">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e1963-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e1963-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e1963-149">-TenantLevel</span></span>
<span data-ttu-id="e1963-150">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="e1963-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e1963-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1963-151">-Confirm</span></span>
<span data-ttu-id="e1963-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1963-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1963-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1963-153">-WhatIf</span></span>
<span data-ttu-id="e1963-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1963-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1963-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1963-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1963-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1963-156">CommonParameters</span></span>
<span data-ttu-id="e1963-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1963-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1963-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1963-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1963-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1963-159">INPUTS</span></span>

### <span data-ttu-id="e1963-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1963-160">None</span></span>

## <span data-ttu-id="e1963-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1963-161">OUTPUTS</span></span>

### <span data-ttu-id="e1963-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1963-162">System.Boolean</span></span>

## <span data-ttu-id="e1963-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1963-163">NOTES</span></span>

## <span data-ttu-id="e1963-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1963-164">RELATED LINKS</span></span>

[<span data-ttu-id="e1963-165">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="e1963-166">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="e1963-167">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e1963-168">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e1963-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e1963-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


