---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498127"
---
# <span data-ttu-id="61abe-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="61abe-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="61abe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61abe-102">SYNOPSIS</span></span>
<span data-ttu-id="61abe-103">Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.</span><span class="sxs-lookup"><span data-stu-id="61abe-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61abe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61abe-104">SYNTAX</span></span>

### <span data-ttu-id="61abe-105">PathBased (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61abe-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="61abe-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="61abe-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="61abe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="61abe-107">DESCRIPTION</span></span>
<span data-ttu-id="61abe-108">A **meghívó-AzureRmStorageSyncCompatibilityCheck** parancsmag a rendszer és az Azure-fájlok szinkronizálása közötti esetleges kompatibilitási problémákat ellenőrzi. Helyi vagy távoli elérési út esetén az érvényes beállításokat a rendszer és a fájl névtérben hajtja végre, majd a talált kompatibilitási problémákat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="61abe-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="61abe-109">Rendszerellenőrzések:</span><span class="sxs-lookup"><span data-stu-id="61abe-109">System checks:</span></span>
- <span data-ttu-id="61abe-110">Az operációs rendszer kompatibilitási fájljának névtér-ellenőrzése:</span><span class="sxs-lookup"><span data-stu-id="61abe-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="61abe-111">Nem támogatott karakterek</span><span class="sxs-lookup"><span data-stu-id="61abe-111">Unsupported characters</span></span>
- <span data-ttu-id="61abe-112">Maximális fájlméret</span><span class="sxs-lookup"><span data-stu-id="61abe-112">Maximum file size</span></span>
- <span data-ttu-id="61abe-113">Maximális útvonal hossza</span><span class="sxs-lookup"><span data-stu-id="61abe-113">Maximum path length</span></span>
- <span data-ttu-id="61abe-114">Fájl maximális hossza</span><span class="sxs-lookup"><span data-stu-id="61abe-114">Maximum file length</span></span>
- <span data-ttu-id="61abe-115">Adatkészlet maximális mérete</span><span class="sxs-lookup"><span data-stu-id="61abe-115">Maximum dataset size</span></span>
- <span data-ttu-id="61abe-116">A könyvtár maximális mélysége</span><span class="sxs-lookup"><span data-stu-id="61abe-116">Maximum directory depth</span></span>

## <span data-ttu-id="61abe-117">Példák</span><span class="sxs-lookup"><span data-stu-id="61abe-117">EXAMPLES</span></span>

### <span data-ttu-id="61abe-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="61abe-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="61abe-119">Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\DATA.-ban.</span><span class="sxs-lookup"><span data-stu-id="61abe-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="61abe-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="61abe-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="61abe-121">Ez a parancs ellenőrzi a fájlok és mappák kompatibilitását a C:\ADATOK-ban, de nem végez rendszerkompatibilitás-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="61abe-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="61abe-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="61abe-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="61abe-123">Ez a parancs ellenőrzi a rendszer és a fájlok és mappák kompatibilitását a C:\ADATOK-ban, majd CSV-fájlként exportálja az eredményeket a C:\results.</span><span class="sxs-lookup"><span data-stu-id="61abe-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="61abe-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61abe-124">PARAMETERS</span></span>

### <span data-ttu-id="61abe-125">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="61abe-125">-ComputerName</span></span>
<span data-ttu-id="61abe-126">Az a számítógép, amelyen a beadást végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="61abe-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="61abe-127">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="61abe-127">-Credential</span></span>
<span data-ttu-id="61abe-128">Az érvényesíteni kívánt megosztáshoz tartozó hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="61abe-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="61abe-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="61abe-129">-Path</span></span>
<span data-ttu-id="61abe-130">Az érvényesíteni kívánt megosztás UNC-elérési útja.</span><span class="sxs-lookup"><span data-stu-id="61abe-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="61abe-131">-Quiet (csendes)</span><span class="sxs-lookup"><span data-stu-id="61abe-131">-Quiet</span></span>
<span data-ttu-id="61abe-132">Letiltja a kimeneti jelentés írását a konzolra.</span><span class="sxs-lookup"><span data-stu-id="61abe-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="61abe-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="61abe-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="61abe-134">Ezt a jelölőt úgy állíthatja be, hogy kihagyja a fájl névterének érvényességét, és csak a rendszerérvényességet végezze</span><span class="sxs-lookup"><span data-stu-id="61abe-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="61abe-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="61abe-135">-SkipSystemChecks</span></span>
<span data-ttu-id="61abe-136">Ezt a jelölőt beállíthatja a rendszerérvényességek kihagyására, és csak a fájl névterének érvényességét végezze el.</span><span class="sxs-lookup"><span data-stu-id="61abe-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="61abe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61abe-137">CommonParameters</span></span>
<span data-ttu-id="61abe-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61abe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61abe-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61abe-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61abe-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61abe-140">INPUTS</span></span>

### <span data-ttu-id="61abe-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="61abe-141">None</span></span>

## <span data-ttu-id="61abe-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61abe-142">OUTPUTS</span></span>

### <span data-ttu-id="61abe-143">Microsoft. Azure. Command. StorageSync. Értékelés. modellek. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="61abe-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="61abe-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61abe-144">NOTES</span></span>
* <span data-ttu-id="61abe-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="61abe-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="61abe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61abe-146">RELATED LINKS</span></span>
