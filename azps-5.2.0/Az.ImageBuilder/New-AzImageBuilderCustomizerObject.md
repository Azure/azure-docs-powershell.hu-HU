---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343109"
---
# <span data-ttu-id="c9c9b-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="c9c9b-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="c9c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c9b-103">A kép testreszabásának egy egysége</span><span class="sxs-lookup"><span data-stu-id="c9c9b-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="c9c9b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9c9b-104">SYNTAX</span></span>

### <span data-ttu-id="c9c9b-105">ShellCustomizer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9c9b-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c9b-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c9b-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c9b-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c9b-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c9c9b-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9c9b-110">DESCRIPTION</span></span>
<span data-ttu-id="c9c9b-111">A kép testreszabásának egy egysége</span><span class="sxs-lookup"><span data-stu-id="c9c9b-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="c9c9b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9c9b-112">EXAMPLES</span></span>

### <span data-ttu-id="c9c9b-113">1. példa: Windows Update customizer létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9c9b-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="c9c9b-114">Ez a parancs létrehoz egy Windows Update-testre szabót.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="c9c9b-115">2. példa: Fájl testre szabó létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9c9b-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="c9c9b-116">Ez a parancs egy fájl testre szabót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="c9c9b-117">3. példa: PowerShell-testre szabó létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9c9b-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="c9c9b-118">Ez a parancs powershell-testre szabót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="c9c9b-119">4. példa: Újraindítás testre szabó létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9c9b-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="c9c9b-120">Ez a parancs újraindítási testre szabót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="c9c9b-121">5. példa: Rendszerhéj-testre szabó létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9c9b-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="c9c9b-122">Ez a parancs létrehoz egy rendszerhéj-testre szabót.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="c9c9b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9c9b-123">PARAMETERS</span></span>

