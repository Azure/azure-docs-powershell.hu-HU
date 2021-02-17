---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164683"
---
# <span data-ttu-id="7243b-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="7243b-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="7243b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7243b-102">SYNOPSIS</span></span>
<span data-ttu-id="7243b-103">A rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="7243b-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="7243b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7243b-104">SYNTAX</span></span>

### <span data-ttu-id="7243b-105">PathBased (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7243b-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="7243b-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="7243b-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="7243b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7243b-107">DESCRIPTION</span></span>
<span data-ttu-id="7243b-108">Az **Invoke-AzStorageSyncCompatibilityCheck** parancsmag ellenőrzi a rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat. Egy helyi vagy távoli elérési út megadva érvényesíti a rendszert és a fájlnévteret, majd visszaadja a talált kompatibilitási problémákat.</span><span class="sxs-lookup"><span data-stu-id="7243b-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="7243b-109">Rendszerellenőrzések:</span><span class="sxs-lookup"><span data-stu-id="7243b-109">System checks:</span></span>
- <span data-ttu-id="7243b-110">Az operációs rendszer kompatibilitási fájlnévterének ellenőrzése:</span><span class="sxs-lookup"><span data-stu-id="7243b-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="7243b-111">Nem támogatott karakterek</span><span class="sxs-lookup"><span data-stu-id="7243b-111">Unsupported characters</span></span>
- <span data-ttu-id="7243b-112">Maximális fájlméret</span><span class="sxs-lookup"><span data-stu-id="7243b-112">Maximum file size</span></span>
- <span data-ttu-id="7243b-113">Maximális elérési út hossza</span><span class="sxs-lookup"><span data-stu-id="7243b-113">Maximum path length</span></span>
- <span data-ttu-id="7243b-114">Fájl maximális hossza</span><span class="sxs-lookup"><span data-stu-id="7243b-114">Maximum file length</span></span>
- <span data-ttu-id="7243b-115">Az adatkészlet maximális mérete</span><span class="sxs-lookup"><span data-stu-id="7243b-115">Maximum dataset size</span></span>
- <span data-ttu-id="7243b-116">Címtár mélységének maximális mérete</span><span class="sxs-lookup"><span data-stu-id="7243b-116">Maximum directory depth</span></span>

## <span data-ttu-id="7243b-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7243b-117">EXAMPLES</span></span>

### <span data-ttu-id="7243b-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="7243b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="7243b-119">Ez a parancs ellenőrzi a rendszer, valamint a C:\DATA fájlokkal és mappákkal való kompatibilitását.</span><span class="sxs-lookup"><span data-stu-id="7243b-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="7243b-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="7243b-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="7243b-121">Ez a parancs ellenőrzi a C:\DATA fájlokkal és mappákkal való kompatibilitást, de nem ellenőrzi a rendszer kompatibilitását.</span><span class="sxs-lookup"><span data-stu-id="7243b-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="7243b-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="7243b-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="7243b-123">Ez a parancs ellenőrzi a rendszer, valamint a C:\DATA fájlokkal és mappákkal való kompatibilitását, majd az eredményeket CSV-fájlként exportálja a C:\results fájlba.</span><span class="sxs-lookup"><span data-stu-id="7243b-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="7243b-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7243b-124">PARAMETERS</span></span>

### <span data-ttu-id="7243b-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="7243b-125">-ComputerName</span></span>
<span data-ttu-id="7243b-126">Az a számítógép, amely ezt az ellenőrzést végzi.</span><span class="sxs-lookup"><span data-stu-id="7243b-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="7243b-127">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="7243b-127">-Credential</span></span>
<span data-ttu-id="7243b-128">Az érvényesíthető megosztás hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="7243b-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="7243b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7243b-129">-Path</span></span>
<span data-ttu-id="7243b-130">Az érvényesített megosztás UNC elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7243b-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="7243b-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="7243b-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="7243b-132">Ezt a jelölőt beállítva kihagyhatja a fájlnévtér-érvényesítéseket, és csak rendszerérvényesítéseket hajthat végre.</span><span class="sxs-lookup"><span data-stu-id="7243b-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="7243b-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="7243b-133">-SkipSystemChecks</span></span>
<span data-ttu-id="7243b-134">Ezt a jelölőt beállítva kihagyhatja a rendszerérvényesítéseket, és csak a fájlnévtér-érvényesítéseket hajthatja végre.</span><span class="sxs-lookup"><span data-stu-id="7243b-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="7243b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7243b-135">CommonParameters</span></span>
<span data-ttu-id="7243b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7243b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7243b-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7243b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7243b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7243b-138">INPUTS</span></span>

### <span data-ttu-id="7243b-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="7243b-139">None</span></span>

## <span data-ttu-id="7243b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7243b-140">OUTPUTS</span></span>

### <span data-ttu-id="7243b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="7243b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="7243b-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7243b-142">NOTES</span></span>
* <span data-ttu-id="7243b-143">Kulcsszavak: azure, Az, arm, erőforrás, kezelés, tárhelyszinkronizáció, fájlszinkronizáció</span><span class="sxs-lookup"><span data-stu-id="7243b-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="7243b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7243b-144">RELATED LINKS</span></span>
