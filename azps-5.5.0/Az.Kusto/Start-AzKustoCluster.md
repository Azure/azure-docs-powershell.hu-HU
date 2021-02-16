---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161491"
---
# <span data-ttu-id="d7fa3-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d7fa3-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="d7fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fa3-103">Kusto-fürt indítása.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="d7fa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7fa3-104">SYNTAX</span></span>

### <span data-ttu-id="d7fa3-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7fa3-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7fa3-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7fa3-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7fa3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7fa3-107">DESCRIPTION</span></span>
<span data-ttu-id="d7fa3-108">Kusto-fürt indítása.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="d7fa3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7fa3-109">EXAMPLES</span></span>

### <span data-ttu-id="d7fa3-110">1. példa: Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="d7fa3-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="d7fa3-111">A fenti parancs egy Kusto-fürtöt kezd el.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="d7fa3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7fa3-112">PARAMETERS</span></span>

### <span data-ttu-id="d7fa3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7fa3-113">-AsJob</span></span>
<span data-ttu-id="d7fa3-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d7fa3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d7fa3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fa3-115">-DefaultProfile</span></span>
<span data-ttu-id="d7fa3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7fa3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7fa3-117">-InputObject</span></span>
<span data-ttu-id="d7fa3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7fa3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d7fa3-119">-Name</span></span>
<span data-ttu-id="d7fa3-120">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fa3-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d7fa3-121">-NoWait</span></span>
<span data-ttu-id="d7fa3-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d7fa3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d7fa3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7fa3-123">-PassThru</span></span>
<span data-ttu-id="d7fa3-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="d7fa3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d7fa3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7fa3-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7fa3-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fa3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7fa3-127">-SubscriptionId</span></span>
<span data-ttu-id="d7fa3-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7fa3-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fa3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7fa3-130">-Confirm</span></span>
<span data-ttu-id="d7fa3-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7fa3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7fa3-132">-WhatIf</span></span>
<span data-ttu-id="d7fa3-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7fa3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7fa3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fa3-135">CommonParameters</span></span>
<span data-ttu-id="d7fa3-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fa3-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7fa3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fa3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7fa3-138">INPUTS</span></span>

### <span data-ttu-id="d7fa3-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d7fa3-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d7fa3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7fa3-140">OUTPUTS</span></span>

### <span data-ttu-id="d7fa3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7fa3-141">System.Boolean</span></span>

## <span data-ttu-id="d7fa3-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7fa3-142">NOTES</span></span>

<span data-ttu-id="d7fa3-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d7fa3-143">ALIASES</span></span>

<span data-ttu-id="d7fa3-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d7fa3-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7fa3-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7fa3-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7fa3-147">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d7fa3-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7fa3-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d7fa3-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d7fa3-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d7fa3-151">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d7fa3-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d7fa3-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7fa3-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d7fa3-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d7fa3-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d7fa3-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d7fa3-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d7fa3-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d7fa3-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7fa3-158">RELATED LINKS</span></span>

