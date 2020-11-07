---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ef81674d75ee2f5f79988875e70764df91d23d2c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "93851014"
---
# <span data-ttu-id="6da65-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6da65-101">Remove-AzResource</span></span>

## <span data-ttu-id="6da65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6da65-102">SYNOPSIS</span></span>
<span data-ttu-id="6da65-103">Eltávolít egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6da65-103">Removes a resource.</span></span>

## <span data-ttu-id="6da65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6da65-104">SYNTAX</span></span>

### <span data-ttu-id="6da65-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6da65-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da65-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6da65-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6da65-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6da65-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6da65-108">DESCRIPTION</span></span>
<span data-ttu-id="6da65-109">A **Remove-AzResource** parancsmag eltávolítja az Azure-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6da65-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="6da65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6da65-110">EXAMPLES</span></span>

### <span data-ttu-id="6da65-111">1. példa: webhely-erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6da65-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="6da65-112">Ez a parancs eltávolítja a ContosoSite nevű webhely-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6da65-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="6da65-113">A példa az előfizetés AZONOSÍTÓjának helyőrző értékét használja.</span><span class="sxs-lookup"><span data-stu-id="6da65-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="6da65-114">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6da65-115">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6da65-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6da65-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6da65-116">PARAMETERS</span></span>

### <span data-ttu-id="6da65-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6da65-117">-ApiVersion</span></span>
<span data-ttu-id="6da65-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6da65-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6da65-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6da65-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6da65-120">-AsJob</span></span>
<span data-ttu-id="6da65-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6da65-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6da65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da65-122">-DefaultProfile</span></span>
<span data-ttu-id="6da65-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6da65-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6da65-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6da65-124">-ExtensionResourceName</span></span>
<span data-ttu-id="6da65-125">A parancsmag által eltávolított erőforrás mellék-erőforrásának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6da65-126">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="6da65-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="6da65-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6da65-127">-ExtensionResourceType</span></span>
<span data-ttu-id="6da65-128">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6da65-129">Az erőforráshoz tartozó mellék-erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="6da65-130">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6da65-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6da65-131">-Force</span><span class="sxs-lookup"><span data-stu-id="6da65-131">-Force</span></span>
<span data-ttu-id="6da65-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6da65-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6da65-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6da65-133">-ODataQuery</span></span>
<span data-ttu-id="6da65-134">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6da65-135">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="6da65-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6da65-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="6da65-136">-Pre</span></span>
<span data-ttu-id="6da65-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6da65-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6da65-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da65-138">-ResourceGroupName</span></span>
<span data-ttu-id="6da65-139">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6da65-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="6da65-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6da65-140">-ResourceId</span></span>
<span data-ttu-id="6da65-141">A parancsmag által eltávolított erőforrás teljesen minősített erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6da65-142">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6da65-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6da65-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6da65-143">-ResourceName</span></span>
<span data-ttu-id="6da65-144">A parancsmag által eltávolított erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6da65-145">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6da65-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6da65-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6da65-146">-ResourceType</span></span>
<span data-ttu-id="6da65-147">A parancsmag által eltávolított erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6da65-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6da65-148">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6da65-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6da65-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6da65-149">-TenantLevel</span></span>
<span data-ttu-id="6da65-150">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="6da65-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6da65-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6da65-151">-Confirm</span></span>
<span data-ttu-id="6da65-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6da65-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da65-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da65-153">-WhatIf</span></span>
<span data-ttu-id="6da65-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6da65-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da65-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6da65-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da65-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da65-156">CommonParameters</span></span>
<span data-ttu-id="6da65-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6da65-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da65-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da65-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da65-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6da65-159">INPUTS</span></span>

### <span data-ttu-id="6da65-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6da65-160">System.String</span></span>

## <span data-ttu-id="6da65-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6da65-161">OUTPUTS</span></span>

### <span data-ttu-id="6da65-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6da65-162">System.Boolean</span></span>

## <span data-ttu-id="6da65-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6da65-163">NOTES</span></span>

## <span data-ttu-id="6da65-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6da65-164">RELATED LINKS</span></span>

[<span data-ttu-id="6da65-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6da65-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="6da65-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="6da65-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="6da65-167">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="6da65-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="6da65-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="6da65-168">Set-AzResource</span></span>](./Set-AzResource.md)


