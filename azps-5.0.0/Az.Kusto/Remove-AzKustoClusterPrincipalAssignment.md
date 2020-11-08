---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194691"
---
# <span data-ttu-id="b8147-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b8147-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b8147-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8147-102">SYNOPSIS</span></span>
<span data-ttu-id="b8147-103">Törli a Kusto-fürtös principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b8147-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b8147-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8147-104">SYNTAX</span></span>

### <span data-ttu-id="b8147-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8147-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8147-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8147-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8147-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8147-107">DESCRIPTION</span></span>
<span data-ttu-id="b8147-108">Törli a Kusto-fürtös principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b8147-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b8147-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8147-109">EXAMPLES</span></span>

### <span data-ttu-id="b8147-110">Példa 1: meglévő Kusto törlése PrincipalAssignment név szerint</span><span class="sxs-lookup"><span data-stu-id="b8147-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="b8147-111">A fenti parancs törli a "kustoprincipal1" nevű PrincipalAssignment a Kusto "testnewkustocluster" nevű fürtjében.</span><span class="sxs-lookup"><span data-stu-id="b8147-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="b8147-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8147-112">PARAMETERS</span></span>

### <span data-ttu-id="b8147-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8147-113">-AsJob</span></span>
<span data-ttu-id="b8147-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="b8147-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b8147-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b8147-115">-ClusterName</span></span>
<span data-ttu-id="b8147-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b8147-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8147-117">-DefaultProfile</span></span>
<span data-ttu-id="b8147-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8147-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8147-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8147-119">-InputObject</span></span>
<span data-ttu-id="b8147-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8147-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8147-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="b8147-121">-NoWait</span></span>
<span data-ttu-id="b8147-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="b8147-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b8147-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8147-123">-PassThru</span></span>
<span data-ttu-id="b8147-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="b8147-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b8147-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b8147-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b8147-126">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="b8147-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8147-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8147-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b8147-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8147-129">-SubscriptionId</span></span>
<span data-ttu-id="b8147-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8147-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b8147-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b8147-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b8147-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8147-132">-Confirm</span></span>
<span data-ttu-id="b8147-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8147-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8147-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8147-134">-WhatIf</span></span>
<span data-ttu-id="b8147-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8147-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8147-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8147-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8147-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8147-137">CommonParameters</span></span>
<span data-ttu-id="b8147-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8147-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8147-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8147-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8147-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8147-140">INPUTS</span></span>

### <span data-ttu-id="b8147-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b8147-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b8147-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8147-142">OUTPUTS</span></span>

### <span data-ttu-id="b8147-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8147-143">System.Boolean</span></span>

## <span data-ttu-id="b8147-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8147-144">NOTES</span></span>

<span data-ttu-id="b8147-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b8147-145">ALIASES</span></span>

<span data-ttu-id="b8147-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="b8147-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8147-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b8147-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8147-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b8147-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8147-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b8147-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8147-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b8147-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b8147-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b8147-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="b8147-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b8147-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b8147-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8147-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="b8147-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b8147-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b8147-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8147-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b8147-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8147-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b8147-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b8147-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b8147-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8147-160">RELATED LINKS</span></span>

