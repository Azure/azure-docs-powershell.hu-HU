---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018214"
---
# <span data-ttu-id="e4242-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="e4242-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="e4242-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4242-102">SYNOPSIS</span></span>
<span data-ttu-id="e4242-103">A megadott nevű adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="e4242-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="e4242-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4242-104">SYNTAX</span></span>

### <span data-ttu-id="e4242-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4242-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e4242-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4242-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4242-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4242-107">DESCRIPTION</span></span>
<span data-ttu-id="e4242-108">A megadott nevű adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="e4242-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="e4242-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e4242-109">EXAMPLES</span></span>

### <span data-ttu-id="e4242-110">Példa 1: meglévő Kusto-adatbázis törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="e4242-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="e4242-111">A fenti parancs törli a "mykustodatabase" nevű Kusto-adatbázist a "testnewkustocluster" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e4242-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="e4242-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4242-112">PARAMETERS</span></span>

### <span data-ttu-id="e4242-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4242-113">-AsJob</span></span>
<span data-ttu-id="e4242-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e4242-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e4242-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e4242-115">-ClusterName</span></span>
<span data-ttu-id="e4242-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e4242-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4242-117">-DefaultProfile</span></span>
<span data-ttu-id="e4242-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4242-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4242-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4242-119">-InputObject</span></span>
<span data-ttu-id="e4242-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4242-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4242-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4242-121">-Name</span></span>
<span data-ttu-id="e4242-122">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="e4242-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4242-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="e4242-123">-NoWait</span></span>
<span data-ttu-id="e4242-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e4242-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4242-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4242-125">-PassThru</span></span>
<span data-ttu-id="e4242-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="e4242-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4242-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4242-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4242-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e4242-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4242-129">-SubscriptionId</span></span>
<span data-ttu-id="e4242-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e4242-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4242-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e4242-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4242-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4242-132">-Confirm</span></span>
<span data-ttu-id="e4242-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4242-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4242-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4242-134">-WhatIf</span></span>
<span data-ttu-id="e4242-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4242-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4242-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4242-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4242-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4242-137">CommonParameters</span></span>
<span data-ttu-id="e4242-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4242-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4242-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4242-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4242-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4242-140">INPUTS</span></span>

### <span data-ttu-id="e4242-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e4242-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e4242-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4242-142">OUTPUTS</span></span>

### <span data-ttu-id="e4242-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4242-143">System.Boolean</span></span>

## <span data-ttu-id="e4242-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4242-144">NOTES</span></span>

<span data-ttu-id="e4242-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e4242-145">ALIASES</span></span>

<span data-ttu-id="e4242-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e4242-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4242-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e4242-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4242-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e4242-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4242-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e4242-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4242-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e4242-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e4242-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e4242-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="e4242-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e4242-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e4242-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4242-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="e4242-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e4242-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e4242-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4242-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e4242-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e4242-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e4242-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e4242-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4242-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4242-160">RELATED LINKS</span></span>

