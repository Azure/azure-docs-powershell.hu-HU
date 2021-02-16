---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 9cac9f92e61ac17ed825dd3e39991fc85c661d9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161539"
---
# <span data-ttu-id="7c8f6-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="7c8f6-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="7c8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8f6-103">Távolítsa el a KQL-lekérdezésekben futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7c8f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c8f6-104">SYNTAX</span></span>

### <span data-ttu-id="7c8f6-105">RemoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c8f6-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7c8f6-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7c8f6-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c8f6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c8f6-107">DESCRIPTION</span></span>
<span data-ttu-id="7c8f6-108">Távolítsa el a KQL-lekérdezésekben futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7c8f6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c8f6-109">EXAMPLES</span></span>

### <span data-ttu-id="7c8f6-110">1. példa: Nyelvbővítmények listájának eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="7c8f6-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="7c8f6-111">A fenti parancs eltávolítja a KQL-lekérdezésekben futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7c8f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c8f6-112">PARAMETERS</span></span>

### <span data-ttu-id="7c8f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c8f6-113">-AsJob</span></span>
<span data-ttu-id="7c8f6-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7c8f6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7c8f6-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7c8f6-115">-ClusterName</span></span>
<span data-ttu-id="7c8f6-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7c8f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8f6-117">-DefaultProfile</span></span>
<span data-ttu-id="7c8f6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c8f6-119">-InputObject</span></span>
<span data-ttu-id="7c8f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7c8f6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c8f6-121">-NoWait</span></span>
<span data-ttu-id="7c8f6-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7c8f6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c8f6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c8f6-123">-PassThru</span></span>
<span data-ttu-id="7c8f6-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="7c8f6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7c8f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c8f6-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7c8f6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c8f6-127">-SubscriptionId</span></span>
<span data-ttu-id="7c8f6-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c8f6-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7c8f6-130">-Érték</span><span class="sxs-lookup"><span data-stu-id="7c8f6-130">-Value</span></span>
<span data-ttu-id="7c8f6-131">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-131">The list of language extensions.</span></span>
<span data-ttu-id="7c8f6-132">Az ÉRTÉK tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c8f6-133">-Confirm</span></span>
<span data-ttu-id="7c8f6-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8f6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8f6-135">-WhatIf</span></span>
<span data-ttu-id="7c8f6-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8f6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8f6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8f6-138">CommonParameters</span></span>
<span data-ttu-id="7c8f6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8f6-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c8f6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8f6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c8f6-141">INPUTS</span></span>

### <span data-ttu-id="7c8f6-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7c8f6-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7c8f6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c8f6-143">OUTPUTS</span></span>

### <span data-ttu-id="7c8f6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c8f6-144">System.Boolean</span></span>

## <span data-ttu-id="7c8f6-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c8f6-145">NOTES</span></span>

<span data-ttu-id="7c8f6-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7c8f6-146">ALIASES</span></span>

<span data-ttu-id="7c8f6-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7c8f6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c8f6-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c8f6-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c8f6-150">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7c8f6-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c8f6-151">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7c8f6-152">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7c8f6-153">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7c8f6-154">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7c8f6-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7c8f6-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c8f6-156">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7c8f6-157">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7c8f6-158">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7c8f6-159">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7c8f6-160">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="7c8f6-161">VALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="7c8f6-162">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="7c8f6-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="7c8f6-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c8f6-163">RELATED LINKS</span></span>

