---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194694"
---
# <span data-ttu-id="6f705-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="6f705-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="6f705-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f705-102">SYNOPSIS</span></span>
<span data-ttu-id="6f705-103">Eltávolíthatja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="6f705-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6f705-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f705-104">SYNTAX</span></span>

### <span data-ttu-id="6f705-105">RemoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f705-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6f705-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6f705-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f705-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f705-107">DESCRIPTION</span></span>
<span data-ttu-id="6f705-108">Eltávolíthatja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="6f705-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6f705-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6f705-109">EXAMPLES</span></span>

### <span data-ttu-id="6f705-110">1. példa: a nyelvi kiterjesztések listájának eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="6f705-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="6f705-111">A fenti parancs eltávolítja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="6f705-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6f705-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f705-112">PARAMETERS</span></span>

### <span data-ttu-id="6f705-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f705-113">-AsJob</span></span>
<span data-ttu-id="6f705-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6f705-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6f705-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="6f705-115">-ClusterName</span></span>
<span data-ttu-id="6f705-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f705-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f705-117">-DefaultProfile</span></span>
<span data-ttu-id="6f705-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f705-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f705-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f705-119">-InputObject</span></span>
<span data-ttu-id="6f705-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f705-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f705-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="6f705-121">-NoWait</span></span>
<span data-ttu-id="6f705-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6f705-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6f705-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f705-123">-PassThru</span></span>
<span data-ttu-id="6f705-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="6f705-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6f705-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f705-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f705-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f705-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f705-127">-SubscriptionId</span></span>
<span data-ttu-id="6f705-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f705-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6f705-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6f705-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f705-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="6f705-130">-Value</span></span>
<span data-ttu-id="6f705-131">A nyelvi kiterjesztések listája.</span><span class="sxs-lookup"><span data-stu-id="6f705-131">The list of language extensions.</span></span>
<span data-ttu-id="6f705-132">A kivitelezéshez lásd: az érték tulajdonságainak FELJEGYZÉSek szakasza, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6f705-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f705-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f705-133">-Confirm</span></span>
<span data-ttu-id="6f705-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f705-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f705-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f705-135">-WhatIf</span></span>
<span data-ttu-id="6f705-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f705-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f705-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f705-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f705-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f705-138">CommonParameters</span></span>
<span data-ttu-id="6f705-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f705-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f705-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f705-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f705-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f705-141">INPUTS</span></span>

### <span data-ttu-id="6f705-142">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6f705-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6f705-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f705-143">OUTPUTS</span></span>

### <span data-ttu-id="6f705-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f705-144">System.Boolean</span></span>

## <span data-ttu-id="6f705-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f705-145">NOTES</span></span>

<span data-ttu-id="6f705-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6f705-146">ALIASES</span></span>

<span data-ttu-id="6f705-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6f705-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f705-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6f705-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f705-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6f705-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f705-150">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6f705-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f705-151">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6f705-152">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6f705-153">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6f705-154">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="6f705-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6f705-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6f705-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f705-156">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="6f705-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6f705-157">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6f705-158">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6f705-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f705-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6f705-160">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6f705-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="6f705-161">VALUE <ILanguageExtension [] >: a nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="6f705-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="6f705-162">`[Name <LanguageExtensionName?>]`: A nyelvi kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="6f705-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="6f705-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f705-163">RELATED LINKS</span></span>

