---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 75cd5e76fe4ebce1479525aba2c36e6741b6094b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671227"
---
# <span data-ttu-id="d51ac-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d51ac-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="d51ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d51ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d51ac-103">A DSC bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d51ac-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d51ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d51ac-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d51ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d51ac-105">DESCRIPTION</span></span>
<span data-ttu-id="d51ac-106">A **set-AzVMDscExtension** parancsmag egy erőforráscsoport virtuális gépén a Windows PowerShell által kért állapot-konfigurációs (DSC) kiterjesztést adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="d51ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d51ac-107">EXAMPLES</span></span>

### <span data-ttu-id="d51ac-108">1. példa: DSC-bővítmény beállítása</span><span class="sxs-lookup"><span data-stu-id="d51ac-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d51ac-109">Ez a parancs beállítja a VM07 nevű virtuális gép DSC bővítményét, hogy letöltse Sample.ps1.zip a STG nevű tároló fiókból és az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d51ac-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="d51ac-110">A parancs a ConfigName nevű konfigurációt hívja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="d51ac-111">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="d51ac-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d51ac-112">2. példa: DSC-bővítmény beállítása konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="d51ac-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d51ac-113">Ez a parancs beállítja a VM13 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d51ac-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d51ac-114">A parancs a ConfigName nevű konfigurációt adja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d51ac-115">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="d51ac-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d51ac-116">3. példa: DSC-bővítmény beállítása az automatikus frissítést tartalmazó konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="d51ac-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="d51ac-117">Ez a parancs beállítja a VM22 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d51ac-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d51ac-118">A parancs a ConfigName nevű konfigurációt hívja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d51ac-119">Ez a parancs azt is lehetővé teszi, hogy a kiterjesztés-kezelő automatikusan frissítse a legújabb verzióra.</span><span class="sxs-lookup"><span data-stu-id="d51ac-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="d51ac-120">A Sample.ps1.zip korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="d51ac-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="d51ac-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d51ac-121">PARAMETERS</span></span>

### <span data-ttu-id="d51ac-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="d51ac-122">-ArchiveBlobName</span></span>
<span data-ttu-id="d51ac-123">A Publish-AzVMDscConfiguration parancsmag által korábban feltöltött konfigurációs fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="d51ac-124">-ArchiveContainerName</span></span>
<span data-ttu-id="d51ac-125">Annak az Azure-tárolónak a megnevezése, amelyben a konfigurációs Archívum található.</span><span class="sxs-lookup"><span data-stu-id="d51ac-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51ac-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="d51ac-127">Annak a csoportnak a neve, amely a konfigurációs archívumot tartalmazó tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d51ac-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="d51ac-128">Ez a paraméter nem kötelező, ha a tárolási fiók és a virtuális gép egyaránt ugyanabban az erőforráscsoport-csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d51ac-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="d51ac-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d51ac-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="d51ac-130">Megadja a ArchiveBlobName letöltéséhez használt Azure Storage Account nevet.</span><span class="sxs-lookup"><span data-stu-id="d51ac-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d51ac-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="d51ac-132">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d51ac-133">-AutoUpdate</span></span>
<span data-ttu-id="d51ac-134">A *verzió* paraméter által megadott kiterjesztés-kezelő verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="d51ac-135">Alapértelmezés szerint az Extension Handler nem frissíti az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="d51ac-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="d51ac-136">Használja az *AutoUpdate* paramétert, amellyel engedélyezheti a bővítmények automatikus frissítését a legújabb verzióra, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="d51ac-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="d51ac-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="d51ac-137">-ConfigurationArgument</span></span>
<span data-ttu-id="d51ac-138">A konfigurációs függvény argumentumait tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d51ac-139">-ConfigurationData</span></span>
<span data-ttu-id="d51ac-140">Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="d51ac-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d51ac-141">-ConfigurationName</span></span>
<span data-ttu-id="d51ac-142">Annak a konfigurációnak a nevét adja meg, amelyre a DSC bővítmény hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d51ac-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="d51ac-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="d51ac-143">-DataCollection</span></span>
<span data-ttu-id="d51ac-144">Az adatgyűjtési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-144">Specifies the data collection type.</span></span>
<span data-ttu-id="d51ac-145">A paraméter elfogadható értékei a következők: engedélyezés és letiltás.</span><span class="sxs-lookup"><span data-stu-id="d51ac-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51ac-146">-DefaultProfile</span></span>
<span data-ttu-id="d51ac-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d51ac-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51ac-148">-Force</span><span class="sxs-lookup"><span data-stu-id="d51ac-148">-Force</span></span>
<span data-ttu-id="d51ac-149">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d51ac-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d51ac-150">-Hely</span><span class="sxs-lookup"><span data-stu-id="d51ac-150">-Location</span></span>
<span data-ttu-id="d51ac-151">Az erőforrás-kiterjesztés elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="d51ac-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d51ac-152">-Name</span></span>
<span data-ttu-id="d51ac-153">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d51ac-154">Az alapértelmezett érték a Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="d51ac-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="d51ac-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51ac-155">-ResourceGroupName</span></span>
<span data-ttu-id="d51ac-156">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-156">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-157">-Verzió</span><span class="sxs-lookup"><span data-stu-id="d51ac-157">-Version</span></span>
<span data-ttu-id="d51ac-158">Annak a DSC-bővítménynek a verziószámát adja meg, amely a Set-AzVMDscExtension alkalmazza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d51ac-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="d51ac-159">-VMName</span></span>
<span data-ttu-id="d51ac-160">Annak a virtuális gépnek a neve, ahol a DSC Extension Handler telepítve van.</span><span class="sxs-lookup"><span data-stu-id="d51ac-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="d51ac-161">-WmfVersion</span></span>
<span data-ttu-id="d51ac-162">A WMF-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d51ac-162">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51ac-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d51ac-163">-Confirm</span></span>
<span data-ttu-id="d51ac-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d51ac-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51ac-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51ac-165">-WhatIf</span></span>
<span data-ttu-id="d51ac-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d51ac-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51ac-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d51ac-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51ac-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51ac-168">CommonParameters</span></span>
<span data-ttu-id="d51ac-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d51ac-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51ac-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51ac-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51ac-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d51ac-171">INPUTS</span></span>

### <span data-ttu-id="d51ac-172">System. String</span><span class="sxs-lookup"><span data-stu-id="d51ac-172">System.String</span></span>

### <span data-ttu-id="d51ac-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d51ac-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d51ac-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d51ac-174">OUTPUTS</span></span>

### <span data-ttu-id="d51ac-175">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d51ac-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d51ac-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d51ac-176">NOTES</span></span>

## <span data-ttu-id="d51ac-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d51ac-177">RELATED LINKS</span></span>

[<span data-ttu-id="d51ac-178">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d51ac-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="d51ac-179">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d51ac-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="d51ac-180">Közzététel – AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d51ac-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


