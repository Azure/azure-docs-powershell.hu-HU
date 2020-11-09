---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302915"
---
# <span data-ttu-id="8165b-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="8165b-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="8165b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8165b-102">SYNOPSIS</span></span>
<span data-ttu-id="8165b-103">Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.</span><span class="sxs-lookup"><span data-stu-id="8165b-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="8165b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8165b-104">SYNTAX</span></span>

### <span data-ttu-id="8165b-105">PathBased (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8165b-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="8165b-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="8165b-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="8165b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8165b-107">DESCRIPTION</span></span>
<span data-ttu-id="8165b-108">A **meghívó-AzStorageSyncCompatibilityCheck** parancsmag a rendszer és az Azure-fájlok szinkronizálása közötti esetleges kompatibilitási problémákat ellenőrzi. Helyi vagy távoli elérési út esetén az érvényes beállításokat a rendszer és a fájl névtérben hajtja végre, majd a talált kompatibilitási problémákat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8165b-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="8165b-109">Rendszerellenőrzések:</span><span class="sxs-lookup"><span data-stu-id="8165b-109">System checks:</span></span>
- <span data-ttu-id="8165b-110">Az operációs rendszer kompatibilitási fájljának névtér-ellenőrzése:</span><span class="sxs-lookup"><span data-stu-id="8165b-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="8165b-111">Nem támogatott karakterek</span><span class="sxs-lookup"><span data-stu-id="8165b-111">Unsupported characters</span></span>
- <span data-ttu-id="8165b-112">Maximális fájlméret</span><span class="sxs-lookup"><span data-stu-id="8165b-112">Maximum file size</span></span>
- <span data-ttu-id="8165b-113">Maximális útvonal hossza</span><span class="sxs-lookup"><span data-stu-id="8165b-113">Maximum path length</span></span>
- <span data-ttu-id="8165b-114">Fájl maximális hossza</span><span class="sxs-lookup"><span data-stu-id="8165b-114">Maximum file length</span></span>
- <span data-ttu-id="8165b-115">Adatkészlet maximális mérete</span><span class="sxs-lookup"><span data-stu-id="8165b-115">Maximum dataset size</span></span>
- <span data-ttu-id="8165b-116">A könyvtár maximális mélysége</span><span class="sxs-lookup"><span data-stu-id="8165b-116">Maximum directory depth</span></span>

## <span data-ttu-id="8165b-117">Példák</span><span class="sxs-lookup"><span data-stu-id="8165b-117">EXAMPLES</span></span>

### <span data-ttu-id="8165b-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8165b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="8165b-119">Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\DATA.-ban.</span><span class="sxs-lookup"><span data-stu-id="8165b-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="8165b-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="8165b-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="8165b-121">Ez a parancs ellenőrzi a fájlok és mappák kompatibilitását a C:\ADATOK-ban, de nem végez rendszerkompatibilitás-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="8165b-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="8165b-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="8165b-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="8165b-123">Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\ADATOK-ban, majd CSV-fájlként exportálja az eredményeket a C:\results.</span><span class="sxs-lookup"><span data-stu-id="8165b-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="8165b-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8165b-124">PARAMETERS</span></span>

### <span data-ttu-id="8165b-125">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="8165b-125">-ComputerName</span></span>
<span data-ttu-id="8165b-126">Az a számítógép, amelyen a beadást végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="8165b-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165b-127">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="8165b-127">-Credential</span></span>
<span data-ttu-id="8165b-128">Az érvényesíteni kívánt megosztáshoz tartozó hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8165b-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165b-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8165b-129">-Path</span></span>
<span data-ttu-id="8165b-130">Az érvényesíteni kívánt megosztás UNC-elérési útja.</span><span class="sxs-lookup"><span data-stu-id="8165b-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165b-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="8165b-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="8165b-132">Ezt a jelölőt úgy állíthatja be, hogy kihagyja a fájl névterének érvényességét, és csak a rendszerérvényességet végezze</span><span class="sxs-lookup"><span data-stu-id="8165b-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8165b-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="8165b-133">-SkipSystemChecks</span></span>
<span data-ttu-id="8165b-134">Ezt a jelölőt beállíthatja a rendszerérvényességek kihagyására, és csak a fájl névterének érvényességét végezze el.</span><span class="sxs-lookup"><span data-stu-id="8165b-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="8165b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8165b-135">CommonParameters</span></span>
<span data-ttu-id="8165b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8165b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8165b-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8165b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8165b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8165b-138">INPUTS</span></span>

### <span data-ttu-id="8165b-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="8165b-139">None</span></span>

## <span data-ttu-id="8165b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8165b-140">OUTPUTS</span></span>

### <span data-ttu-id="8165b-141">Microsoft. Azure. Command. StorageSync. Értékelés. modellek. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="8165b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="8165b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8165b-142">NOTES</span></span>
* <span data-ttu-id="8165b-143">Kulcsszavak: Azure, az, kar, erőforrás, kezelés, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="8165b-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="8165b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8165b-144">RELATED LINKS</span></span>
