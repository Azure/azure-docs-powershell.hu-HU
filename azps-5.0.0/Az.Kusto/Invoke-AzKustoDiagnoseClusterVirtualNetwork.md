---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194709"
---
# <span data-ttu-id="56712-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56712-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="56712-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56712-102">SYNOPSIS</span></span>
<span data-ttu-id="56712-103">Annak a külső erőforrásoknak a hálózati kapcsolati állapotát diagnosztizálja, amelyen a szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="56712-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="56712-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56712-104">SYNTAX</span></span>

### <span data-ttu-id="56712-105">Diagnózis (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="56712-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="56712-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56712-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56712-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="56712-107">DESCRIPTION</span></span>
<span data-ttu-id="56712-108">Annak a külső erőforrásoknak a hálózati kapcsolati állapotát diagnosztizálja, amelyen a szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="56712-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="56712-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56712-109">EXAMPLES</span></span>

### <span data-ttu-id="56712-110">1. példa: külső erőforrások hálózati kapcsolati diagnosztizálásának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="56712-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="56712-111">A fenti parancs a külső erőforrásokhoz tartozó hálózati kapcsolati állapotot diagnosztizálja, amelyen a "testnewkustocluster" szektorcsoport függ</span><span class="sxs-lookup"><span data-stu-id="56712-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="56712-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56712-112">PARAMETERS</span></span>

### <span data-ttu-id="56712-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56712-113">-AsJob</span></span>
<span data-ttu-id="56712-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="56712-114">Run the command as a job</span></span>

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

### <span data-ttu-id="56712-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="56712-115">-ClusterName</span></span>
<span data-ttu-id="56712-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="56712-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="56712-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56712-117">-DefaultProfile</span></span>
<span data-ttu-id="56712-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56712-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56712-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56712-119">-InputObject</span></span>
<span data-ttu-id="56712-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56712-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56712-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="56712-121">-NoWait</span></span>
<span data-ttu-id="56712-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="56712-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56712-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56712-123">-ResourceGroupName</span></span>
<span data-ttu-id="56712-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="56712-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="56712-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56712-125">-SubscriptionId</span></span>
<span data-ttu-id="56712-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="56712-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="56712-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="56712-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="56712-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56712-128">-Confirm</span></span>
<span data-ttu-id="56712-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56712-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56712-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56712-130">-WhatIf</span></span>
<span data-ttu-id="56712-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56712-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56712-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56712-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56712-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56712-133">CommonParameters</span></span>
<span data-ttu-id="56712-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56712-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56712-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56712-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56712-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56712-136">INPUTS</span></span>

### <span data-ttu-id="56712-137">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="56712-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="56712-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56712-138">OUTPUTS</span></span>

### <span data-ttu-id="56712-139">System. String</span><span class="sxs-lookup"><span data-stu-id="56712-139">System.String</span></span>

## <span data-ttu-id="56712-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56712-140">NOTES</span></span>

<span data-ttu-id="56712-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="56712-141">ALIASES</span></span>

<span data-ttu-id="56712-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="56712-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56712-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="56712-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56712-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="56712-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56712-145">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="56712-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56712-146">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="56712-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="56712-147">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="56712-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="56712-148">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="56712-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="56712-149">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="56712-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="56712-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="56712-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56712-151">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="56712-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="56712-152">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="56712-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="56712-153">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="56712-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="56712-154">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="56712-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="56712-155">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="56712-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="56712-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56712-156">RELATED LINKS</span></span>

