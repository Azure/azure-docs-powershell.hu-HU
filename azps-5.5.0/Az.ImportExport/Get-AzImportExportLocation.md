---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209343"
---
# <span data-ttu-id="4e01d-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="4e01d-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="4e01d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e01d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e01d-103">Az importálási vagy exportálási feladathoz társított lemezeket tartalmazó hely adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4e01d-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="4e01d-104">A hely egy Azure-régió.</span><span class="sxs-lookup"><span data-stu-id="4e01d-104">A location is an Azure region.</span></span>

## <span data-ttu-id="4e01d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e01d-105">SYNTAX</span></span>

### <span data-ttu-id="4e01d-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e01d-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e01d-107">Bej.le</span><span class="sxs-lookup"><span data-stu-id="4e01d-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e01d-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e01d-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4e01d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e01d-109">DESCRIPTION</span></span>
<span data-ttu-id="4e01d-110">Az importálási vagy exportálási feladathoz társított lemezeket tartalmazó hely adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4e01d-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="4e01d-111">A hely egy Azure-régió.</span><span class="sxs-lookup"><span data-stu-id="4e01d-111">A location is an Azure region.</span></span>

## <span data-ttu-id="4e01d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e01d-112">EXAMPLES</span></span>

### <span data-ttu-id="4e01d-113">1. példa: Az összes Azure-régió helyének részleteinek lekérte az alapértelmezett környezetben</span><span class="sxs-lookup"><span data-stu-id="4e01d-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="4e01d-114">Ez a parancsmag az összes Azure-régió helyének adatait bekérte az alapértelmezett környezetben.</span><span class="sxs-lookup"><span data-stu-id="4e01d-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="4e01d-115">2. példa: Az Azure-régió helyének részletei hely neve alapján</span><span class="sxs-lookup"><span data-stu-id="4e01d-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="4e01d-116">Ez a parancsmag helynév szerint lekérte az Azure-régió adatait.</span><span class="sxs-lookup"><span data-stu-id="4e01d-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="4e01d-117">3. példa: Azure-régió tartózkodási helyének lekért részletei identitás alapján</span><span class="sxs-lookup"><span data-stu-id="4e01d-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="4e01d-118">Ez a parancsmaglista identitás alapján lekérte az Azure-régió helyének részleteit.</span><span class="sxs-lookup"><span data-stu-id="4e01d-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="4e01d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e01d-119">PARAMETERS</span></span>

### <span data-ttu-id="4e01d-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4e01d-120">-AcceptLanguage</span></span>
<span data-ttu-id="4e01d-121">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4e01d-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4e01d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e01d-122">-DefaultProfile</span></span>
<span data-ttu-id="4e01d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e01d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e01d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e01d-124">-InputObject</span></span>
<span data-ttu-id="4e01d-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4e01d-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e01d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e01d-126">-Name</span></span>
<span data-ttu-id="4e01d-127">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="4e01d-127">The name of the location.</span></span>
<span data-ttu-id="4e01d-128">Ilyen például az Egyesült Államok nyugati és nyugati régiója.</span><span class="sxs-lookup"><span data-stu-id="4e01d-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e01d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e01d-129">CommonParameters</span></span>
<span data-ttu-id="4e01d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e01d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e01d-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e01d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e01d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e01d-132">INPUTS</span></span>

### <span data-ttu-id="4e01d-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="4e01d-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="4e01d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e01d-134">OUTPUTS</span></span>

### <span data-ttu-id="4e01d-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="4e01d-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="4e01d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e01d-136">NOTES</span></span>

<span data-ttu-id="4e01d-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4e01d-137">ALIASES</span></span>

<span data-ttu-id="4e01d-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4e01d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e01d-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4e01d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e01d-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e01d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e01d-141">INPUTOBJECT: <IImportExportIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4e01d-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e01d-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4e01d-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e01d-143">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="4e01d-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="4e01d-144">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="4e01d-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="4e01d-145">Ilyen például az Egyesült Államok nyugati és nyugati régiója.</span><span class="sxs-lookup"><span data-stu-id="4e01d-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="4e01d-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="4e01d-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="4e01d-147">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="4e01d-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="4e01d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e01d-148">RELATED LINKS</span></span>

