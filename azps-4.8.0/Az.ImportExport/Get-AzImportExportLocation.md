---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182749"
---
# <span data-ttu-id="854ff-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="854ff-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="854ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="854ff-102">SYNOPSIS</span></span>
<span data-ttu-id="854ff-103">Egy olyan hely részleteit számítja ki, amelybe az importálási vagy exportálási feladathoz kapcsolódó lemezeket szállíthatja.</span><span class="sxs-lookup"><span data-stu-id="854ff-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="854ff-104">A hely egy Azure-terület.</span><span class="sxs-lookup"><span data-stu-id="854ff-104">A location is an Azure region.</span></span>

## <span data-ttu-id="854ff-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="854ff-105">SYNTAX</span></span>

### <span data-ttu-id="854ff-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="854ff-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="854ff-107">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="854ff-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="854ff-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="854ff-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="854ff-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="854ff-109">DESCRIPTION</span></span>
<span data-ttu-id="854ff-110">Egy olyan hely részleteit számítja ki, amelybe az importálási vagy exportálási feladathoz kapcsolódó lemezeket szállíthatja.</span><span class="sxs-lookup"><span data-stu-id="854ff-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="854ff-111">A hely egy Azure-terület.</span><span class="sxs-lookup"><span data-stu-id="854ff-111">A location is an Azure region.</span></span>

## <span data-ttu-id="854ff-112">Példák</span><span class="sxs-lookup"><span data-stu-id="854ff-112">EXAMPLES</span></span>

### <span data-ttu-id="854ff-113">Példa 1: az Azure területi hely minden részletének beolvasása alapértelmezett környezettel</span><span class="sxs-lookup"><span data-stu-id="854ff-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="854ff-114">Ez a parancsmag az Azure region minden helyének részleteit az alapértelmezett környezettel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="854ff-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="854ff-115">2. példa: az Azure területi hely adatainak beolvasása hely neve szerint</span><span class="sxs-lookup"><span data-stu-id="854ff-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="854ff-116">Ez a parancsmag a hely neve alapján kapja meg az Azure régió helyének adatait.</span><span class="sxs-lookup"><span data-stu-id="854ff-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="854ff-117">3. példa: az Azure területi hely adatainak beolvasása identitás szerint</span><span class="sxs-lookup"><span data-stu-id="854ff-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="854ff-118">Ez a parancsmag az Azure régió helyének adatait identitás szerint jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="854ff-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="854ff-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="854ff-119">PARAMETERS</span></span>

### <span data-ttu-id="854ff-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="854ff-120">-AcceptLanguage</span></span>
<span data-ttu-id="854ff-121">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="854ff-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="854ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854ff-122">-DefaultProfile</span></span>
<span data-ttu-id="854ff-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="854ff-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="854ff-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="854ff-124">-InputObject</span></span>
<span data-ttu-id="854ff-125">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="854ff-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="854ff-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="854ff-126">-Name</span></span>
<span data-ttu-id="854ff-127">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="854ff-127">The name of the location.</span></span>
<span data-ttu-id="854ff-128">Például Nyugat-amerikai vagy westus.</span><span class="sxs-lookup"><span data-stu-id="854ff-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="854ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854ff-129">CommonParameters</span></span>
<span data-ttu-id="854ff-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="854ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854ff-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="854ff-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854ff-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="854ff-132">INPUTS</span></span>

### <span data-ttu-id="854ff-133">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="854ff-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="854ff-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="854ff-134">OUTPUTS</span></span>

### <span data-ttu-id="854ff-135">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="854ff-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="854ff-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="854ff-136">NOTES</span></span>

<span data-ttu-id="854ff-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="854ff-137">ALIASES</span></span>

<span data-ttu-id="854ff-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="854ff-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="854ff-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="854ff-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="854ff-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="854ff-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="854ff-141">INPUTOBJECT <IImportExportIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="854ff-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="854ff-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="854ff-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="854ff-143">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="854ff-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="854ff-144">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="854ff-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="854ff-145">Például Nyugat-amerikai vagy westus.</span><span class="sxs-lookup"><span data-stu-id="854ff-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="854ff-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="854ff-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="854ff-147">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="854ff-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="854ff-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="854ff-148">RELATED LINKS</span></span>

