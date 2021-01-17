---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 12e43eeb22151df8569e068933036fe29749ed1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476930"
---
# <span data-ttu-id="86a63-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="86a63-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="86a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86a63-102">SYNOPSIS</span></span>
<span data-ttu-id="86a63-103">Távolítsa el az adatbázis-igazgatók engedélyét.</span><span class="sxs-lookup"><span data-stu-id="86a63-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="86a63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86a63-104">SYNTAX</span></span>

### <span data-ttu-id="86a63-105">RemoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86a63-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="86a63-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="86a63-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86a63-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86a63-107">DESCRIPTION</span></span>
<span data-ttu-id="86a63-108">Távolítsa el az adatbázis-igazgatók engedélyét.</span><span class="sxs-lookup"><span data-stu-id="86a63-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="86a63-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86a63-109">EXAMPLES</span></span>

### <span data-ttu-id="86a63-110">1. példa: Az adatbázis-kezelők engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86a63-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="86a63-111">A fenti parancs eltávolítja az adatbázis-igazgatók engedélyét.</span><span class="sxs-lookup"><span data-stu-id="86a63-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="86a63-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86a63-112">PARAMETERS</span></span>

### <span data-ttu-id="86a63-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="86a63-113">-ClusterName</span></span>
<span data-ttu-id="86a63-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86a63-115">-DatabaseName</span></span>
<span data-ttu-id="86a63-116">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a63-117">-DefaultProfile</span></span>
<span data-ttu-id="86a63-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86a63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86a63-119">-InputObject</span></span>
<span data-ttu-id="86a63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="86a63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a63-121">-ResourceGroupName</span></span>
<span data-ttu-id="86a63-122">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86a63-123">-SubscriptionId</span></span>
<span data-ttu-id="86a63-124">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="86a63-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="86a63-125">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="86a63-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-126">-Érték</span><span class="sxs-lookup"><span data-stu-id="86a63-126">-Value</span></span>
<span data-ttu-id="86a63-127">A Kusto-adatbázis-principalsok listája.</span><span class="sxs-lookup"><span data-stu-id="86a63-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="86a63-128">Az ÉRTÉK tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="86a63-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86a63-129">-Confirm</span></span>
<span data-ttu-id="86a63-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86a63-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86a63-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a63-131">-WhatIf</span></span>
<span data-ttu-id="86a63-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86a63-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86a63-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86a63-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86a63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a63-134">CommonParameters</span></span>
<span data-ttu-id="86a63-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a63-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86a63-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a63-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86a63-137">INPUTS</span></span>

### <span data-ttu-id="86a63-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="86a63-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="86a63-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86a63-139">OUTPUTS</span></span>

### <span data-ttu-id="86a63-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="86a63-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="86a63-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86a63-141">NOTES</span></span>

<span data-ttu-id="86a63-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="86a63-142">ALIASES</span></span>

<span data-ttu-id="86a63-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="86a63-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86a63-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="86a63-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86a63-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86a63-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86a63-146">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="86a63-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86a63-147">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="86a63-148">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="86a63-149">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="86a63-150">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="86a63-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="86a63-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86a63-152">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="86a63-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="86a63-153">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="86a63-154">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="86a63-155">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="86a63-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="86a63-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="86a63-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="86a63-157">VALUE <IDatabasePrincipal[]>: A Kusto-adatbázis-principalok listája.</span><span class="sxs-lookup"><span data-stu-id="86a63-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="86a63-158">`Name <String>`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="86a63-159">`Role <DatabasePrincipalRole>`: Az adatbázis elsődleges szerepköre.</span><span class="sxs-lookup"><span data-stu-id="86a63-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="86a63-160">`Type <DatabasePrincipalType>`: Az adatbázis-kezelő egyszerű típusa.</span><span class="sxs-lookup"><span data-stu-id="86a63-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="86a63-161">`[AppId <String>]`: Alkalmazásazonosító – csak az alkalmazásnév típusa esetén releváns.</span><span class="sxs-lookup"><span data-stu-id="86a63-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="86a63-162">`[Email <String>]`: Egyszerű adatbázis-e-mail,ha létezik.</span><span class="sxs-lookup"><span data-stu-id="86a63-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="86a63-163">`[Fqn <String>]`: Az egyszerű adatbázisnév teljesen minősített neve.</span><span class="sxs-lookup"><span data-stu-id="86a63-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="86a63-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86a63-164">RELATED LINKS</span></span>

