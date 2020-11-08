---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194688"
---
# <span data-ttu-id="956eb-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="956eb-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="956eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="956eb-102">SYNOPSIS</span></span>
<span data-ttu-id="956eb-103">Törli az adatkapcsolatot a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="956eb-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="956eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="956eb-104">SYNTAX</span></span>

### <span data-ttu-id="956eb-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="956eb-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="956eb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="956eb-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="956eb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="956eb-107">DESCRIPTION</span></span>
<span data-ttu-id="956eb-108">Törli az adatkapcsolatot a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="956eb-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="956eb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="956eb-109">EXAMPLES</span></span>

### <span data-ttu-id="956eb-110">1. példa: meglévő adatkapcsolat törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="956eb-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="956eb-111">A fenti parancs törli az "mykustodataconnection" nevű adatkapcsolatot az adatbázis "mykustodatabase" nevű "testnewkustocluster" nevű "" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="956eb-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="956eb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="956eb-112">PARAMETERS</span></span>

### <span data-ttu-id="956eb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="956eb-113">-AsJob</span></span>
<span data-ttu-id="956eb-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="956eb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="956eb-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="956eb-115">-ClusterName</span></span>
<span data-ttu-id="956eb-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="956eb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="956eb-117">-DatabaseName</span></span>
<span data-ttu-id="956eb-118">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="956eb-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="956eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956eb-119">-DefaultProfile</span></span>
<span data-ttu-id="956eb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="956eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="956eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="956eb-121">-InputObject</span></span>
<span data-ttu-id="956eb-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="956eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="956eb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="956eb-123">-Name</span></span>
<span data-ttu-id="956eb-124">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956eb-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="956eb-125">-NoWait</span></span>
<span data-ttu-id="956eb-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="956eb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="956eb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="956eb-127">-PassThru</span></span>
<span data-ttu-id="956eb-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="956eb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="956eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="956eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="956eb-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="956eb-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="956eb-131">-SubscriptionId</span></span>
<span data-ttu-id="956eb-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="956eb-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="956eb-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="956eb-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="956eb-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="956eb-134">-Confirm</span></span>
<span data-ttu-id="956eb-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="956eb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956eb-136">-WhatIf</span></span>
<span data-ttu-id="956eb-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="956eb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956eb-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="956eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956eb-139">CommonParameters</span></span>
<span data-ttu-id="956eb-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="956eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956eb-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="956eb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956eb-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="956eb-142">INPUTS</span></span>

### <span data-ttu-id="956eb-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="956eb-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="956eb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="956eb-144">OUTPUTS</span></span>

### <span data-ttu-id="956eb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="956eb-145">System.Boolean</span></span>

## <span data-ttu-id="956eb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="956eb-146">NOTES</span></span>

<span data-ttu-id="956eb-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="956eb-147">ALIASES</span></span>

<span data-ttu-id="956eb-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="956eb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="956eb-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="956eb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="956eb-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="956eb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="956eb-151">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="956eb-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="956eb-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="956eb-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="956eb-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="956eb-155">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="956eb-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="956eb-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="956eb-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="956eb-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="956eb-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="956eb-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="956eb-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="956eb-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="956eb-160">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="956eb-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="956eb-161">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="956eb-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="956eb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="956eb-162">RELATED LINKS</span></span>

