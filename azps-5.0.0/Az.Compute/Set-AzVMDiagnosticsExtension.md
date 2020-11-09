---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296519"
---
# <span data-ttu-id="d65d8-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d65d8-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d65d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d65d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d65d8-103">Az Azure Diagnostics bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d65d8-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d65d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d65d8-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d65d8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d65d8-105">DESCRIPTION</span></span>
<span data-ttu-id="d65d8-106">A **set-AzVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="d65d8-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d65d8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d65d8-107">EXAMPLES</span></span>

### <span data-ttu-id="d65d8-108">1. példa: a diagnosztika engedélyezése diagnosztikai konfigurációs fájlban megadott tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="d65d8-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="d65d8-109">Ez a parancs diagnosztikai konfigurációs fájlt használ a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d65d8-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="d65d8-110">A fájl diagnostics_publicconfig.xml tartalmazza a diagnosztika bővítmény nyilvános XML-konfigurációját, benne annak a tárolási fióknak a nevét, amelyre a diagnosztikai adatokat küldi a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d65d8-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="d65d8-111">A diagnosztikai tárterület-fióknak ugyanazon az előfizetésben kell lennie, mint a virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="d65d8-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d65d8-112">2. példa: a diagnosztika engedélyezése a tárterület-fióknév használatával</span><span class="sxs-lookup"><span data-stu-id="d65d8-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="d65d8-113">Ez a parancs a tároló fiók nevét használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d65d8-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="d65d8-114">Ha a diagnosztikai konfiguráció nem ad meg tárterület-fióknevet, vagy ha felül szeretné bírálni a konfigurációs fájlban megadott diagnosztikai tárolási fiók nevét, használja a *StorageAccountName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d65d8-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="d65d8-115">A diagnosztikai tárterület-fióknak ugyanazon az előfizetésben kell lennie, mint a virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="d65d8-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d65d8-116">3. példa: a diagnosztika engedélyezése a tárolási fiók nevével és a kulccsal</span><span class="sxs-lookup"><span data-stu-id="d65d8-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="d65d8-117">Ez a parancs a tárolási fiók nevét és kulcsát használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d65d8-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="d65d8-118">Ha a diagnosztikai tárterület-fiók eltérő előfizetéssel rendelkezik, mint a virtuális gép, akkor engedélyezze a diagnosztikai adatok küldését a tárolási fiókba úgy, hogy kifejezetten megadhatja a nevét és a kulcsát.</span><span class="sxs-lookup"><span data-stu-id="d65d8-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="d65d8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d65d8-119">PARAMETERS</span></span>

### <span data-ttu-id="d65d8-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d65d8-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d65d8-121">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="d65d8-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="d65d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65d8-122">-DefaultProfile</span></span>
<span data-ttu-id="d65d8-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d65d8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65d8-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d65d8-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d65d8-125">A konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="d65d8-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="d65d8-126">-Location</span></span>
<span data-ttu-id="d65d8-127">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d65d8-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d65d8-128">-Name</span></span>
<span data-ttu-id="d65d8-129">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="d65d8-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="d65d8-130">-NoWait</span></span>
<span data-ttu-id="d65d8-131">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="d65d8-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d65d8-132">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="d65d8-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d65d8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65d8-133">-ResourceGroupName</span></span>
<span data-ttu-id="d65d8-134">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d65d8-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d65d8-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d65d8-136">A tárolási fiók végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="d65d8-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d65d8-137">-StorageAccountKey</span></span>
<span data-ttu-id="d65d8-138">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="d65d8-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d65d8-139">-StorageAccountName</span></span>
<span data-ttu-id="d65d8-140">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="d65d8-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d65d8-141">-StorageContext</span></span>
<span data-ttu-id="d65d8-142">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d65d8-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d65d8-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d65d8-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="d65d8-144">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="d65d8-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d65d8-145">A verzió beolvasásához futtassa a Get-AzVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="d65d8-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="d65d8-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="d65d8-146">-VMName</span></span>
<span data-ttu-id="d65d8-147">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d65d8-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d65d8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65d8-148">CommonParameters</span></span>
<span data-ttu-id="d65d8-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d65d8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65d8-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d65d8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65d8-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d65d8-151">INPUTS</span></span>

### <span data-ttu-id="d65d8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d65d8-152">System.String</span></span>

### <span data-ttu-id="d65d8-153">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d65d8-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="d65d8-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d65d8-154">System.Boolean</span></span>

## <span data-ttu-id="d65d8-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d65d8-155">OUTPUTS</span></span>

### <span data-ttu-id="d65d8-156">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d65d8-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d65d8-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d65d8-157">NOTES</span></span>

## <span data-ttu-id="d65d8-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d65d8-158">RELATED LINKS</span></span>

[<span data-ttu-id="d65d8-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d65d8-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d65d8-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d65d8-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d65d8-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d65d8-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


