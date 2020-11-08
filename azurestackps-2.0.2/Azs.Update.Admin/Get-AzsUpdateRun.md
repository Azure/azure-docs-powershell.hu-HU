---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/29/2020
ms.locfileid: "94017349"
---
# <span data-ttu-id="4559d-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4559d-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="4559d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4559d-102">SYNOPSIS</span></span>
<span data-ttu-id="4559d-103">Az AZONOSÍTÓval beolvashatja az Update Run példányát.</span><span class="sxs-lookup"><span data-stu-id="4559d-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="4559d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4559d-104">SYNTAX</span></span>

### <span data-ttu-id="4559d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4559d-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4559d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4559d-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4559d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4559d-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4559d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4559d-108">DESCRIPTION</span></span>
<span data-ttu-id="4559d-109">Az AZONOSÍTÓval beolvashatja az Update Run példányát.</span><span class="sxs-lookup"><span data-stu-id="4559d-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="4559d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4559d-110">EXAMPLES</span></span>

### <span data-ttu-id="4559d-111">Példa 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4559d-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="4559d-112">Ha nem adja meg a UpdateName értékét, a Get-UpdateRun mindig a bevitelt kérni fogja.</span><span class="sxs-lookup"><span data-stu-id="4559d-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="4559d-113">A beírást követően a UpdateRun minden olyan előfordulását megjeleníti, amely sikertelen vagy sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="4559d-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="4559d-114">2. példa: UpdateName szerint Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4559d-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="4559d-115">Egy adott frissítéshez társított összes UpdateRuns lekérése</span><span class="sxs-lookup"><span data-stu-id="4559d-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="4559d-116">2. példa: Get-AzsUpdateRun név szerint</span><span class="sxs-lookup"><span data-stu-id="4559d-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="4559d-117">Visszaadja az adott frissítéshez társított összes UpdateRuns és egy konkrét nevet.</span><span class="sxs-lookup"><span data-stu-id="4559d-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="4559d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4559d-118">PARAMETERS</span></span>

### <span data-ttu-id="4559d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4559d-119">-DefaultProfile</span></span>
<span data-ttu-id="4559d-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4559d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4559d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4559d-121">-InputObject</span></span>
<span data-ttu-id="4559d-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4559d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="4559d-123">-Location</span></span>
<span data-ttu-id="4559d-124">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="4559d-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4559d-125">-Name</span></span>
<span data-ttu-id="4559d-126">A futtatási azonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="4559d-126">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4559d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4559d-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4559d-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4559d-129">-SubscriptionId</span></span>
<span data-ttu-id="4559d-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4559d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4559d-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4559d-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="4559d-132">-UpdateName</span></span>
<span data-ttu-id="4559d-133">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="4559d-133">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4559d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4559d-134">CommonParameters</span></span>
<span data-ttu-id="4559d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4559d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4559d-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4559d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4559d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4559d-137">INPUTS</span></span>

### <span data-ttu-id="4559d-138">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4559d-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="4559d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4559d-139">OUTPUTS</span></span>

### <span data-ttu-id="4559d-140">Microsoft. Azure. PowerShell. parancsmagok. UpdateAdmin. modellek. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4559d-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="4559d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4559d-141">NOTES</span></span>

<span data-ttu-id="4559d-142">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4559d-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4559d-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4559d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4559d-144">INPUTOBJECT <IUpdateAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4559d-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4559d-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4559d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4559d-146">`[ResourceGroupName <String>]`: Erőforrás-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4559d-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="4559d-147">`[RunName <String>]`: Update Run Identifier.</span><span class="sxs-lookup"><span data-stu-id="4559d-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="4559d-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4559d-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="4559d-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4559d-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4559d-150">`[UpdateLocation <String>]`: A frissítés helyének neve.</span><span class="sxs-lookup"><span data-stu-id="4559d-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="4559d-151">`[UpdateName <String>]`: A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="4559d-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="4559d-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4559d-152">RELATED LINKS</span></span>

