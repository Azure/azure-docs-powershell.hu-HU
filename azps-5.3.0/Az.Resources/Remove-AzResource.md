---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 31039d71f0c26b6fea3e19220b3932d2abd02073
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468565"
---
# <span data-ttu-id="facc6-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="facc6-101">Remove-AzResource</span></span>

## <span data-ttu-id="facc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="facc6-102">SYNOPSIS</span></span>
<span data-ttu-id="facc6-103">Eltávolít egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="facc6-103">Removes a resource.</span></span>

## <span data-ttu-id="facc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="facc6-104">SYNTAX</span></span>

### <span data-ttu-id="facc6-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="facc6-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="facc6-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="facc6-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="facc6-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="facc6-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="facc6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="facc6-108">DESCRIPTION</span></span>
<span data-ttu-id="facc6-109">A **Remove-AzResource** parancsmag eltávolít egy Azure-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="facc6-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="facc6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="facc6-110">EXAMPLES</span></span>

### <span data-ttu-id="facc6-111">1. példa: Webhelyerőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="facc6-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="facc6-112">Ez a parancs eltávolítja a ContosoSite nevű webhelyerőforrást.</span><span class="sxs-lookup"><span data-stu-id="facc6-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="facc6-113">A példa egy helyőrző értéket használ az előfizetésazonosítóhoz.</span><span class="sxs-lookup"><span data-stu-id="facc6-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="facc6-114">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="facc6-115">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="facc6-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="facc6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="facc6-116">PARAMETERS</span></span>

### <span data-ttu-id="facc6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="facc6-117">-ApiVersion</span></span>
<span data-ttu-id="facc6-118">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="facc6-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="facc6-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="facc6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="facc6-120">-AsJob</span></span>
<span data-ttu-id="facc6-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="facc6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="facc6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facc6-122">-DefaultProfile</span></span>
<span data-ttu-id="facc6-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="facc6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="facc6-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="facc6-124">-ExtensionResourceName</span></span>
<span data-ttu-id="facc6-125">Annak az erőforrásnak a nevét adja meg, amelyből a parancsmag eltávolítja a bővítményerőforrást.</span><span class="sxs-lookup"><span data-stu-id="facc6-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="facc6-126">Adatbázis megadásához például használja a következő formátumot: kiszolgálónév `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="facc6-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="facc6-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="facc6-127">-ExtensionResourceType</span></span>
<span data-ttu-id="facc6-128">Egy bővítményerőforrás erőforrástípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="facc6-129">Az erőforrás bővítményerőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="facc6-130">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="facc6-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="facc6-131">-Force</span><span class="sxs-lookup"><span data-stu-id="facc6-131">-Force</span></span>
<span data-ttu-id="facc6-132">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="facc6-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="facc6-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="facc6-133">-ODataQuery</span></span>
<span data-ttu-id="facc6-134">OData-stílusszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="facc6-135">Ez a parancsmag minden más szűrő mellett hozzáfűzi ezt az értéket a kérelemhez.</span><span class="sxs-lookup"><span data-stu-id="facc6-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="facc6-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="facc6-136">-Pre</span></span>
<span data-ttu-id="facc6-137">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="facc6-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="facc6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="facc6-138">-ResourceGroupName</span></span>
<span data-ttu-id="facc6-139">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="facc6-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="facc6-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="facc6-140">-ResourceId</span></span>
<span data-ttu-id="facc6-141">A parancsmag által eltávolított erőforrás teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="facc6-142">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában is: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="facc6-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="facc6-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="facc6-143">-ResourceName</span></span>
<span data-ttu-id="facc6-144">Annak az erőforrásnak a nevét adja meg, amelyből a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="facc6-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="facc6-145">Adatbázis megadásához például használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="facc6-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="facc6-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="facc6-146">-ResourceType</span></span>
<span data-ttu-id="facc6-147">A parancsmag által eltávolított erőforrás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="facc6-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="facc6-148">Adatbázis például az alábbi erőforrástípust követi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="facc6-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="facc6-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="facc6-149">-TenantLevel</span></span>
<span data-ttu-id="facc6-150">Azt jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="facc6-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="facc6-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="facc6-151">-Confirm</span></span>
<span data-ttu-id="facc6-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="facc6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="facc6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="facc6-153">-WhatIf</span></span>
<span data-ttu-id="facc6-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="facc6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="facc6-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="facc6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="facc6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facc6-156">CommonParameters</span></span>
<span data-ttu-id="facc6-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="facc6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facc6-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="facc6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facc6-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="facc6-159">INPUTS</span></span>

### <span data-ttu-id="facc6-160">System.String</span><span class="sxs-lookup"><span data-stu-id="facc6-160">System.String</span></span>

## <span data-ttu-id="facc6-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="facc6-161">OUTPUTS</span></span>

### <span data-ttu-id="facc6-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="facc6-162">System.Boolean</span></span>

## <span data-ttu-id="facc6-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="facc6-163">NOTES</span></span>

## <span data-ttu-id="facc6-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="facc6-164">RELATED LINKS</span></span>

[<span data-ttu-id="facc6-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="facc6-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="facc6-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="facc6-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="facc6-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="facc6-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="facc6-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="facc6-168">Set-AzResource</span></span>](./Set-AzResource.md)


