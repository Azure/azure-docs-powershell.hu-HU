---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181863"
---
# <span data-ttu-id="a284e-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="a284e-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="a284e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a284e-102">SYNOPSIS</span></span>
<span data-ttu-id="a284e-103">A KQL-lekérdezéseken belül futtatható nyelvi bővítmények listájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a284e-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="a284e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a284e-104">SYNTAX</span></span>

### <span data-ttu-id="a284e-105">AddExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a284e-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a284e-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a284e-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a284e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a284e-107">DESCRIPTION</span></span>
<span data-ttu-id="a284e-108">A KQL-lekérdezéseken belül futtatható nyelvi bővítmények listájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a284e-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="a284e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a284e-109">EXAMPLES</span></span>

### <span data-ttu-id="a284e-110">1. példa: nyelvi bővítmények listájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a284e-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="a284e-111">A fenti parancs hozzáadja a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="a284e-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="a284e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a284e-112">PARAMETERS</span></span>

### <span data-ttu-id="a284e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a284e-113">-AsJob</span></span>
<span data-ttu-id="a284e-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="a284e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a284e-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="a284e-115">-ClusterName</span></span>
<span data-ttu-id="a284e-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a284e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a284e-117">-DefaultProfile</span></span>
<span data-ttu-id="a284e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a284e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a284e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a284e-119">-InputObject</span></span>
<span data-ttu-id="a284e-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a284e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a284e-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="a284e-121">-NoWait</span></span>
<span data-ttu-id="a284e-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="a284e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a284e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a284e-123">-PassThru</span></span>
<span data-ttu-id="a284e-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a284e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a284e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a284e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a284e-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a284e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a284e-127">-SubscriptionId</span></span>
<span data-ttu-id="a284e-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a284e-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a284e-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a284e-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a284e-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="a284e-130">-Value</span></span>
<span data-ttu-id="a284e-131">A nyelvi kiterjesztések listája.</span><span class="sxs-lookup"><span data-stu-id="a284e-131">The list of language extensions.</span></span>
<span data-ttu-id="a284e-132">A kivitelezéshez lásd: az érték tulajdonságainak FELJEGYZÉSek szakasza, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a284e-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a284e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a284e-133">-Confirm</span></span>
<span data-ttu-id="a284e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a284e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a284e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a284e-135">-WhatIf</span></span>
<span data-ttu-id="a284e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a284e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a284e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a284e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a284e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a284e-138">CommonParameters</span></span>
<span data-ttu-id="a284e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a284e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a284e-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a284e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a284e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a284e-141">INPUTS</span></span>

### <span data-ttu-id="a284e-142">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a284e-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a284e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a284e-143">OUTPUTS</span></span>

### <span data-ttu-id="a284e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a284e-144">System.Boolean</span></span>

## <span data-ttu-id="a284e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a284e-145">NOTES</span></span>

<span data-ttu-id="a284e-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a284e-146">ALIASES</span></span>

<span data-ttu-id="a284e-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a284e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a284e-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a284e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a284e-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a284e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a284e-150">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a284e-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a284e-151">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a284e-152">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a284e-153">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a284e-154">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a284e-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a284e-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a284e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a284e-156">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="a284e-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a284e-157">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a284e-158">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a284e-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a284e-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a284e-160">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a284e-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="a284e-161">VALUE <ILanguageExtension [] >: a nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="a284e-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="a284e-162">`[Name <LanguageExtensionName?>]`: A nyelvi kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="a284e-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="a284e-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a284e-163">RELATED LINKS</span></span>

