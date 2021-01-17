---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476914"
---
# <span data-ttu-id="92dcf-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="92dcf-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="92dcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="92dcf-103">Leállít egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="92dcf-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="92dcf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92dcf-104">SYNTAX</span></span>

### <span data-ttu-id="92dcf-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92dcf-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92dcf-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92dcf-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92dcf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92dcf-107">DESCRIPTION</span></span>
<span data-ttu-id="92dcf-108">Leállít egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="92dcf-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="92dcf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92dcf-109">EXAMPLES</span></span>

### <span data-ttu-id="92dcf-110">1. példa: Kusto-fürt leállítása</span><span class="sxs-lookup"><span data-stu-id="92dcf-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="92dcf-111">A fenti parancs leállítja a Kusto-fürtöt</span><span class="sxs-lookup"><span data-stu-id="92dcf-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="92dcf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92dcf-112">PARAMETERS</span></span>

### <span data-ttu-id="92dcf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92dcf-113">-AsJob</span></span>
<span data-ttu-id="92dcf-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="92dcf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="92dcf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92dcf-115">-DefaultProfile</span></span>
<span data-ttu-id="92dcf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92dcf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92dcf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92dcf-117">-InputObject</span></span>
<span data-ttu-id="92dcf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="92dcf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92dcf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="92dcf-119">-Name</span></span>
<span data-ttu-id="92dcf-120">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="92dcf-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92dcf-121">-NoWait</span></span>
<span data-ttu-id="92dcf-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="92dcf-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92dcf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92dcf-123">-PassThru</span></span>
<span data-ttu-id="92dcf-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="92dcf-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92dcf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92dcf-125">-ResourceGroupName</span></span>
<span data-ttu-id="92dcf-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="92dcf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92dcf-127">-SubscriptionId</span></span>
<span data-ttu-id="92dcf-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="92dcf-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92dcf-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="92dcf-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="92dcf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92dcf-130">-Confirm</span></span>
<span data-ttu-id="92dcf-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92dcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92dcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92dcf-132">-WhatIf</span></span>
<span data-ttu-id="92dcf-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92dcf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92dcf-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92dcf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92dcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92dcf-135">CommonParameters</span></span>
<span data-ttu-id="92dcf-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92dcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92dcf-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92dcf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92dcf-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92dcf-138">INPUTS</span></span>

### <span data-ttu-id="92dcf-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="92dcf-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="92dcf-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92dcf-140">OUTPUTS</span></span>

### <span data-ttu-id="92dcf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92dcf-141">System.Boolean</span></span>

## <span data-ttu-id="92dcf-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92dcf-142">NOTES</span></span>

<span data-ttu-id="92dcf-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92dcf-143">ALIASES</span></span>

<span data-ttu-id="92dcf-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="92dcf-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92dcf-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="92dcf-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92dcf-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92dcf-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92dcf-147">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="92dcf-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92dcf-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="92dcf-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="92dcf-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="92dcf-151">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="92dcf-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="92dcf-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92dcf-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="92dcf-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="92dcf-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="92dcf-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92dcf-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="92dcf-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="92dcf-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92dcf-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="92dcf-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="92dcf-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92dcf-158">RELATED LINKS</span></span>

