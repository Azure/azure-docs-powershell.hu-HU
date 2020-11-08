---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195894"
---
# <span data-ttu-id="cd433-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="cd433-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="cd433-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd433-102">SYNOPSIS</span></span>
<span data-ttu-id="cd433-103">Leállít egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="cd433-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="cd433-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd433-104">SYNTAX</span></span>

### <span data-ttu-id="cd433-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd433-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd433-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd433-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd433-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd433-107">DESCRIPTION</span></span>
<span data-ttu-id="cd433-108">Leállít egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="cd433-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="cd433-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cd433-109">EXAMPLES</span></span>

### <span data-ttu-id="cd433-110">Példa 1: Kusto-fürt leállítása</span><span class="sxs-lookup"><span data-stu-id="cd433-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="cd433-111">A fenti parancs Kusto-fürtöt állít le</span><span class="sxs-lookup"><span data-stu-id="cd433-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="cd433-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd433-112">PARAMETERS</span></span>

### <span data-ttu-id="cd433-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd433-113">-AsJob</span></span>
<span data-ttu-id="cd433-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="cd433-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cd433-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd433-115">-DefaultProfile</span></span>
<span data-ttu-id="cd433-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd433-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd433-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd433-117">-InputObject</span></span>
<span data-ttu-id="cd433-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd433-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd433-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd433-119">-Name</span></span>
<span data-ttu-id="cd433-120">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd433-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="cd433-121">-NoWait</span></span>
<span data-ttu-id="cd433-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="cd433-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd433-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd433-123">-PassThru</span></span>
<span data-ttu-id="cd433-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="cd433-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd433-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd433-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd433-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd433-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd433-127">-SubscriptionId</span></span>
<span data-ttu-id="cd433-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd433-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd433-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="cd433-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd433-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd433-130">-Confirm</span></span>
<span data-ttu-id="cd433-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd433-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd433-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd433-132">-WhatIf</span></span>
<span data-ttu-id="cd433-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd433-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd433-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd433-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd433-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd433-135">CommonParameters</span></span>
<span data-ttu-id="cd433-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd433-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd433-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd433-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd433-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd433-138">INPUTS</span></span>

### <span data-ttu-id="cd433-139">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cd433-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cd433-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd433-140">OUTPUTS</span></span>

### <span data-ttu-id="cd433-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd433-141">System.Boolean</span></span>

## <span data-ttu-id="cd433-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd433-142">NOTES</span></span>

<span data-ttu-id="cd433-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cd433-143">ALIASES</span></span>

<span data-ttu-id="cd433-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="cd433-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd433-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="cd433-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd433-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="cd433-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd433-147">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="cd433-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd433-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cd433-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cd433-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cd433-151">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="cd433-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cd433-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cd433-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd433-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="cd433-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cd433-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cd433-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd433-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cd433-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd433-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cd433-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="cd433-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd433-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd433-158">RELATED LINKS</span></span>

