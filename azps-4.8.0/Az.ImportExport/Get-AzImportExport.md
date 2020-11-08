---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182747"
---
# <span data-ttu-id="b28a0-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b28a0-101">Get-AzImportExport</span></span>

## <span data-ttu-id="b28a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b28a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b28a0-103">Információt kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="b28a0-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="b28a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b28a0-104">SYNTAX</span></span>

### <span data-ttu-id="b28a0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b28a0-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b28a0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b28a0-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b28a0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b28a0-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b28a0-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="b28a0-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b28a0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b28a0-109">DESCRIPTION</span></span>
<span data-ttu-id="b28a0-110">Információt kap egy meglévő feladatról.</span><span class="sxs-lookup"><span data-stu-id="b28a0-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="b28a0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b28a0-111">EXAMPLES</span></span>

### <span data-ttu-id="b28a0-112">Példa 1: a ImportExport feladatának beszerzése alapértelmezett környezettel</span><span class="sxs-lookup"><span data-stu-id="b28a0-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b28a0-113">Ez a parancsmag alapértelmezett környezettel kapja a ImportExport-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b28a0-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="b28a0-114">2. példa: ImportExport-feladat beszerzése erőforráscsoport és feladatnév szerint</span><span class="sxs-lookup"><span data-stu-id="b28a0-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b28a0-115">Ez a parancsmag az erőforráscsoport és a feladatnév szerint kap ImportExport munkát.</span><span class="sxs-lookup"><span data-stu-id="b28a0-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="b28a0-116">3. példa: a megadott erőforráscsoport ImportExport feladatok listája</span><span class="sxs-lookup"><span data-stu-id="b28a0-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b28a0-117">Ez a parancsmag felsorolja a megadott erőforráscsoport összes ImportExport-feladatát.</span><span class="sxs-lookup"><span data-stu-id="b28a0-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="b28a0-118">4. példa: ImportExport-feladat beszerzése identitással</span><span class="sxs-lookup"><span data-stu-id="b28a0-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b28a0-119">Ez a parancsmag a ImportExport a feladatot identitás szerint jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b28a0-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="b28a0-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b28a0-120">PARAMETERS</span></span>

### <span data-ttu-id="b28a0-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="b28a0-121">-AcceptLanguage</span></span>
<span data-ttu-id="b28a0-122">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b28a0-122">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28a0-123">-DefaultProfile</span></span>
<span data-ttu-id="b28a0-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b28a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b28a0-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b28a0-125">-Filter</span></span>
<span data-ttu-id="b28a0-126">Segítségével bizonyos feltételekhez korlátozhatja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="b28a0-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b28a0-127">-InputObject</span></span>
<span data-ttu-id="b28a0-128">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b28a0-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b28a0-129">-Name</span></span>
<span data-ttu-id="b28a0-130">Az Importálás/exportálás feladat neve.</span><span class="sxs-lookup"><span data-stu-id="b28a0-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28a0-131">-ResourceGroupName</span></span>
<span data-ttu-id="b28a0-132">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b28a0-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b28a0-133">-SubscriptionId</span></span>
<span data-ttu-id="b28a0-134">Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b28a0-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-135">-Top</span><span class="sxs-lookup"><span data-stu-id="b28a0-135">-Top</span></span>
<span data-ttu-id="b28a0-136">Egy egész szám, amely megadja, hogy hány feladatot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="b28a0-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="b28a0-137">Az érték nem haladhatja meg az 100-ot.</span><span class="sxs-lookup"><span data-stu-id="b28a0-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28a0-138">CommonParameters</span></span>
<span data-ttu-id="b28a0-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b28a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28a0-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b28a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28a0-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b28a0-141">INPUTS</span></span>

### <span data-ttu-id="b28a0-142">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="b28a0-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="b28a0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b28a0-143">OUTPUTS</span></span>

### <span data-ttu-id="b28a0-144">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="b28a0-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="b28a0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b28a0-145">NOTES</span></span>

<span data-ttu-id="b28a0-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b28a0-146">ALIASES</span></span>

<span data-ttu-id="b28a0-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="b28a0-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b28a0-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b28a0-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b28a0-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b28a0-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b28a0-150">INPUTOBJECT <IImportExportIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b28a0-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b28a0-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b28a0-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b28a0-152">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="b28a0-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="b28a0-153">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="b28a0-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="b28a0-154">Például Nyugat-amerikai vagy westus.</span><span class="sxs-lookup"><span data-stu-id="b28a0-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="b28a0-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b28a0-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="b28a0-156">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b28a0-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="b28a0-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b28a0-157">RELATED LINKS</span></span>

