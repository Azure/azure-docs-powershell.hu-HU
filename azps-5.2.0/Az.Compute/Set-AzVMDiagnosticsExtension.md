---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365342"
---
# <span data-ttu-id="d1ca6-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d1ca6-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d1ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ca6-103">Konfigurálja az Azure diagnosztikai bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d1ca6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1ca6-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ca6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="d1ca6-106">A **Set-AzVMDiagnosticsExtension** parancsmag konfigurálja az Azure diagnosztikai bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d1ca6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="d1ca6-108">1. példa: Diagnosztikai konfigurációban megadott tárfiók használatával való diagnosztika engedélyezése</span><span class="sxs-lookup"><span data-stu-id="d1ca6-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="d1ca6-109">Ez a parancs diagnosztikai konfigurációs fájlt használ a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="d1ca6-110">A diagnostics_publicconfig.xml a diagnosztikai bővítmény nyilvános XML-konfigurációját tartalmazza, beleértve annak a tárfióknak a nevét, amelyre a diagnosztikai adatokat küldeni fogja.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="d1ca6-111">A diagnosztikai tárfióknak ugyanabban az előfizetésben kell lennie, mint a virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d1ca6-112">2. példa: Diagnosztikai adatok engedélyezése tárfiók nevével</span><span class="sxs-lookup"><span data-stu-id="d1ca6-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="d1ca6-113">Ez a parancs a tárfiók nevét használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="d1ca6-114">Ha a diagnosztikai konfiguráció nem ad meg tárfióknevet, vagy felül szeretné bírálni a konfigurációs fájlban megadott diagnosztikai tárfiók nevét, használja a *StorageAccountName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="d1ca6-115">A diagnosztikai tárfióknak ugyanabban az előfizetésben kell lennie, mint a virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d1ca6-116">3. példa: A diagnosztika engedélyezése a tárfiók nevével és kulcsával</span><span class="sxs-lookup"><span data-stu-id="d1ca6-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="d1ca6-117">Ez a parancs a tárfiók nevét és kulcsát használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="d1ca6-118">Ha a diagnosztikai tárfiók másik előfizetésben van, mint a virtuális gép, engedélyezze a diagnosztikai adatok küldését a tárfiókba a név és a kulcs explicit megadásával.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="d1ca6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1ca6-119">PARAMETERS</span></span>

### <span data-ttu-id="d1ca6-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d1ca6-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d1ca6-121">Azt jelzi, hogy ez a parancsmag lehetővé teszi-e az Azure-vendégügynöknek, hogy automatikusan frissítse a bővítményt egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ca6-122">-DefaultProfile</span></span>
<span data-ttu-id="d1ca6-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ca6-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d1ca6-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d1ca6-125">A konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-126">-Location</span><span class="sxs-lookup"><span data-stu-id="d1ca6-126">-Location</span></span>
<span data-ttu-id="d1ca6-127">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d1ca6-128">-Name</span></span>
<span data-ttu-id="d1ca6-129">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d1ca6-130">-NoWait</span></span>
<span data-ttu-id="d1ca6-131">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d1ca6-132">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d1ca6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ca6-133">-ResourceGroupName</span></span>
<span data-ttu-id="d1ca6-134">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1ca6-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d1ca6-136">A tárfiók végpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d1ca6-137">-StorageAccountKey</span></span>
<span data-ttu-id="d1ca6-138">A tárfiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1ca6-139">-StorageAccountName</span></span>
<span data-ttu-id="d1ca6-140">A tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d1ca6-141">-StorageContext</span></span>
<span data-ttu-id="d1ca6-142">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d1ca6-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="d1ca6-144">A bővítménynek a virtuális géphez használt verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d1ca6-145">A verzió beszerzéséhez futtassa a Get-AzVMExtensionImage parancsmagot a *PublisherName* paraméterhez a Microsoft.Compute értékkel, a Type paraméterhez pedig a VMAccessAgent *parancsmagot.*</span><span class="sxs-lookup"><span data-stu-id="d1ca6-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="d1ca6-146">-VMName</span></span>
<span data-ttu-id="d1ca6-147">Annak a virtuális gépnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ca6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ca6-148">CommonParameters</span></span>
<span data-ttu-id="d1ca6-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ca6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ca6-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1ca6-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ca6-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1ca6-151">INPUTS</span></span>

### <span data-ttu-id="d1ca6-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d1ca6-152">System.String</span></span>

### <span data-ttu-id="d1ca6-153">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1ca6-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="d1ca6-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1ca6-154">System.Boolean</span></span>

## <span data-ttu-id="d1ca6-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1ca6-155">OUTPUTS</span></span>

### <span data-ttu-id="d1ca6-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d1ca6-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d1ca6-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1ca6-157">NOTES</span></span>

## <span data-ttu-id="d1ca6-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1ca6-158">RELATED LINKS</span></span>

[<span data-ttu-id="d1ca6-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d1ca6-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d1ca6-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d1ca6-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d1ca6-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d1ca6-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


