---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018219"
---
# <span data-ttu-id="88b06-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="88b06-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="88b06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88b06-102">SYNOPSIS</span></span>
<span data-ttu-id="88b06-103">A csatolt adatbázis-konfiguráció törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="88b06-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="88b06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88b06-104">SYNTAX</span></span>

### <span data-ttu-id="88b06-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88b06-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="88b06-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88b06-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88b06-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88b06-107">DESCRIPTION</span></span>
<span data-ttu-id="88b06-108">A csatolt adatbázis-konfiguráció törlése a megadott névvel</span><span class="sxs-lookup"><span data-stu-id="88b06-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="88b06-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88b06-109">EXAMPLES</span></span>

### <span data-ttu-id="88b06-110">Példa 1: meglévő AttachedDatabaseConfiguration törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="88b06-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="88b06-111">A fenti parancs törli a "myfollowerconfiguration" AttachedDatabaseConfiguration "" testnewkustoclusterf megadott követő adatbázist.</span><span class="sxs-lookup"><span data-stu-id="88b06-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="88b06-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88b06-112">PARAMETERS</span></span>

### <span data-ttu-id="88b06-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88b06-113">-AsJob</span></span>
<span data-ttu-id="88b06-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="88b06-114">Run the command as a job</span></span>

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

### <span data-ttu-id="88b06-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="88b06-115">-ClusterName</span></span>
<span data-ttu-id="88b06-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="88b06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b06-117">-DefaultProfile</span></span>
<span data-ttu-id="88b06-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88b06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b06-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88b06-119">-InputObject</span></span>
<span data-ttu-id="88b06-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88b06-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88b06-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88b06-121">-Name</span></span>
<span data-ttu-id="88b06-122">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-122">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="88b06-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="88b06-123">-NoWait</span></span>
<span data-ttu-id="88b06-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="88b06-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88b06-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88b06-125">-PassThru</span></span>
<span data-ttu-id="88b06-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="88b06-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88b06-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b06-127">-ResourceGroupName</span></span>
<span data-ttu-id="88b06-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="88b06-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88b06-129">-SubscriptionId</span></span>
<span data-ttu-id="88b06-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="88b06-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88b06-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="88b06-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88b06-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88b06-132">-Confirm</span></span>
<span data-ttu-id="88b06-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88b06-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b06-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b06-134">-WhatIf</span></span>
<span data-ttu-id="88b06-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88b06-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b06-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88b06-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b06-137">CommonParameters</span></span>
<span data-ttu-id="88b06-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88b06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b06-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88b06-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b06-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b06-140">INPUTS</span></span>

### <span data-ttu-id="88b06-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="88b06-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="88b06-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b06-142">OUTPUTS</span></span>

### <span data-ttu-id="88b06-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88b06-143">System.Boolean</span></span>

## <span data-ttu-id="88b06-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88b06-144">NOTES</span></span>

<span data-ttu-id="88b06-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="88b06-145">ALIASES</span></span>

<span data-ttu-id="88b06-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="88b06-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88b06-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="88b06-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88b06-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="88b06-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88b06-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="88b06-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88b06-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="88b06-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="88b06-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="88b06-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="88b06-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="88b06-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="88b06-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88b06-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="88b06-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="88b06-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="88b06-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88b06-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="88b06-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="88b06-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88b06-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="88b06-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88b06-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88b06-160">RELATED LINKS</span></span>

