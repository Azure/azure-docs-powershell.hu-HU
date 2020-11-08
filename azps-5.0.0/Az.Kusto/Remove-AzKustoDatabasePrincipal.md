---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194687"
---
# <span data-ttu-id="e6424-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e6424-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="e6424-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6424-102">SYNOPSIS</span></span>
<span data-ttu-id="e6424-103">Adatbázis-résztvevők engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6424-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="e6424-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6424-104">SYNTAX</span></span>

### <span data-ttu-id="e6424-105">RemoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6424-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e6424-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e6424-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6424-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6424-107">DESCRIPTION</span></span>
<span data-ttu-id="e6424-108">Adatbázis-résztvevők engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6424-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="e6424-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e6424-109">EXAMPLES</span></span>

### <span data-ttu-id="e6424-110">1. példa: az adatbázis-résztvevők engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6424-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="e6424-111">A fenti parancs eltávolítja az adatbázis-résztvevők engedélyeit</span><span class="sxs-lookup"><span data-stu-id="e6424-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="e6424-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6424-112">PARAMETERS</span></span>

### <span data-ttu-id="e6424-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e6424-113">-ClusterName</span></span>
<span data-ttu-id="e6424-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e6424-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6424-115">-DatabaseName</span></span>
<span data-ttu-id="e6424-116">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="e6424-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="e6424-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6424-117">-DefaultProfile</span></span>
<span data-ttu-id="e6424-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6424-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6424-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6424-119">-InputObject</span></span>
<span data-ttu-id="e6424-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6424-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e6424-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6424-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6424-122">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e6424-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6424-123">-SubscriptionId</span></span>
<span data-ttu-id="e6424-124">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6424-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e6424-125">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6424-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e6424-126">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="e6424-126">-Value</span></span>
<span data-ttu-id="e6424-127">A Kusto-adatbázis-résztvevők listája.</span><span class="sxs-lookup"><span data-stu-id="e6424-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="e6424-128">A kivitelezéshez lásd: az érték tulajdonságainak FELJEGYZÉSek szakasza, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e6424-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6424-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6424-129">-Confirm</span></span>
<span data-ttu-id="e6424-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6424-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6424-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6424-131">-WhatIf</span></span>
<span data-ttu-id="e6424-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6424-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6424-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6424-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6424-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6424-134">CommonParameters</span></span>
<span data-ttu-id="e6424-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6424-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6424-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6424-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6424-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6424-137">INPUTS</span></span>

### <span data-ttu-id="e6424-138">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e6424-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e6424-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6424-139">OUTPUTS</span></span>

### <span data-ttu-id="e6424-140">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e6424-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="e6424-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6424-141">NOTES</span></span>

<span data-ttu-id="e6424-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e6424-142">ALIASES</span></span>

<span data-ttu-id="e6424-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e6424-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6424-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e6424-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6424-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e6424-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6424-146">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e6424-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6424-147">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e6424-148">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e6424-149">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e6424-150">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="e6424-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e6424-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e6424-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6424-152">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="e6424-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e6424-153">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e6424-154">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6424-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e6424-155">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6424-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e6424-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6424-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e6424-157">VALUE <IDatabasePrincipal [] >: a Kusto adatbázis-résztvevők listája.</span><span class="sxs-lookup"><span data-stu-id="e6424-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="e6424-158">`Name <String>`: Adatbázis-egyszerű név.</span><span class="sxs-lookup"><span data-stu-id="e6424-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="e6424-159">`Role <DatabasePrincipalRole>`: Adatbázis-résztvevők szerepköre</span><span class="sxs-lookup"><span data-stu-id="e6424-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="e6424-160">`Type <DatabasePrincipalType>`: Adatbázis-résztvevő típusa.</span><span class="sxs-lookup"><span data-stu-id="e6424-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="e6424-161">`[AppId <String>]`: Alkalmazásspecifikus azonosító – csak az alkalmazásobjektum-típus esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="e6424-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="e6424-162">`[Email <String>]`: Ha létezik, az adatbázis-résztvevők e-mail-címe</span><span class="sxs-lookup"><span data-stu-id="e6424-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="e6424-163">`[Fqn <String>]`: Adatbázis-résztvevő: teljes mértékben minősített név.</span><span class="sxs-lookup"><span data-stu-id="e6424-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="e6424-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6424-164">RELATED LINKS</span></span>

