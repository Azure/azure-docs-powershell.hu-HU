---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494545"
---
# <span data-ttu-id="909de-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="909de-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="909de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="909de-102">SYNOPSIS</span></span>
<span data-ttu-id="909de-103">A DSC bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="909de-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="909de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="909de-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="909de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="909de-105">DESCRIPTION</span></span>
<span data-ttu-id="909de-106">A **set-AzureRmVMDscExtension** parancsmag egy erőforráscsoport virtuális gépén a Windows PowerShell által kért állapot-konfigurációs (DSC) kiterjesztést adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="909de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="909de-107">EXAMPLES</span></span>

### <span data-ttu-id="909de-108">1. példa: DSC-bővítmény beállítása</span><span class="sxs-lookup"><span data-stu-id="909de-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="909de-109">Ez a parancs beállítja a VM07 nevű virtuális gép DSC bővítményét, hogy letöltse Sample.ps1.zip a STG nevű tároló fiókból és az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="909de-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="909de-110">A parancs a ConfigName nevű konfigurációt hívja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="909de-111">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzureRmVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="909de-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="909de-112">2. példa: DSC-bővítmény beállítása konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="909de-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="909de-113">Ez a parancs beállítja a VM13 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="909de-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="909de-114">A parancs a ConfigName nevű konfigurációt adja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="909de-115">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzureRmVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="909de-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="909de-116">3. példa: DSC-bővítmény beállítása az automatikus frissítést tartalmazó konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="909de-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="909de-117">Ez a parancs beállítja a VM22 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="909de-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="909de-118">A parancs a ConfigName nevű konfigurációt hívja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="909de-119">Ez a parancs azt is lehetővé teszi, hogy a kiterjesztés-kezelő automatikusan frissítse a legújabb verzióra.</span><span class="sxs-lookup"><span data-stu-id="909de-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="909de-120">A Sample.ps1.zip korábban a **Közzététel-AzureRmVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="909de-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="909de-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="909de-121">PARAMETERS</span></span>

### <span data-ttu-id="909de-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="909de-122">-ArchiveBlobName</span></span>
<span data-ttu-id="909de-123">A Publish-AzureRmVMDscConfiguration parancsmag által korábban feltöltött konfigurációs fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="909de-124">-ArchiveContainerName</span></span>
<span data-ttu-id="909de-125">Annak az Azure-tárolónak a megnevezése, amelyben a konfigurációs Archívum található.</span><span class="sxs-lookup"><span data-stu-id="909de-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909de-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="909de-127">Annak a csoportnak a neve, amely a konfigurációs archívumot tartalmazó tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="909de-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="909de-128">Ez a paraméter nem kötelező, ha a tárolási fiók és a virtuális gép egyaránt ugyanabban az erőforráscsoport-csoportban található.</span><span class="sxs-lookup"><span data-stu-id="909de-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="909de-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="909de-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="909de-130">Megadja a ArchiveBlobName letöltéséhez használt Azure Storage Account nevet.</span><span class="sxs-lookup"><span data-stu-id="909de-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="909de-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="909de-132">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="909de-133">-AutoUpdate</span></span>
<span data-ttu-id="909de-134">A *verzió* paraméter által megadott kiterjesztés-kezelő verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="909de-135">Alapértelmezés szerint az Extension Handler nem frissíti az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="909de-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="909de-136">Használja az *AutoUpdate* paramétert, amellyel engedélyezheti a bővítmények automatikus frissítését a legújabb verzióra, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="909de-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="909de-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="909de-137">-ConfigurationArgument</span></span>
<span data-ttu-id="909de-138">A konfigurációs függvény argumentumait tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="909de-139">-ConfigurationData</span></span>
<span data-ttu-id="909de-140">Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="909de-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="909de-141">-ConfigurationName</span></span>
<span data-ttu-id="909de-142">Annak a konfigurációnak a nevét adja meg, amelyre a DSC bővítmény hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="909de-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="909de-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="909de-143">-DataCollection</span></span>
<span data-ttu-id="909de-144">Az adatgyűjtési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-144">Specifies the data collection type.</span></span>
<span data-ttu-id="909de-145">A paraméter elfogadható értékei a következők: engedélyezés és letiltás.</span><span class="sxs-lookup"><span data-stu-id="909de-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-146">-Force</span><span class="sxs-lookup"><span data-stu-id="909de-146">-Force</span></span>
<span data-ttu-id="909de-147">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="909de-147">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="909de-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="909de-148">-Location</span></span>
<span data-ttu-id="909de-149">Az erőforrás-kiterjesztés elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="909de-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="909de-150">-Name</span></span>
<span data-ttu-id="909de-151">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="909de-152">Az alapértelmezett érték a Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="909de-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="909de-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909de-153">-ResourceGroupName</span></span>
<span data-ttu-id="909de-154">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-154">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-155">-Verzió</span><span class="sxs-lookup"><span data-stu-id="909de-155">-Version</span></span>
<span data-ttu-id="909de-156">Annak a DSC-bővítménynek a verziószámát adja meg, amely a Set-AzureRmVMDscExtension alkalmazza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="909de-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="909de-157">-VMName</span></span>
<span data-ttu-id="909de-158">Annak a virtuális gépnek a neve, ahol a DSC Extension Handler telepítve van.</span><span class="sxs-lookup"><span data-stu-id="909de-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="909de-159">-WmfVersion</span></span>
<span data-ttu-id="909de-160">A WMF-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="909de-160">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909de-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="909de-161">-Confirm</span></span>
<span data-ttu-id="909de-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="909de-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="909de-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="909de-163">-WhatIf</span></span>
<span data-ttu-id="909de-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="909de-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="909de-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="909de-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="909de-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909de-166">CommonParameters</span></span>
<span data-ttu-id="909de-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="909de-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909de-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="909de-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909de-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="909de-169">INPUTS</span></span>

### <span data-ttu-id="909de-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="909de-170">None</span></span>
<span data-ttu-id="909de-171">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="909de-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="909de-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="909de-172">OUTPUTS</span></span>

## <span data-ttu-id="909de-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="909de-173">NOTES</span></span>

## <span data-ttu-id="909de-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="909de-174">RELATED LINKS</span></span>

[<span data-ttu-id="909de-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="909de-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="909de-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="909de-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="909de-177">Közzététel – AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="909de-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


