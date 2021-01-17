---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480699"
---
# <span data-ttu-id="4ff3b-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4ff3b-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="4ff3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ff3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff3b-103">Konfigurálja a DSC bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="4ff3b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ff3b-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff3b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ff3b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff3b-106">A **Set-AzVMDscExtension** parancsmag konfigurálja a Kívánt Windows PowerShell-konfiguráció (DSC) bővítményt egy erőforráscsoport virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="4ff3b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ff3b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff3b-108">1. példa: DSC-bővítmény beállítása</span><span class="sxs-lookup"><span data-stu-id="4ff3b-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="4ff3b-109">Ez a parancs beállítja a DSC bővítményt a VM07 nevű virtuális gépen, hogy letöltsen Sample.ps1.zip Stg nevű tárfiókból és az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="4ff3b-110">A parancs meghívja a ConfigName nevű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="4ff3b-111">A Sample.ps1.zip fájl feltöltése korábban a **Publish-AzVMDscConfiguration használatával történt.**</span><span class="sxs-lookup"><span data-stu-id="4ff3b-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="4ff3b-112">2. példa: DSC-bővítmény beállítása konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="4ff3b-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="4ff3b-113">Ez a parancs beállítja a VM13 nevű virtuális gép bővítményét, hogy letöltsen Sample.ps1.zip Stg nevű tárfiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="4ff3b-114">A ConfigName nevű konfigurációs parancs, amely megadja a konfigurációs adatokat és az argumentumokat.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="4ff3b-115">A Sample.ps1.zip fájl feltöltése korábban a **Publish-AzVMDscConfiguration használatával történt.**</span><span class="sxs-lookup"><span data-stu-id="4ff3b-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="4ff3b-116">3. példa: Automatikus frissítéssel elérhető DSC-bővítmény beállítása konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="4ff3b-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="4ff3b-117">Ez a parancs beállítja a VM22 nevű virtuális gép bővítményét, hogy letöltsen Sample.ps1.zip Stg nevű tárfiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="4ff3b-118">A parancs meghívja a ConfigName nevű konfigurációt, és megadja a konfigurációs adatokat és az argumentumokat.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="4ff3b-119">Ez a parancs lehetővé teszi a bővítménykezelő automatikus frissítését a legújabb verzióra.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="4ff3b-120">A Sample.ps1.zip feltöltése a **Publish-AzVMDscConfiguration használatával történt.**</span><span class="sxs-lookup"><span data-stu-id="4ff3b-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="4ff3b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ff3b-121">PARAMETERS</span></span>

### <span data-ttu-id="4ff3b-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-122">-ArchiveBlobName</span></span>
<span data-ttu-id="4ff3b-123">Annak a konfigurációs fájlnak a nevét adja meg, amelyet korábban feltöltött a Publish-AzVMDscConfiguration parancsmag.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="4ff3b-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-124">-ArchiveContainerName</span></span>
<span data-ttu-id="4ff3b-125">Annak az Azure-tárolónak a neve, ahol a konfigurációs archívum található.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="4ff3b-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="4ff3b-127">Annak az erőforráscsoportnak a nevét adja meg, amely a konfigurációs archívumot tartalmazó tárfiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="4ff3b-128">Ez a paraméter nem kötelező, ha a tárfiók és a virtuális gép is ugyanabban az erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="4ff3b-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="4ff3b-130">Az ArchiveBlobName letöltéséhez használt Azure-tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="4ff3b-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4ff3b-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="4ff3b-132">A tárolási végpont utótagját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="4ff3b-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4ff3b-133">-AutoUpdate</span></span>
<span data-ttu-id="4ff3b-134">A Verzió paraméterben megadott *bővítménykezelő-verziót* adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="4ff3b-135">Alapértelmezés szerint a bővítménykezelő nincs automatikusan frissítve.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="4ff3b-136">Az *AutoUpdate* paraméterrel engedélyezheti a bővítménykezelő automatikus frissítését a legújabb verzióra, amint és amikor elérhető.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="4ff3b-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="4ff3b-137">-ConfigurationArgument</span></span>
<span data-ttu-id="4ff3b-138">Egy olyan kivonattáblát ad meg, amely a konfigurációs függvény argumentumát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="4ff3b-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="4ff3b-139">-ConfigurationData</span></span>
<span data-ttu-id="4ff3b-140">Egy .psd1 fájl elérési útját adja meg, amely a konfiguráció adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="4ff3b-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-141">-ConfigurationName</span></span>
<span data-ttu-id="4ff3b-142">A DSC-bővítmény által meghívt konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="4ff3b-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="4ff3b-143">-DataCollection</span></span>
<span data-ttu-id="4ff3b-144">Az adatgyűjtés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-144">Specifies the data collection type.</span></span>
<span data-ttu-id="4ff3b-145">A paraméter elfogadható értékei a következőek: Engedélyezés és Letiltás.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="4ff3b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff3b-146">-DefaultProfile</span></span>
<span data-ttu-id="4ff3b-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff3b-148">-Force</span><span class="sxs-lookup"><span data-stu-id="4ff3b-148">-Force</span></span>
<span data-ttu-id="4ff3b-149">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ff3b-150">-Location</span><span class="sxs-lookup"><span data-stu-id="4ff3b-150">-Location</span></span>
<span data-ttu-id="4ff3b-151">Az erőforrás-kiterjesztés elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="4ff3b-152">-Name</span><span class="sxs-lookup"><span data-stu-id="4ff3b-152">-Name</span></span>
<span data-ttu-id="4ff3b-153">A bővítményt képviselő Azure Resource Manager-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4ff3b-154">Az alapértelmezett érték a Microsoft.Powershell.DSC.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="4ff3b-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ff3b-155">-NoWait</span></span>
<span data-ttu-id="4ff3b-156">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4ff3b-157">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4ff3b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-158">-ResourceGroupName</span></span>
<span data-ttu-id="4ff3b-159">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4ff3b-160">-Version</span><span class="sxs-lookup"><span data-stu-id="4ff3b-160">-Version</span></span>
<span data-ttu-id="4ff3b-161">A DSC bővítménynek azt a verzióját adja meg, Set-AzVMDscExtension a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="4ff3b-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-162">-VMName</span></span>
<span data-ttu-id="4ff3b-163">Annak a virtuális gépnek a neve, ahol a DSC bővítménykezelő telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="4ff3b-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="4ff3b-164">-WmfVersion</span></span>
<span data-ttu-id="4ff3b-165">A WMF-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="4ff3b-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ff3b-166">-Confirm</span></span>
<span data-ttu-id="4ff3b-167">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff3b-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff3b-168">-WhatIf</span></span>
<span data-ttu-id="4ff3b-169">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff3b-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff3b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff3b-171">CommonParameters</span></span>
<span data-ttu-id="4ff3b-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff3b-173">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ff3b-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff3b-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ff3b-174">INPUTS</span></span>

### <span data-ttu-id="4ff3b-175">System.String</span><span class="sxs-lookup"><span data-stu-id="4ff3b-175">System.String</span></span>

### <span data-ttu-id="4ff3b-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ff3b-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ff3b-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ff3b-177">OUTPUTS</span></span>

### <span data-ttu-id="4ff3b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4ff3b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4ff3b-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ff3b-179">NOTES</span></span>

## <span data-ttu-id="4ff3b-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ff3b-180">RELATED LINKS</span></span>

[<span data-ttu-id="4ff3b-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4ff3b-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="4ff3b-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4ff3b-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="4ff3b-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff3b-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


