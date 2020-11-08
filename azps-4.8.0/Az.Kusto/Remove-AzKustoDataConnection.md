---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018215"
---
# <span data-ttu-id="5137a-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="5137a-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="5137a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5137a-102">SYNOPSIS</span></span>
<span data-ttu-id="5137a-103">Törli az adatkapcsolatot a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="5137a-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="5137a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5137a-104">SYNTAX</span></span>

### <span data-ttu-id="5137a-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5137a-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5137a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5137a-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5137a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5137a-107">DESCRIPTION</span></span>
<span data-ttu-id="5137a-108">Törli az adatkapcsolatot a megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="5137a-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="5137a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5137a-109">EXAMPLES</span></span>

### <span data-ttu-id="5137a-110">1. példa: meglévő adatkapcsolat törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="5137a-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="5137a-111">A fenti parancs törli az "mykustodataconnection" nevű adatkapcsolatot az adatbázis "mykustodatabase" nevű "testnewkustocluster" nevű "" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5137a-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="5137a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5137a-112">PARAMETERS</span></span>

### <span data-ttu-id="5137a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5137a-113">-AsJob</span></span>
<span data-ttu-id="5137a-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5137a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5137a-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="5137a-115">-ClusterName</span></span>
<span data-ttu-id="5137a-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5137a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5137a-117">-DatabaseName</span></span>
<span data-ttu-id="5137a-118">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="5137a-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5137a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5137a-119">-DefaultProfile</span></span>
<span data-ttu-id="5137a-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5137a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5137a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5137a-121">-InputObject</span></span>
<span data-ttu-id="5137a-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5137a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5137a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5137a-123">-Name</span></span>
<span data-ttu-id="5137a-124">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-124">The name of the data connection.</span></span>

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

### <span data-ttu-id="5137a-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="5137a-125">-NoWait</span></span>
<span data-ttu-id="5137a-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5137a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5137a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5137a-127">-PassThru</span></span>
<span data-ttu-id="5137a-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="5137a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5137a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5137a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5137a-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5137a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5137a-131">-SubscriptionId</span></span>
<span data-ttu-id="5137a-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5137a-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5137a-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5137a-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5137a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5137a-134">-Confirm</span></span>
<span data-ttu-id="5137a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5137a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5137a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5137a-136">-WhatIf</span></span>
<span data-ttu-id="5137a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5137a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5137a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5137a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5137a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5137a-139">CommonParameters</span></span>
<span data-ttu-id="5137a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5137a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5137a-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5137a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5137a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5137a-142">INPUTS</span></span>

### <span data-ttu-id="5137a-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5137a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5137a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5137a-144">OUTPUTS</span></span>

### <span data-ttu-id="5137a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5137a-145">System.Boolean</span></span>

## <span data-ttu-id="5137a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5137a-146">NOTES</span></span>

<span data-ttu-id="5137a-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5137a-147">ALIASES</span></span>

<span data-ttu-id="5137a-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5137a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5137a-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5137a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5137a-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5137a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5137a-151">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5137a-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5137a-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5137a-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5137a-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5137a-155">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="5137a-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5137a-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5137a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5137a-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="5137a-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5137a-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5137a-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5137a-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5137a-160">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5137a-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5137a-161">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5137a-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5137a-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5137a-162">RELATED LINKS</span></span>

