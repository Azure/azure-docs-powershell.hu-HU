---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024807"
---
# <span data-ttu-id="63d35-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63d35-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="63d35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63d35-102">SYNOPSIS</span></span>
<span data-ttu-id="63d35-103">A DSC bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="63d35-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="63d35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63d35-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63d35-105">DESCRIPTION</span></span>
<span data-ttu-id="63d35-106">A **set-AzVMDscExtension** parancsmag egy erőforráscsoport virtuális gépén a Windows PowerShell által kért állapot-konfigurációs (DSC) kiterjesztést adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="63d35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63d35-107">EXAMPLES</span></span>

### <span data-ttu-id="63d35-108">1. példa: DSC-bővítmény beállítása</span><span class="sxs-lookup"><span data-stu-id="63d35-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="63d35-109">Ez a parancs beállítja a VM07 nevű virtuális gép DSC bővítményét, hogy letöltse Sample.ps1.zip a STG nevű tároló fiókból és az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="63d35-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="63d35-110">A parancs a ConfigName nevű konfigurációt hívja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="63d35-111">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="63d35-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="63d35-112">2. példa: DSC-bővítmény beállítása konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="63d35-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="63d35-113">Ez a parancs beállítja a VM13 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="63d35-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="63d35-114">A parancs a ConfigName nevű konfigurációt adja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="63d35-115">A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="63d35-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="63d35-116">3. példa: DSC-bővítmény beállítása az automatikus frissítést tartalmazó konfigurációs adatokkal</span><span class="sxs-lookup"><span data-stu-id="63d35-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="63d35-117">Ez a parancs beállítja a VM22 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.</span><span class="sxs-lookup"><span data-stu-id="63d35-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="63d35-118">A parancs a ConfigName nevű konfigurációt hívja meg, és a konfigurációs adatokat és argumentumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="63d35-119">Ez a parancs azt is lehetővé teszi, hogy a kiterjesztés-kezelő automatikusan frissítse a legújabb verzióra.</span><span class="sxs-lookup"><span data-stu-id="63d35-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="63d35-120">A Sample.ps1.zip korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.</span><span class="sxs-lookup"><span data-stu-id="63d35-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="63d35-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63d35-121">PARAMETERS</span></span>

### <span data-ttu-id="63d35-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="63d35-122">-ArchiveBlobName</span></span>
<span data-ttu-id="63d35-123">A Publish-AzVMDscConfiguration parancsmag által korábban feltöltött konfigurációs fájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="63d35-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="63d35-124">-ArchiveContainerName</span></span>
<span data-ttu-id="63d35-125">Annak az Azure-tárolónak a megnevezése, amelyben a konfigurációs Archívum található.</span><span class="sxs-lookup"><span data-stu-id="63d35-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="63d35-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d35-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="63d35-127">Annak a csoportnak a neve, amely a konfigurációs archívumot tartalmazó tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="63d35-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="63d35-128">Ez a paraméter nem kötelező, ha a tárolási fiók és a virtuális gép egyaránt ugyanabban az erőforráscsoport-csoportban található.</span><span class="sxs-lookup"><span data-stu-id="63d35-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="63d35-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="63d35-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="63d35-130">Megadja a ArchiveBlobName letöltéséhez használt Azure Storage Account nevet.</span><span class="sxs-lookup"><span data-stu-id="63d35-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="63d35-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="63d35-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="63d35-132">A tárolási végpont utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="63d35-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="63d35-133">-AutoUpdate</span></span>
<span data-ttu-id="63d35-134">A *verzió* paraméter által megadott kiterjesztés-kezelő verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="63d35-135">Alapértelmezés szerint az Extension Handler nem frissíti az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="63d35-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="63d35-136">Használja az *AutoUpdate* paramétert, amellyel engedélyezheti a bővítmények automatikus frissítését a legújabb verzióra, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="63d35-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="63d35-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="63d35-137">-ConfigurationArgument</span></span>
<span data-ttu-id="63d35-138">A konfigurációs függvény argumentumait tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="63d35-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="63d35-139">-ConfigurationData</span></span>
<span data-ttu-id="63d35-140">Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="63d35-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="63d35-141">-ConfigurationName</span></span>
<span data-ttu-id="63d35-142">Annak a konfigurációnak a nevét adja meg, amelyre a DSC bővítmény hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="63d35-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="63d35-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="63d35-143">-DataCollection</span></span>
<span data-ttu-id="63d35-144">Az adatgyűjtési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-144">Specifies the data collection type.</span></span>
<span data-ttu-id="63d35-145">A paraméter elfogadható értékei a következők: engedélyezés és letiltás.</span><span class="sxs-lookup"><span data-stu-id="63d35-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="63d35-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d35-146">-DefaultProfile</span></span>
<span data-ttu-id="63d35-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63d35-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d35-148">-Force</span><span class="sxs-lookup"><span data-stu-id="63d35-148">-Force</span></span>
<span data-ttu-id="63d35-149">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="63d35-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63d35-150">-Hely</span><span class="sxs-lookup"><span data-stu-id="63d35-150">-Location</span></span>
<span data-ttu-id="63d35-151">Az erőforrás-kiterjesztés elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="63d35-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63d35-152">-Name</span></span>
<span data-ttu-id="63d35-153">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="63d35-154">Az alapértelmezett érték a Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="63d35-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="63d35-155">-Várva</span><span class="sxs-lookup"><span data-stu-id="63d35-155">-NoWait</span></span>
<span data-ttu-id="63d35-156">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="63d35-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="63d35-157">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="63d35-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="63d35-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d35-158">-ResourceGroupName</span></span>
<span data-ttu-id="63d35-159">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="63d35-160">-Verzió</span><span class="sxs-lookup"><span data-stu-id="63d35-160">-Version</span></span>
<span data-ttu-id="63d35-161">Annak a DSC-bővítménynek a verziószámát adja meg, amely a Set-AzVMDscExtension alkalmazza a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="63d35-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="63d35-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="63d35-162">-VMName</span></span>
<span data-ttu-id="63d35-163">Annak a virtuális gépnek a neve, ahol a DSC Extension Handler telepítve van.</span><span class="sxs-lookup"><span data-stu-id="63d35-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="63d35-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="63d35-164">-WmfVersion</span></span>
<span data-ttu-id="63d35-165">A WMF-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="63d35-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="63d35-166">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63d35-166">-Confirm</span></span>
<span data-ttu-id="63d35-167">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63d35-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d35-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d35-168">-WhatIf</span></span>
<span data-ttu-id="63d35-169">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63d35-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63d35-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63d35-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d35-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d35-171">CommonParameters</span></span>
<span data-ttu-id="63d35-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63d35-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d35-173">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="63d35-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d35-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63d35-174">INPUTS</span></span>

### <span data-ttu-id="63d35-175">System. String</span><span class="sxs-lookup"><span data-stu-id="63d35-175">System.String</span></span>

### <span data-ttu-id="63d35-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63d35-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="63d35-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63d35-177">OUTPUTS</span></span>

### <span data-ttu-id="63d35-178">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="63d35-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="63d35-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63d35-179">NOTES</span></span>

## <span data-ttu-id="63d35-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63d35-180">RELATED LINKS</span></span>

[<span data-ttu-id="63d35-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63d35-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="63d35-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63d35-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="63d35-183">Közzététel – AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63d35-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


