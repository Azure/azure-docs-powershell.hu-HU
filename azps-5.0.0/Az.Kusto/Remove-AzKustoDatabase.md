---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194686"
---
# <span data-ttu-id="cef86-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="cef86-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="cef86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cef86-102">SYNOPSIS</span></span>
<span data-ttu-id="cef86-103">A megadott nevű adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="cef86-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="cef86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cef86-104">SYNTAX</span></span>

### <span data-ttu-id="cef86-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cef86-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cef86-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cef86-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cef86-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cef86-107">DESCRIPTION</span></span>
<span data-ttu-id="cef86-108">A megadott nevű adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="cef86-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="cef86-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cef86-109">EXAMPLES</span></span>

### <span data-ttu-id="cef86-110">Példa 1: meglévő Kusto-adatbázis törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="cef86-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="cef86-111">A fenti parancs törli a "mykustodatabase" nevű Kusto-adatbázist a "testnewkustocluster" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="cef86-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="cef86-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cef86-112">PARAMETERS</span></span>

### <span data-ttu-id="cef86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cef86-113">-AsJob</span></span>
<span data-ttu-id="cef86-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="cef86-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cef86-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="cef86-115">-ClusterName</span></span>
<span data-ttu-id="cef86-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cef86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef86-117">-DefaultProfile</span></span>
<span data-ttu-id="cef86-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cef86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef86-119">-InputObject</span></span>
<span data-ttu-id="cef86-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cef86-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cef86-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cef86-121">-Name</span></span>
<span data-ttu-id="cef86-122">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="cef86-122">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cef86-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="cef86-123">-NoWait</span></span>
<span data-ttu-id="cef86-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="cef86-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cef86-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cef86-125">-PassThru</span></span>
<span data-ttu-id="cef86-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="cef86-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cef86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef86-127">-ResourceGroupName</span></span>
<span data-ttu-id="cef86-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cef86-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cef86-129">-SubscriptionId</span></span>
<span data-ttu-id="cef86-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cef86-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cef86-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="cef86-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cef86-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cef86-132">-Confirm</span></span>
<span data-ttu-id="cef86-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cef86-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef86-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef86-134">-WhatIf</span></span>
<span data-ttu-id="cef86-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cef86-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef86-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cef86-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef86-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef86-137">CommonParameters</span></span>
<span data-ttu-id="cef86-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cef86-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef86-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cef86-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef86-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef86-140">INPUTS</span></span>

### <span data-ttu-id="cef86-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cef86-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cef86-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef86-142">OUTPUTS</span></span>

### <span data-ttu-id="cef86-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cef86-143">System.Boolean</span></span>

## <span data-ttu-id="cef86-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cef86-144">NOTES</span></span>

<span data-ttu-id="cef86-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cef86-145">ALIASES</span></span>

<span data-ttu-id="cef86-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="cef86-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cef86-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="cef86-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cef86-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="cef86-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cef86-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="cef86-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cef86-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cef86-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cef86-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cef86-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="cef86-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cef86-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cef86-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cef86-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="cef86-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cef86-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cef86-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cef86-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cef86-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cef86-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cef86-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="cef86-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cef86-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cef86-160">RELATED LINKS</span></span>

