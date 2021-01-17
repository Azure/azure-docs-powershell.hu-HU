---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332153"
---
# <span data-ttu-id="7c30c-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c30c-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="7c30c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c30c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c30c-103">Diagnosztizálja a hálózati kapcsolat állapotát azokkal a külső erőforrásokkal, amelyektől a szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="7c30c-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="7c30c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c30c-104">SYNTAX</span></span>

### <span data-ttu-id="7c30c-105">Diagnosztizálás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c30c-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7c30c-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c30c-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c30c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c30c-107">DESCRIPTION</span></span>
<span data-ttu-id="7c30c-108">Diagnosztizálja a hálózati kapcsolat állapotát azokkal a külső erőforrásokkal, amelyektől a szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="7c30c-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="7c30c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c30c-109">EXAMPLES</span></span>

### <span data-ttu-id="7c30c-110">1. példa: Hálózati kapcsolati problémák megjelenítése külső erőforrások esetén</span><span class="sxs-lookup"><span data-stu-id="7c30c-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="7c30c-111">A fenti parancs a külső erőforrások hálózati kapcsolati állapotát diagnosztizálja, amelyektől az "testnewkustocluster" fürt függ</span><span class="sxs-lookup"><span data-stu-id="7c30c-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="7c30c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c30c-112">PARAMETERS</span></span>

### <span data-ttu-id="7c30c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c30c-113">-AsJob</span></span>
<span data-ttu-id="7c30c-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7c30c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7c30c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7c30c-115">-ClusterName</span></span>
<span data-ttu-id="7c30c-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c30c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c30c-117">-DefaultProfile</span></span>
<span data-ttu-id="7c30c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c30c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c30c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c30c-119">-InputObject</span></span>
<span data-ttu-id="7c30c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7c30c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c30c-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c30c-121">-NoWait</span></span>
<span data-ttu-id="7c30c-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7c30c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c30c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c30c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c30c-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c30c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c30c-125">-SubscriptionId</span></span>
<span data-ttu-id="7c30c-126">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7c30c-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c30c-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7c30c-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c30c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c30c-128">-Confirm</span></span>
<span data-ttu-id="7c30c-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c30c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c30c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c30c-130">-WhatIf</span></span>
<span data-ttu-id="7c30c-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c30c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c30c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c30c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c30c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c30c-133">CommonParameters</span></span>
<span data-ttu-id="7c30c-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c30c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c30c-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c30c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c30c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c30c-136">INPUTS</span></span>

### <span data-ttu-id="7c30c-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7c30c-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7c30c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c30c-138">OUTPUTS</span></span>

### <span data-ttu-id="7c30c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7c30c-139">System.String</span></span>

## <span data-ttu-id="7c30c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c30c-140">NOTES</span></span>

<span data-ttu-id="7c30c-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7c30c-141">ALIASES</span></span>

<span data-ttu-id="7c30c-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7c30c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c30c-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7c30c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c30c-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c30c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c30c-145">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7c30c-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c30c-146">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7c30c-147">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7c30c-148">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7c30c-149">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7c30c-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7c30c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c30c-151">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="7c30c-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7c30c-152">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7c30c-153">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c30c-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7c30c-154">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7c30c-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7c30c-155">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7c30c-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7c30c-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c30c-156">RELATED LINKS</span></span>

