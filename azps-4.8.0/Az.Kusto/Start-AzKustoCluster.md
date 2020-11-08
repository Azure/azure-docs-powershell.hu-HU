---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018210"
---
# <span data-ttu-id="e49ab-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e49ab-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="e49ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e49ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e49ab-103">Elindítja a Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e49ab-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="e49ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e49ab-104">SYNTAX</span></span>

### <span data-ttu-id="e49ab-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e49ab-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e49ab-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e49ab-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e49ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e49ab-107">DESCRIPTION</span></span>
<span data-ttu-id="e49ab-108">Elindítja a Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e49ab-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="e49ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e49ab-109">EXAMPLES</span></span>

### <span data-ttu-id="e49ab-110">Példa 1: Kusto-fürt indítása</span><span class="sxs-lookup"><span data-stu-id="e49ab-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="e49ab-111">A fenti parancs elindítja a Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e49ab-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="e49ab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e49ab-112">PARAMETERS</span></span>

### <span data-ttu-id="e49ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e49ab-113">-AsJob</span></span>
<span data-ttu-id="e49ab-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e49ab-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e49ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49ab-115">-DefaultProfile</span></span>
<span data-ttu-id="e49ab-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e49ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e49ab-117">-InputObject</span></span>
<span data-ttu-id="e49ab-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e49ab-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e49ab-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e49ab-119">-Name</span></span>
<span data-ttu-id="e49ab-120">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e49ab-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="e49ab-121">-NoWait</span></span>
<span data-ttu-id="e49ab-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e49ab-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e49ab-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e49ab-123">-PassThru</span></span>
<span data-ttu-id="e49ab-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="e49ab-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e49ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="e49ab-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e49ab-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e49ab-127">-SubscriptionId</span></span>
<span data-ttu-id="e49ab-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e49ab-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e49ab-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e49ab-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e49ab-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e49ab-130">-Confirm</span></span>
<span data-ttu-id="e49ab-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e49ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e49ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49ab-132">-WhatIf</span></span>
<span data-ttu-id="e49ab-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e49ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49ab-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e49ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e49ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49ab-135">CommonParameters</span></span>
<span data-ttu-id="e49ab-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e49ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49ab-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e49ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49ab-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e49ab-138">INPUTS</span></span>

### <span data-ttu-id="e49ab-139">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e49ab-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e49ab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e49ab-140">OUTPUTS</span></span>

### <span data-ttu-id="e49ab-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e49ab-141">System.Boolean</span></span>

## <span data-ttu-id="e49ab-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e49ab-142">NOTES</span></span>

<span data-ttu-id="e49ab-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e49ab-143">ALIASES</span></span>

<span data-ttu-id="e49ab-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e49ab-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e49ab-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e49ab-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e49ab-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e49ab-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e49ab-147">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e49ab-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e49ab-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e49ab-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e49ab-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e49ab-151">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="e49ab-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e49ab-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e49ab-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e49ab-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="e49ab-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e49ab-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e49ab-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e49ab-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e49ab-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e49ab-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e49ab-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e49ab-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e49ab-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e49ab-158">RELATED LINKS</span></span>

