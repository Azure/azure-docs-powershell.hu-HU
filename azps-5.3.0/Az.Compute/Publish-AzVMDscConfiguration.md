---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465889"
---
# <span data-ttu-id="7c185-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c185-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="7c185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c185-102">SYNOPSIS</span></span>
<span data-ttu-id="7c185-103">Egy DSC-parancsfájlt tölt fel azure blobtárolóba.</span><span class="sxs-lookup"><span data-stu-id="7c185-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="7c185-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c185-104">SYNTAX</span></span>

### <span data-ttu-id="7c185-105">UploadArchive (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c185-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c185-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="7c185-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c185-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c185-107">DESCRIPTION</span></span>
<span data-ttu-id="7c185-108">A **Publish-AzVMDscConfiguration** parancsmag feltölti a kívánt államkonfigurációs (DSC) parancsfájlt az Azure blobtárba, amelyet később a Set-AzVMDscExtension parancsmagot használva lehet azure-Set-AzVMDscExtension alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="7c185-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="7c185-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c185-109">EXAMPLES</span></span>

### <span data-ttu-id="7c185-110">1. példa: .zip csomag létrehozása egy azure-tárhelyre való feltöltéshez</span><span class="sxs-lookup"><span data-stu-id="7c185-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="7c185-111">Ez a parancs létrehoz egy .zip csomagot az adott parancsfájlhoz és a függő erőforrásmodulhoz, és feltölti azt az Azure-tárhelyre.</span><span class="sxs-lookup"><span data-stu-id="7c185-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="7c185-112">2. példa: .zip-csomag létrehozása és tárolása helyi fájlban</span><span class="sxs-lookup"><span data-stu-id="7c185-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="7c185-113">Ez a parancs .zip csomagot hoz létre az adott parancsprogramhoz és a függő erőforrásmodulhoz, és azt a helyi fájlban tárolja, .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="7c185-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="7c185-114">3. példa: Konfiguráció hozzáadása az archívumhoz, majd feltöltése tárhelyre</span><span class="sxs-lookup"><span data-stu-id="7c185-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="7c185-115">Ez a parancs hozzáadja a Sample.ps1 nevű konfigurációt a konfigurációs archívumhoz az Azure-tárhelyre való feltöltéshez, és kihagyja a függő erőforrásmodulokat.</span><span class="sxs-lookup"><span data-stu-id="7c185-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="7c185-116">4. példa: Konfigurációs adatok hozzáadása az archívumhoz, majd feltöltése tárhelyre</span><span class="sxs-lookup"><span data-stu-id="7c185-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="7c185-117">Ez a parancs hozzáadja a Sample.ps1 1-es nevű konfigurációs adatokat és SampleData.psda konfigurációs archívumhoz, és feltölti az Azure-tárhelyre.</span><span class="sxs-lookup"><span data-stu-id="7c185-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="7c185-118">5. példa: Konfiguráció, konfigurációs adatok és további tartalmak hozzáadása az archívumhoz, majd feltöltése tárhelyre</span><span class="sxs-lookup"><span data-stu-id="7c185-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="7c185-119">Ez a parancs hozzáadja a Sample.ps1 nevű konfigurációt, az 1-es SampleData.psdkonfigurációs adatokat és további tartalmakat a konfigurációs archívumhoz az Azure-tárhelyre való feltöltéshez.</span><span class="sxs-lookup"><span data-stu-id="7c185-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="7c185-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c185-120">PARAMETERS</span></span>

### <span data-ttu-id="7c185-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="7c185-121">-AdditionalPath</span></span>
<span data-ttu-id="7c185-122">A konfigurációs archívumba foglalni kívánt fájl vagy címtár elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="7c185-123">A rendszer letölti a virtuális gépre a konfigurációval együtt.</span><span class="sxs-lookup"><span data-stu-id="7c185-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="7c185-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="7c185-125">Egy .psd1 fájl elérési útját adja meg, amely a konfiguráció adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="7c185-126">Ez bekerül a konfigurációs archívumba, majd átkerül a konfigurációs függvénynek.</span><span class="sxs-lookup"><span data-stu-id="7c185-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="7c185-127">A parancsmagon keresztül biztosított konfigurációs adatút felülírja azt Set-AzVMDscExtension parancsmagon keresztül</span><span class="sxs-lookup"><span data-stu-id="7c185-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="7c185-128">-ConfigurationPath</span></span>
<span data-ttu-id="7c185-129">Egy vagy több konfigurációt tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="7c185-130">A fájl lehet Windows PowerShell-parancsfájl (.ps1) vagy Windows PowerShell-modulfájl (.psm1).</span><span class="sxs-lookup"><span data-stu-id="7c185-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7c185-131">-ContainerName</span></span>
<span data-ttu-id="7c185-132">Annak az Azure-tárolónak a neve, amelybe a konfiguráció feltöltődik.</span><span class="sxs-lookup"><span data-stu-id="7c185-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c185-133">-DefaultProfile</span></span>
<span data-ttu-id="7c185-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c185-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-135">-Force</span><span class="sxs-lookup"><span data-stu-id="7c185-135">-Force</span></span>
<span data-ttu-id="7c185-136">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7c185-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c185-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="7c185-137">-OutputArchivePath</span></span>
<span data-ttu-id="7c185-138">Annak a helyi .zip fájlnak az elérési útját adja meg, amelybe a konfigurációs archívumot meg kell írni.</span><span class="sxs-lookup"><span data-stu-id="7c185-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="7c185-139">Ha ezt a paramétert használja, a konfigurációs parancsfájl nem lesz feltöltve az Azure blobtárba.</span><span class="sxs-lookup"><span data-stu-id="7c185-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c185-140">-ResourceGroupName</span></span>
<span data-ttu-id="7c185-141">A tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="7c185-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="7c185-143">Azt jelzi, hogy ez a parancsmag kizárja a DSC-erőforrásfüggőségeket a konfigurációs archívumból.</span><span class="sxs-lookup"><span data-stu-id="7c185-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="7c185-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c185-144">-StorageAccountName</span></span>
<span data-ttu-id="7c185-145">A konfigurációs parancsfájlnak a ContainerName paraméterben megadott tárolóba való feltöltéshez használt *Azure-tárfiók* nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7c185-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="7c185-147">A tárolási végpont utótagját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7c185-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c185-148">-Confirm</span></span>
<span data-ttu-id="7c185-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c185-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c185-150">-WhatIf</span></span>
<span data-ttu-id="7c185-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c185-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c185-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c185-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c185-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c185-153">CommonParameters</span></span>
<span data-ttu-id="7c185-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c185-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c185-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c185-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c185-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c185-156">INPUTS</span></span>

### <span data-ttu-id="7c185-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7c185-157">System.String</span></span>

### <span data-ttu-id="7c185-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7c185-158">System.String[]</span></span>

## <span data-ttu-id="7c185-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c185-159">OUTPUTS</span></span>

### <span data-ttu-id="7c185-160">System.String</span><span class="sxs-lookup"><span data-stu-id="7c185-160">System.String</span></span>

## <span data-ttu-id="7c185-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c185-161">NOTES</span></span>

## <span data-ttu-id="7c185-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c185-162">RELATED LINKS</span></span>

[<span data-ttu-id="7c185-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c185-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="7c185-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c185-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="7c185-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c185-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


