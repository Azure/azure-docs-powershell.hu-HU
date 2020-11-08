---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018087"
---
# <span data-ttu-id="7fda8-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="7fda8-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="7fda8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fda8-102">SYNOPSIS</span></span>
<span data-ttu-id="7fda8-103">A kép testreszabási egységét ismerteti</span><span class="sxs-lookup"><span data-stu-id="7fda8-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="7fda8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fda8-104">SYNTAX</span></span>

### <span data-ttu-id="7fda8-105">ShellCustomizer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fda8-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fda8-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fda8-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fda8-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="7fda8-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7fda8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fda8-110">DESCRIPTION</span></span>
<span data-ttu-id="7fda8-111">A kép testreszabási egységét ismerteti</span><span class="sxs-lookup"><span data-stu-id="7fda8-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="7fda8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7fda8-112">EXAMPLES</span></span>

### <span data-ttu-id="7fda8-113">Példa 1: Windows Update-Testreszabás létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fda8-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="7fda8-114">Ez a parancs létrehoz egy Windows Update-testre szabható személyt.</span><span class="sxs-lookup"><span data-stu-id="7fda8-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="7fda8-115">2. példa: fájl-testreszabási beállítások létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fda8-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="7fda8-116">Ezzel a paranccsal létrehozhatja a fájl testreszabásait.</span><span class="sxs-lookup"><span data-stu-id="7fda8-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="7fda8-117">3. példa: PowerShell-Testreszabás létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fda8-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="7fda8-118">Ez a parancs létrehoz egy PowerShell-testre szabható személyt.</span><span class="sxs-lookup"><span data-stu-id="7fda8-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="7fda8-119">4. példa: újraindítási Testreszabás létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fda8-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="7fda8-120">Ez a parancs létrehoz egy újraindítási testreszabást.</span><span class="sxs-lookup"><span data-stu-id="7fda8-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="7fda8-121">Példa 5: rendszerhéj-Testreszabás létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fda8-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="7fda8-122">Ez a parancs létrehoz egy rendszerhéj-testreszabó.</span><span class="sxs-lookup"><span data-stu-id="7fda8-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="7fda8-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fda8-123">PARAMETERS</span></span>