### <span data-ttu-id="c9c9b-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="c9c9b-124">-CustomizerName</span></span>
<span data-ttu-id="c9c9b-125">Rövid név, hogy kontextust nyújtson arról, hogy mit tesz ez a testreszabási lépés.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="c9c9b-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="c9c9b-126">-Destination</span></span>
<span data-ttu-id="c9c9b-127">A fájl abszolút elérési útja (a már létrehozott beágyazott címtárszerkezetekkel), ahol a fájl (a sourceUri fájlból) feltöltődik a VM-be.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="c9c9b-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-128">-FileCustomizer</span></span>
<span data-ttu-id="c9c9b-129">Fájlok feltöltése virtuális gépekre (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="c9c9b-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="c9c9b-130">A Packer fájl kiépítési szolgáltatásának felel meg.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="c9c9b-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="c9c9b-131">-Filter</span></span>
<span data-ttu-id="c9c9b-132">Szűrők tömbje az alkalmazni kívánt frissítések kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="c9c9b-133">Kihagyja vagy megadja az üres tömböt az alapértelmezett (nincs szűrő) beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="c9c9b-134">A fenti hivatkozásra kattintva példákat és részletes leírást talál erről a mezőről.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="c9c9b-135">-Beágyazott</span><span class="sxs-lookup"><span data-stu-id="c9c9b-135">-Inline</span></span>
<span data-ttu-id="c9c9b-136">Futtatandó parancshéj-tömb.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="c9c9b-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="c9c9b-138">A megadott PowerShellt futtatja a virtuális gépen (Windows).</span><span class="sxs-lookup"><span data-stu-id="c9c9b-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="c9c9b-139">Megfelel a Packer powershell-kiépítési szolgáltatásának.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="c9c9b-140">Pontosan az egyik "scriptUri" vagy "beágyazott" meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="c9c9b-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="c9c9b-141">-RestartCheckCommand</span></span>
<span data-ttu-id="c9c9b-142">Command to check if restart succeeded [Default: ''].</span><span class="sxs-lookup"><span data-stu-id="c9c9b-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="c9c9b-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="c9c9b-143">-RestartCommand</span></span>
<span data-ttu-id="c9c9b-144">Az újraindítás végrehajtásához szükséges parancs [Alapértelmezett: 'leállítás /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="c9c9b-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="c9c9b-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-145">-RestartCustomizer</span></span>
<span data-ttu-id="c9c9b-146">Újraindítja a vm-et, és várja, hogy újra elérhető lesz (Windows).</span><span class="sxs-lookup"><span data-stu-id="c9c9b-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="c9c9b-147">A Packer windows-restart kiépítési eszközének felel meg.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="c9c9b-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="c9c9b-148">-RestartTimeout</span></span>
<span data-ttu-id="c9c9b-149">Adja meg a szám és az egység karakterláncaként megadott újraindítási időtúllépést, például "5 m" (5 perc) vagy "2h" (2 óra) [Alapértelmezett: '5m'].</span><span class="sxs-lookup"><span data-stu-id="c9c9b-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="c9c9b-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="c9c9b-150">-RunElevated</span></span>
<span data-ttu-id="c9c9b-151">Ha meg van adva, a PowerShell-parancsfájl magasabb szintű jogosultságokkal fog futni.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="c9c9b-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="c9c9b-152">-ScriptUri</span></span>
<span data-ttu-id="c9c9b-153">A testreszabáshoz futtatott rendszerhéj-parancsfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="c9c9b-154">Ez lehet egy github-hivatkozás, Azure Storage-hoz elérhető SAS URI stb.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="c9c9b-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="c9c9b-155">-SearchCriterion</span></span>
<span data-ttu-id="c9c9b-156">A frissítések keresésére vonatkozó feltételek.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-156">Criteria to search updates.</span></span>
<span data-ttu-id="c9c9b-157">Kihagyja vagy megadja az alapértelmezett értékhez használni kívánt üres karakterláncot (az összesben keres).</span><span class="sxs-lookup"><span data-stu-id="c9c9b-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="c9c9b-158">A fenti hivatkozásra kattintva példákat és részletes leírást talál erről a mezőről.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="c9c9b-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="c9c9b-159">-Sha256Checksum</span></span>
<span data-ttu-id="c9c9b-160">Sha256 checksum of the shell script provided in the scriptUri field.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="c9c9b-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-161">-ShellCustomizer</span></span>
<span data-ttu-id="c9c9b-162">Egy rendszerhéj-parancsfájlt futtat a testreszabási fázis alatt (Linux).</span><span class="sxs-lookup"><span data-stu-id="c9c9b-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="c9c9b-163">Megfelel a Packer rendszerhéj-kiépítésnek.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="c9c9b-164">Pontosan az egyik "scriptUri" vagy "beágyazott" meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="c9c9b-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="c9c9b-165">-SourceUri</span></span>
<span data-ttu-id="c9c9b-166">A virtuális gép testreszabására feltöltni kívánt fájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="c9c9b-167">Ez lehet egy github-hivatkozás, Azure Storage-hoz elérhető SAS URI stb.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="c9c9b-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="c9c9b-168">-UpdateLimit</span></span>
<span data-ttu-id="c9c9b-169">Az egyszerre alkalmazandó frissítések maximális száma.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="c9c9b-170">Az alapértelmezett érték (1000) használata esetén ne adja meg a 0 értéket, vagy adja meg a 0 értéket.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="c9c9b-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="c9c9b-171">-ValidExitCode</span></span>
<span data-ttu-id="c9c9b-172">A PowerShell-parancsprogram érvényes kilépési kódjai.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="c9c9b-173">[Alapértelmezett: 0].</span><span class="sxs-lookup"><span data-stu-id="c9c9b-173">[Default: 0].</span></span>

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

### <span data-ttu-id="c9c9b-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="c9c9b-175">Telepíti a Windows-frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-175">Installs Windows Updates.</span></span>
<span data-ttu-id="c9c9b-176">Megfelel a Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="c9c9b-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="c9c9b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c9b-177">CommonParameters</span></span>
<span data-ttu-id="c9c9b-178">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c9b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c9b-179">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9c9b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c9b-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9c9b-180">INPUTS</span></span>

## <span data-ttu-id="c9c9b-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c9b-181">OUTPUTS</span></span>

### <span data-ttu-id="c9c9b-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="c9c9b-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="c9c9b-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9c9b-183">NOTES</span></span>

<span data-ttu-id="c9c9b-184">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c9c9b-184">ALIASES</span></span>

## <span data-ttu-id="c9c9b-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c9b-185">RELATED LINKS</span></span>

