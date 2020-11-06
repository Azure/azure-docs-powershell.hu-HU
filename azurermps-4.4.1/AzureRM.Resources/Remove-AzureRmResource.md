---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500716"
---
# <span data-ttu-id="6cc12-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="6cc12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cc12-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc12-103">Eltávolít egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6cc12-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cc12-104">SYNTAX</span></span>

### <span data-ttu-id="6cc12-105">Az erőforrás azonosítója. (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cc12-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc12-106">Az előfizetési szinten található erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6cc12-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc12-107">A bérlői szinten lakóhellyel rendelkező erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6cc12-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc12-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cc12-108">DESCRIPTION</span></span>
<span data-ttu-id="6cc12-109">A **Remove-AzureRmResource** parancsmag eltávolítja az Azure-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6cc12-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="6cc12-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6cc12-110">EXAMPLES</span></span>

### <span data-ttu-id="6cc12-111">1. példa: webhely-erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6cc12-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="6cc12-112">Ez a parancs eltávolítja a ContosoSite nevű webhely-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6cc12-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="6cc12-113">A példa az előfizetés AZONOSÍTÓjának helyőrző értékét használja.</span><span class="sxs-lookup"><span data-stu-id="6cc12-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="6cc12-114">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6cc12-115">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cc12-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6cc12-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cc12-116">PARAMETERS</span></span>

### <span data-ttu-id="6cc12-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cc12-117">-ApiVersion</span></span>
<span data-ttu-id="6cc12-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cc12-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6cc12-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6cc12-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6cc12-120">-ExtensionResourceName</span></span>
<span data-ttu-id="6cc12-121">A parancsmag által eltávolított erőforrás mellék-erőforrásának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc12-122">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="6cc12-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="6cc12-123">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="6cc12-123">server name`/`database name</span></span>

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

### <span data-ttu-id="6cc12-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6cc12-124">-ExtensionResourceType</span></span>
<span data-ttu-id="6cc12-125">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6cc12-126">Az erőforráshoz tartozó mellék-erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="6cc12-127">Például:</span><span class="sxs-lookup"><span data-stu-id="6cc12-127">For instance:</span></span> 

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

### <span data-ttu-id="6cc12-128">-Force</span><span class="sxs-lookup"><span data-stu-id="6cc12-128">-Force</span></span>
<span data-ttu-id="6cc12-129">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6cc12-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cc12-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6cc12-130">-ODataQuery</span></span>
<span data-ttu-id="6cc12-131">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6cc12-132">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="6cc12-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6cc12-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cc12-133">-Pre</span></span>
<span data-ttu-id="6cc12-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6cc12-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6cc12-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc12-135">-ResourceGroupName</span></span>
<span data-ttu-id="6cc12-136">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6cc12-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="6cc12-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cc12-137">-ResourceId</span></span>
<span data-ttu-id="6cc12-138">A parancsmag által eltávolított erőforrás teljesen minősített erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc12-139">Az azonosító tartalmazza az előfizetést, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="6cc12-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="6cc12-140">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6cc12-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6cc12-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6cc12-141">-ResourceName</span></span>
<span data-ttu-id="6cc12-142">A parancsmag által eltávolított erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc12-143">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="6cc12-143">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="6cc12-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6cc12-144">-ResourceType</span></span>
<span data-ttu-id="6cc12-145">A parancsmag által eltávolított erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc12-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc12-146">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="6cc12-146">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="6cc12-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6cc12-147">-TenantLevel</span></span>
<span data-ttu-id="6cc12-148">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="6cc12-148">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6cc12-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cc12-149">-Confirm</span></span>
<span data-ttu-id="6cc12-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cc12-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc12-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc12-151">-WhatIf</span></span>
<span data-ttu-id="6cc12-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cc12-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc12-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cc12-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc12-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc12-154">-DefaultProfile</span></span>
<span data-ttu-id="6cc12-155">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cc12-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc12-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc12-156">CommonParameters</span></span>
<span data-ttu-id="6cc12-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cc12-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc12-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc12-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc12-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc12-159">INPUTS</span></span>

## <span data-ttu-id="6cc12-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc12-160">OUTPUTS</span></span>

### <span data-ttu-id="6cc12-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cc12-161">System.Boolean</span></span>

## <span data-ttu-id="6cc12-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cc12-162">NOTES</span></span>

## <span data-ttu-id="6cc12-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cc12-163">RELATED LINKS</span></span>

[<span data-ttu-id="6cc12-164">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="6cc12-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="6cc12-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="6cc12-167">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="6cc12-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc12-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


