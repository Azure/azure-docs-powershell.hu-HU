---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333989"
---
# <span data-ttu-id="679de-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="679de-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="679de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679de-102">SYNOPSIS</span></span>
<span data-ttu-id="679de-103">Törli a csatolt adatbázis-konfigurációt a megadott néven.</span><span class="sxs-lookup"><span data-stu-id="679de-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="679de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="679de-104">SYNTAX</span></span>

### <span data-ttu-id="679de-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="679de-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="679de-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="679de-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="679de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="679de-107">DESCRIPTION</span></span>
<span data-ttu-id="679de-108">Törli a csatolt adatbázis-konfigurációt a megadott néven.</span><span class="sxs-lookup"><span data-stu-id="679de-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="679de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="679de-109">EXAMPLES</span></span>

### <span data-ttu-id="679de-110">1. példa: Meglévő AttachedDatabaseConfiguration törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="679de-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="679de-111">A fenti parancs törli a AttachedDatabaseConfiguration "myfowerconfiguration" tulajdonságban definiált követési adatbázist a "testnewkustoclusterf" fürtből.</span><span class="sxs-lookup"><span data-stu-id="679de-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="679de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679de-112">PARAMETERS</span></span>

### <span data-ttu-id="679de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="679de-113">-AsJob</span></span>
<span data-ttu-id="679de-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="679de-114">Run the command as a job</span></span>

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

### <span data-ttu-id="679de-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="679de-115">-ClusterName</span></span>
<span data-ttu-id="679de-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="679de-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679de-117">-DefaultProfile</span></span>
<span data-ttu-id="679de-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="679de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679de-119">-InputObject</span></span>
<span data-ttu-id="679de-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="679de-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="679de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="679de-121">-Name</span></span>
<span data-ttu-id="679de-122">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="679de-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679de-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="679de-123">-NoWait</span></span>
<span data-ttu-id="679de-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="679de-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="679de-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="679de-125">-PassThru</span></span>
<span data-ttu-id="679de-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="679de-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="679de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679de-127">-ResourceGroupName</span></span>
<span data-ttu-id="679de-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="679de-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679de-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="679de-129">-SubscriptionId</span></span>
<span data-ttu-id="679de-130">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="679de-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="679de-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="679de-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679de-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679de-132">-Confirm</span></span>
<span data-ttu-id="679de-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="679de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679de-134">-WhatIf</span></span>
<span data-ttu-id="679de-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="679de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679de-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="679de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679de-137">CommonParameters</span></span>
<span data-ttu-id="679de-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679de-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="679de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679de-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679de-140">INPUTS</span></span>

### <span data-ttu-id="679de-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="679de-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="679de-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="679de-142">OUTPUTS</span></span>

### <span data-ttu-id="679de-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="679de-143">System.Boolean</span></span>

## <span data-ttu-id="679de-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="679de-144">NOTES</span></span>

<span data-ttu-id="679de-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="679de-145">ALIASES</span></span>

<span data-ttu-id="679de-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="679de-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="679de-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="679de-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="679de-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="679de-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="679de-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="679de-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="679de-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="679de-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="679de-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="679de-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="679de-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="679de-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="679de-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="679de-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="679de-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="679de-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="679de-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="679de-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="679de-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="679de-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="679de-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="679de-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="679de-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="679de-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="679de-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="679de-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="679de-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="679de-160">RELATED LINKS</span></span>

