---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024747"
---
# <span data-ttu-id="ed887-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="ed887-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="ed887-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed887-102">SYNOPSIS</span></span>
<span data-ttu-id="ed887-103">Eltávolíthatja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="ed887-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ed887-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed887-104">SYNTAX</span></span>

### <span data-ttu-id="ed887-105">RemoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed887-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed887-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ed887-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed887-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed887-107">DESCRIPTION</span></span>
<span data-ttu-id="ed887-108">Eltávolíthatja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="ed887-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ed887-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed887-109">EXAMPLES</span></span>

### <span data-ttu-id="ed887-110">1. példa: a nyelvi kiterjesztések listájának eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="ed887-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="ed887-111">A fenti parancs eltávolítja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="ed887-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ed887-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed887-112">PARAMETERS</span></span>

### <span data-ttu-id="ed887-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed887-113">-AsJob</span></span>
<span data-ttu-id="ed887-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="ed887-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ed887-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ed887-115">-ClusterName</span></span>
<span data-ttu-id="ed887-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ed887-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed887-117">-DefaultProfile</span></span>
<span data-ttu-id="ed887-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed887-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed887-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed887-119">-InputObject</span></span>
<span data-ttu-id="ed887-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed887-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ed887-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="ed887-121">-NoWait</span></span>
<span data-ttu-id="ed887-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="ed887-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed887-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed887-123">-PassThru</span></span>
<span data-ttu-id="ed887-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="ed887-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ed887-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed887-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed887-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ed887-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed887-127">-SubscriptionId</span></span>
<span data-ttu-id="ed887-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed887-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ed887-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ed887-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ed887-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="ed887-130">-Value</span></span>
<span data-ttu-id="ed887-131">A nyelvi kiterjesztések listája.</span><span class="sxs-lookup"><span data-stu-id="ed887-131">The list of language extensions.</span></span>
<span data-ttu-id="ed887-132">A kivitelezéshez lásd: az érték tulajdonságainak FELJEGYZÉSek szakasza, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ed887-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ed887-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed887-133">-Confirm</span></span>
<span data-ttu-id="ed887-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed887-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed887-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed887-135">-WhatIf</span></span>
<span data-ttu-id="ed887-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed887-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed887-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed887-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed887-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed887-138">CommonParameters</span></span>
<span data-ttu-id="ed887-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed887-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed887-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed887-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed887-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed887-141">INPUTS</span></span>

### <span data-ttu-id="ed887-142">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ed887-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ed887-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed887-143">OUTPUTS</span></span>

### <span data-ttu-id="ed887-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed887-144">System.Boolean</span></span>

## <span data-ttu-id="ed887-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed887-145">NOTES</span></span>

<span data-ttu-id="ed887-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ed887-146">ALIASES</span></span>

<span data-ttu-id="ed887-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="ed887-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed887-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ed887-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed887-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ed887-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed887-150">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ed887-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed887-151">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ed887-152">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ed887-153">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ed887-154">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="ed887-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ed887-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ed887-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed887-156">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="ed887-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ed887-157">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ed887-158">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ed887-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed887-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ed887-160">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ed887-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ed887-161">VALUE <ILanguageExtension [] >: a nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="ed887-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ed887-162">`[Name <LanguageExtensionName?>]`: A nyelvi kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="ed887-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="ed887-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed887-163">RELATED LINKS</span></span>

