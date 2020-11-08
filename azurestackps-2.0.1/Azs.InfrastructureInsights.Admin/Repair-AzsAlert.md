---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015221"
---
# <span data-ttu-id="7804d-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="7804d-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="7804d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7804d-102">SYNOPSIS</span></span>
<span data-ttu-id="7804d-103">Riasztás kijavítása</span><span class="sxs-lookup"><span data-stu-id="7804d-103">Repairs an alert.</span></span>

## <span data-ttu-id="7804d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7804d-104">SYNTAX</span></span>

### <span data-ttu-id="7804d-105">Javítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7804d-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7804d-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7804d-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7804d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7804d-107">DESCRIPTION</span></span>
<span data-ttu-id="7804d-108">Riasztás kijavítása</span><span class="sxs-lookup"><span data-stu-id="7804d-108">Repairs an alert.</span></span>

## <span data-ttu-id="7804d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7804d-109">EXAMPLES</span></span>

### <span data-ttu-id="7804d-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="7804d-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="7804d-111">Riasztás kijavítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7804d-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="7804d-112">2. példa:</span><span class="sxs-lookup"><span data-stu-id="7804d-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="7804d-113">A csöveken keresztüli riasztás kijavítása.</span><span class="sxs-lookup"><span data-stu-id="7804d-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="7804d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7804d-114">PARAMETERS</span></span>

### <span data-ttu-id="7804d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7804d-115">-AsJob</span></span>
<span data-ttu-id="7804d-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="7804d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7804d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7804d-117">-DefaultProfile</span></span>
<span data-ttu-id="7804d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7804d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7804d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7804d-119">-InputObject</span></span>
<span data-ttu-id="7804d-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7804d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7804d-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="7804d-121">-Location</span></span>
<span data-ttu-id="7804d-122">A régió neve</span><span class="sxs-lookup"><span data-stu-id="7804d-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7804d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7804d-123">-Name</span></span>
<span data-ttu-id="7804d-124">A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="7804d-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7804d-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="7804d-125">-NoWait</span></span>
<span data-ttu-id="7804d-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="7804d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7804d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7804d-127">-PassThru</span></span>
<span data-ttu-id="7804d-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="7804d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7804d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7804d-129">-ResourceGroupName</span></span>
<span data-ttu-id="7804d-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7804d-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7804d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7804d-131">-SubscriptionId</span></span>
<span data-ttu-id="7804d-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="7804d-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7804d-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7804d-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7804d-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7804d-134">-Confirm</span></span>
<span data-ttu-id="7804d-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7804d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7804d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7804d-136">-WhatIf</span></span>
<span data-ttu-id="7804d-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7804d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7804d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7804d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7804d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7804d-139">CommonParameters</span></span>
<span data-ttu-id="7804d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7804d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7804d-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7804d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7804d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7804d-142">INPUTS</span></span>

### <span data-ttu-id="7804d-143">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7804d-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="7804d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7804d-144">OUTPUTS</span></span>

### <span data-ttu-id="7804d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7804d-145">System.Boolean</span></span>



## <span data-ttu-id="7804d-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7804d-146">NOTES</span></span>

<span data-ttu-id="7804d-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7804d-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7804d-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7804d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7804d-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="7804d-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7804d-150">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="7804d-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="7804d-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7804d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7804d-152">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="7804d-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="7804d-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7804d-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7804d-154">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="7804d-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="7804d-155">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="7804d-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="7804d-156">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="7804d-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="7804d-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="7804d-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7804d-158">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7804d-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7804d-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7804d-159">RELATED LINKS</span></span>

