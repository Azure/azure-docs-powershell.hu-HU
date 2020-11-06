---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: ed65956b777ca760be3034f656c25d6c86e5aa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492374"
---
# <span data-ttu-id="25d28-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="25d28-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="25d28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25d28-102">SYNOPSIS</span></span>
<span data-ttu-id="25d28-103">DSC-parancsfájl feltöltése Azure Blob-tárhelyre</span><span class="sxs-lookup"><span data-stu-id="25d28-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25d28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25d28-104">SYNTAX</span></span>

### <span data-ttu-id="25d28-105">UploadArchive (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25d28-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25d28-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="25d28-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25d28-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25d28-107">DESCRIPTION</span></span>
<span data-ttu-id="25d28-108">A **Közzététel-AzureRmVMDscConfiguration** parancsmag az Azure Blob-tárhelyre feltölthet egy kívánt állami konfigurációs (DSC) parancsfájlt, amelyet később a Set-AzureRmVMDscExtension parancsmagot használó Azure virtuális gépekre alkalmazhat.</span><span class="sxs-lookup"><span data-stu-id="25d28-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="25d28-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25d28-109">EXAMPLES</span></span>

### <span data-ttu-id="25d28-110">Példa 1:. zip csomag létrehozása a feltöltés az Azure Storage szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="25d28-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="25d28-111">Ez a parancs létrehoz egy. zip csomagot a megadott parancsfájlhoz és bármely függő erőforrás-modulhoz, és feltölti azt az Azure Storage szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="25d28-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="25d28-112">2. példa: zip-csomag létrehozása és tárolása egy helyi fájlon</span><span class="sxs-lookup"><span data-stu-id="25d28-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="25d28-113">Ez a parancs létrehoz egy. zip csomagot a megadott parancsfájlhoz és bármely függő erőforrás-modulhoz, és a .\MyConfiguration.ps1.zip nevű helyi fájlban tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="25d28-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="25d28-114">3. példa: konfiguráció felvétele az archívumba, majd feltöltés a tárterületre</span><span class="sxs-lookup"><span data-stu-id="25d28-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="25d28-115">Ez a parancs felveszi a konfigurációs archívumba Sample.ps1 nevű konfigurációt az Azure tárhelyre való feltöltéshez, és kihagyja a függő erőforrás-modulokat.</span><span class="sxs-lookup"><span data-stu-id="25d28-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="25d28-116">Példa 4: konfigurációs és konfigurációs adatokat vehet fel az archívumba, majd feltöltheti azt a tárterületre</span><span class="sxs-lookup"><span data-stu-id="25d28-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="25d28-117">Ez a parancs az Azure-tárterületre való feltöltéshez felveszi a SampleData.psd1 nevű Sample.ps1 és konfigurációs adatokat a konfigurációs archívumba.</span><span class="sxs-lookup"><span data-stu-id="25d28-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="25d28-118">Példa 5: konfiguráció, konfigurációs adatok és további tartalmak hozzáadása az archívumhoz, majd feltöltés a tárterületre</span><span class="sxs-lookup"><span data-stu-id="25d28-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="25d28-119">Ez a parancs felveszi a Sample.ps1, a Configuration Data SampleData.psd1 nevű konfigurációt, és további tartalmakat ad a konfigurációs archívumhoz az Azure-tárterületre való feltöltéshez.</span><span class="sxs-lookup"><span data-stu-id="25d28-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="25d28-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25d28-120">PARAMETERS</span></span>

### <span data-ttu-id="25d28-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="25d28-121">-AdditionalPath</span></span>
<span data-ttu-id="25d28-122">A konfigurációs archívumba felvenni kívánt fájl vagy könyvtár elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25d28-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="25d28-123">A rendszer a konfigurációval együtt letölti a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="25d28-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="25d28-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="25d28-125">Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="25d28-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="25d28-126">Ez hozzáadódik a konfigurációs archívumhoz, majd átment a konfigurációs függvényhez.</span><span class="sxs-lookup"><span data-stu-id="25d28-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="25d28-127">A Set-AzureRmVMDscExtension parancsmagon keresztül megadott konfigurációs adatelérési út felülírja.</span><span class="sxs-lookup"><span data-stu-id="25d28-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="25d28-128">-ConfigurationPath</span></span>
<span data-ttu-id="25d28-129">Egy vagy több konfigurációt tartalmazó fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25d28-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="25d28-130">A fájl lehet Windows PowerShell-parancsfájl (. ps1) vagy Windows PowerShell-modul (. psm1).</span><span class="sxs-lookup"><span data-stu-id="25d28-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="25d28-131">-ContainerName</span></span>
<span data-ttu-id="25d28-132">Annak az Azure-tárolónak a nevét adja meg, amelyre a rendszer a konfigurációt feltöltötte.</span><span class="sxs-lookup"><span data-stu-id="25d28-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-133">-Force</span><span class="sxs-lookup"><span data-stu-id="25d28-133">-Force</span></span>
<span data-ttu-id="25d28-134">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="25d28-134">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-135">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="25d28-135">-OutputArchivePath</span></span>
<span data-ttu-id="25d28-136">Annak a helyi. zip fájlnak az elérési útját adja meg, amelybe a konfigurációs archívumot írni kívánja.</span><span class="sxs-lookup"><span data-stu-id="25d28-136">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="25d28-137">Ha ezt a paramétert használja, a konfigurációs parancsfájl nem töltődik fel az Azure Blob-tárolóba.</span><span class="sxs-lookup"><span data-stu-id="25d28-137">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d28-138">-ResourceGroupName</span></span>
<span data-ttu-id="25d28-139">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25d28-139">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-140">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="25d28-140">-SkipDependencyDetection</span></span>
<span data-ttu-id="25d28-141">Azt jelzi, hogy ez a parancsmag kizárja a DSC erőforrás-függőségeket a konfigurációs archívumból.</span><span class="sxs-lookup"><span data-stu-id="25d28-141">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-142">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25d28-142">-StorageAccountName</span></span>
<span data-ttu-id="25d28-143">Annak az Azure-tárterületnek a nevét adja meg, amely a konfigurációs parancsfájlnak a *ContainerName* paraméterben megadott tárolóra való feltöltéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="25d28-143">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-144">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25d28-144">-StorageEndpointSuffix</span></span>
<span data-ttu-id="25d28-145">A tárterület végpontjának utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25d28-145">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25d28-146">-Confirm</span></span>
<span data-ttu-id="25d28-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25d28-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d28-148">-WhatIf</span></span>
<span data-ttu-id="25d28-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25d28-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="25d28-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25d28-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d28-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d28-151">CommonParameters</span></span>
<span data-ttu-id="25d28-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25d28-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d28-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d28-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d28-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25d28-154">INPUTS</span></span>

### <span data-ttu-id="25d28-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="25d28-155">None</span></span>
<span data-ttu-id="25d28-156">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="25d28-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25d28-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25d28-157">OUTPUTS</span></span>

## <span data-ttu-id="25d28-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25d28-158">NOTES</span></span>

## <span data-ttu-id="25d28-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25d28-159">RELATED LINKS</span></span>

[<span data-ttu-id="25d28-160">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="25d28-160">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="25d28-161">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="25d28-161">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="25d28-162">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="25d28-162">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


