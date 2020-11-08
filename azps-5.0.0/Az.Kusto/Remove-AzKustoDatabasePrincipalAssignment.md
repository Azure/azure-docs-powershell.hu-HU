---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194683"
---
# <span data-ttu-id="f5a08-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f5a08-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f5a08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5a08-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a08-103">Törli a Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f5a08-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f5a08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5a08-104">SYNTAX</span></span>

### <span data-ttu-id="f5a08-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5a08-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5a08-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5a08-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5a08-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5a08-107">DESCRIPTION</span></span>
<span data-ttu-id="f5a08-108">Törli a Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f5a08-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f5a08-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5a08-109">EXAMPLES</span></span>

### <span data-ttu-id="f5a08-110">Példa 1: meglévő Kusto-adatbázis törlése PrincipalAssignment néven</span><span class="sxs-lookup"><span data-stu-id="f5a08-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="f5a08-111">A fenti parancs törli a "kustoprincipal1" nevű PrincipalAssignment a Kusto-adatbázisban "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="f5a08-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="f5a08-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5a08-112">PARAMETERS</span></span>

### <span data-ttu-id="f5a08-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5a08-113">-AsJob</span></span>
<span data-ttu-id="f5a08-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="f5a08-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f5a08-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="f5a08-115">-ClusterName</span></span>
<span data-ttu-id="f5a08-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f5a08-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5a08-117">-DatabaseName</span></span>
<span data-ttu-id="f5a08-118">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f5a08-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f5a08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a08-119">-DefaultProfile</span></span>
<span data-ttu-id="f5a08-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5a08-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a08-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5a08-121">-InputObject</span></span>
<span data-ttu-id="f5a08-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5a08-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5a08-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="f5a08-123">-NoWait</span></span>
<span data-ttu-id="f5a08-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="f5a08-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f5a08-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5a08-125">-PassThru</span></span>
<span data-ttu-id="f5a08-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f5a08-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f5a08-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f5a08-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f5a08-128">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f5a08-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a08-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5a08-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f5a08-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5a08-131">-SubscriptionId</span></span>
<span data-ttu-id="f5a08-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5a08-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f5a08-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f5a08-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f5a08-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5a08-134">-Confirm</span></span>
<span data-ttu-id="f5a08-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5a08-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a08-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a08-136">-WhatIf</span></span>
<span data-ttu-id="f5a08-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5a08-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a08-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5a08-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a08-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a08-139">CommonParameters</span></span>
<span data-ttu-id="f5a08-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5a08-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a08-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5a08-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a08-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5a08-142">INPUTS</span></span>

### <span data-ttu-id="f5a08-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f5a08-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f5a08-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5a08-144">OUTPUTS</span></span>

### <span data-ttu-id="f5a08-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5a08-145">System.Boolean</span></span>

## <span data-ttu-id="f5a08-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5a08-146">NOTES</span></span>

<span data-ttu-id="f5a08-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f5a08-147">ALIASES</span></span>

<span data-ttu-id="f5a08-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f5a08-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5a08-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f5a08-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5a08-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f5a08-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5a08-151">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f5a08-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5a08-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f5a08-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f5a08-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f5a08-155">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f5a08-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f5a08-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f5a08-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5a08-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="f5a08-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f5a08-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f5a08-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5a08-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f5a08-160">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5a08-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f5a08-161">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f5a08-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f5a08-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5a08-162">RELATED LINKS</span></span>

