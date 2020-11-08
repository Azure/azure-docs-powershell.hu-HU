---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016745"
---
# <span data-ttu-id="39e40-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="39e40-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="39e40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39e40-102">SYNOPSIS</span></span>
<span data-ttu-id="39e40-103">Sikertelen frissítés folytatása</span><span class="sxs-lookup"><span data-stu-id="39e40-103">Resume a failed update.</span></span>

## <span data-ttu-id="39e40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39e40-104">SYNTAX</span></span>

### <span data-ttu-id="39e40-105">Ismétlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39e40-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39e40-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39e40-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39e40-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39e40-107">DESCRIPTION</span></span>
<span data-ttu-id="39e40-108">Sikertelen frissítés folytatása</span><span class="sxs-lookup"><span data-stu-id="39e40-108">Resume a failed update.</span></span>

## <span data-ttu-id="39e40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39e40-109">EXAMPLES</span></span>

### <span data-ttu-id="39e40-110">Példa 1: Resume-AzsUpdateRun név és UpdateName szerint</span><span class="sxs-lookup"><span data-stu-id="39e40-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="39e40-111">A parancsmagot lehetővé teszi az adott sikertelen frissítés futtatását.</span><span class="sxs-lookup"><span data-stu-id="39e40-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="39e40-112">Felhívjuk a figyelmét arra, hogy a frissítés verziószáma szigorúan meghaladja az aktuális verziót.</span><span class="sxs-lookup"><span data-stu-id="39e40-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="39e40-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39e40-113">PARAMETERS</span></span>

### <span data-ttu-id="39e40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e40-114">-DefaultProfile</span></span>
<span data-ttu-id="39e40-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39e40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39e40-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39e40-116">-InputObject</span></span>
<span data-ttu-id="39e40-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39e40-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="39e40-118">-Location</span></span>
<span data-ttu-id="39e40-119">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="39e40-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39e40-120">-Name</span></span>
<span data-ttu-id="39e40-121">A futtatási azonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="39e40-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39e40-122">-PassThru</span></span>
<span data-ttu-id="39e40-123">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="39e40-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39e40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e40-124">-ResourceGroupName</span></span>
<span data-ttu-id="39e40-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="39e40-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39e40-126">-SubscriptionId</span></span>
<span data-ttu-id="39e40-127">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="39e40-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39e40-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="39e40-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="39e40-129">-UpdateName</span></span>
<span data-ttu-id="39e40-130">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="39e40-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39e40-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39e40-131">-Confirm</span></span>
<span data-ttu-id="39e40-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39e40-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e40-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e40-133">-WhatIf</span></span>
<span data-ttu-id="39e40-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39e40-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39e40-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39e40-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e40-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e40-136">CommonParameters</span></span>
<span data-ttu-id="39e40-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39e40-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e40-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39e40-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e40-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39e40-139">INPUTS</span></span>

### <span data-ttu-id="39e40-140">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="39e40-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="39e40-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39e40-141">OUTPUTS</span></span>

### <span data-ttu-id="39e40-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39e40-142">System.Boolean</span></span>



## <span data-ttu-id="39e40-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39e40-143">NOTES</span></span>

<span data-ttu-id="39e40-144">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="39e40-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39e40-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="39e40-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="39e40-146">INPUTOBJECT <IUpdateAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="39e40-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39e40-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="39e40-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39e40-148">`[ResourceGroupName <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="39e40-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="39e40-149">`[RunName <String>]`: Update Run Identifier.</span><span class="sxs-lookup"><span data-stu-id="39e40-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="39e40-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="39e40-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="39e40-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="39e40-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="39e40-152">`[UpdateLocation <String>]`: A frissítés helyének neve.</span><span class="sxs-lookup"><span data-stu-id="39e40-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="39e40-153">`[UpdateName <String>]`: A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="39e40-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="39e40-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39e40-154">RELATED LINKS</span></span>