### <span data-ttu-id="7fda8-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="7fda8-124">-CustomizerName</span></span>
<span data-ttu-id="7fda8-125">Felhasználóbarát név: Ez a testreszabási lépés a környezet számára elérhető.</span><span class="sxs-lookup"><span data-stu-id="7fda8-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-126">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="7fda8-126">-Destination</span></span>
<span data-ttu-id="7fda8-127">A fájl abszolút elérési útja (beágyazott címtár-szerkezetekkel már létrehozva), ahol a fájlt (a sourceUri-ról) a VM-be fogja feltölteni.</span><span class="sxs-lookup"><span data-stu-id="7fda8-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-128">-FileCustomizer</span></span>
<span data-ttu-id="7fda8-129">Fájlok feltöltése VMs-be (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="7fda8-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="7fda8-130">A csomagoló-fájl kiépítési típusának felel meg.</span><span class="sxs-lookup"><span data-stu-id="7fda8-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-131">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="7fda8-131">-Filter</span></span>
<span data-ttu-id="7fda8-132">Az alkalmazni kívánt frissítések kiválasztására szolgáló szűrők tömbje</span><span class="sxs-lookup"><span data-stu-id="7fda8-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="7fda8-133">Az alapértelmezett (nincs szűrő) beállítás használatához hagyja üresen vagy adja meg az üres tömböt.</span><span class="sxs-lookup"><span data-stu-id="7fda8-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="7fda8-134">Lásd a fenti hivatkozás hivatkozását, és a mező részletes leírását.</span><span class="sxs-lookup"><span data-stu-id="7fda8-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-135">– Szövegközi</span><span class="sxs-lookup"><span data-stu-id="7fda8-135">-Inline</span></span>
<span data-ttu-id="7fda8-136">A végrehajtandó rendszerhéj-parancsok tömbje.</span><span class="sxs-lookup"><span data-stu-id="7fda8-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="7fda8-138">Futtatja a megadott PowerShellt a VM-ben (Windows).</span><span class="sxs-lookup"><span data-stu-id="7fda8-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="7fda8-139">A csomagoló PowerShell-kiépítési csomagnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="7fda8-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="7fda8-140">Pontosan az egyik "scriptUri" vagy "szövegközi" érték van megadva.</span><span class="sxs-lookup"><span data-stu-id="7fda8-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="7fda8-141">-RestartCheckCommand</span></span>
<span data-ttu-id="7fda8-142">Annak ellenőrzése, hogy az újraindítás sikerült-e: [alapértelmezett: ' '].</span><span class="sxs-lookup"><span data-stu-id="7fda8-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="7fda8-143">-RestartCommand</span></span>
<span data-ttu-id="7fda8-144">Az újraindítás végrehajtását szolgáló parancs [alapértelmezett: ' shutdown/r/f/t 0/c csomagoló újraindítása ']</span><span class="sxs-lookup"><span data-stu-id="7fda8-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-145">-RestartCustomizer</span></span>
<span data-ttu-id="7fda8-146">Újraindítja a VM-et, és várja, hogy térjen vissza az internethez (Windows).</span><span class="sxs-lookup"><span data-stu-id="7fda8-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="7fda8-147">A Windows-csomaghoz tartozó Windows – indítsa újra a kiépítő lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="7fda8-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="7fda8-148">-RestartTimeout</span></span>
<span data-ttu-id="7fda8-149">Újraindítási időkorlát a magnitúdó és az egység, például ' 5m ' (5 perc) vagy ' 2H ' (2 óra) [alapértelmezett: ' 5m '] karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="7fda8-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="7fda8-150">-RunElevated</span></span>
<span data-ttu-id="7fda8-151">Ha meg van adva, a PowerShell-parancsfájl magasabb szintű jogosultságokkal fog futni.</span><span class="sxs-lookup"><span data-stu-id="7fda8-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="7fda8-152">-ScriptUri</span></span>
<span data-ttu-id="7fda8-153">A testreszabáshoz futtatandó rendszerhéj-parancsfájl URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7fda8-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="7fda8-154">Ez lehet egy GitHub hivatkozás, az Azure-tárterületet tartalmazó SAS-URI stb.</span><span class="sxs-lookup"><span data-stu-id="7fda8-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="7fda8-155">-SearchCriterion</span></span>
<span data-ttu-id="7fda8-156">A frissítések keresési kritériumai</span><span class="sxs-lookup"><span data-stu-id="7fda8-156">Criteria to search updates.</span></span>
<span data-ttu-id="7fda8-157">Üres karakterlánc kihagyása vagy megadása az alapértelmezett (az összes keresése) használatához.</span><span class="sxs-lookup"><span data-stu-id="7fda8-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="7fda8-158">Lásd a fenti hivatkozás hivatkozását, és a mező részletes leírását.</span><span class="sxs-lookup"><span data-stu-id="7fda8-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="7fda8-159">-Sha256Checksum</span></span>
<span data-ttu-id="7fda8-160">A scriptUri mezőben megadott rendszerhéj-parancsfájl SHA256 ellenőrzőösszege.</span><span class="sxs-lookup"><span data-stu-id="7fda8-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-161">-ShellCustomizer</span></span>
<span data-ttu-id="7fda8-162">Rendszerhéj-parancsfájl futtatása a testreszabási fázis (Linux) során.</span><span class="sxs-lookup"><span data-stu-id="7fda8-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="7fda8-163">A csomagoló rendszerhéj-kiépítés típusának felel meg.</span><span class="sxs-lookup"><span data-stu-id="7fda8-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="7fda8-164">Pontosan az egyik "scriptUri" vagy "szövegközi" érték van megadva.</span><span class="sxs-lookup"><span data-stu-id="7fda8-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7fda8-165">-SourceUri</span></span>
<span data-ttu-id="7fda8-166">A VM testreszabásához feltöltött fájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="7fda8-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="7fda8-167">Ez lehet egy GitHub hivatkozás, az Azure-tárterületet tartalmazó SAS-URI stb.</span><span class="sxs-lookup"><span data-stu-id="7fda8-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="7fda8-168">-UpdateLimit</span></span>
<span data-ttu-id="7fda8-169">A módosítások maximális száma egyszerre érvényes.</span><span class="sxs-lookup"><span data-stu-id="7fda8-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="7fda8-170">Az alapértelmezett (1000) beállításnál hagyja el vagy adja meg a 0 értéket.</span><span class="sxs-lookup"><span data-stu-id="7fda8-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="7fda8-171">-ValidExitCode</span></span>
<span data-ttu-id="7fda8-172">A PowerShell-parancsfájl érvényes kilépési kódjai.</span><span class="sxs-lookup"><span data-stu-id="7fda8-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="7fda8-173">[Alapértelmezett: 0].</span><span class="sxs-lookup"><span data-stu-id="7fda8-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="7fda8-175">Telepíti a Windows-frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="7fda8-175">Installs Windows Updates.</span></span>
<span data-ttu-id="7fda8-176">A Windows Update-kiépítő csomag ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="7fda8-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fda8-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fda8-177">CommonParameters</span></span>
<span data-ttu-id="7fda8-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fda8-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fda8-179">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7fda8-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fda8-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fda8-180">INPUTS</span></span>

## <span data-ttu-id="7fda8-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fda8-181">OUTPUTS</span></span>

### <span data-ttu-id="7fda8-182">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="7fda8-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="7fda8-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fda8-183">NOTES</span></span>

<span data-ttu-id="7fda8-184">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7fda8-184">ALIASES</span></span>

## <span data-ttu-id="7fda8-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fda8-185">RELATED LINKS</span></span>

