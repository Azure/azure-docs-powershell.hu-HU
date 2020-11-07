---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9626198c9a512ef65a2011b040378f194abd50ef
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844218"
---
# <span data-ttu-id="af581-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="af581-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="af581-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af581-102">SYNOPSIS</span></span>
<span data-ttu-id="af581-103">Az Azure Diagnostics bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="af581-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="af581-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af581-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af581-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af581-105">DESCRIPTION</span></span>
<span data-ttu-id="af581-106">A **set-AzVMDiagnosticsExtension** parancsmag a virtuális gépen az Azure Diagnostics bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="af581-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="af581-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af581-107">EXAMPLES</span></span>

### <span data-ttu-id="af581-108">1. példa: a diagnosztika engedélyezése diagnosztikai konfigurációs fájlban megadott tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="af581-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="af581-109">Ez a parancs diagnosztikai konfigurációs fájlt használ a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="af581-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="af581-110">A fájl diagnostics_publicconfig.xml tartalmazza a diagnosztika bővítmény nyilvános XML-konfigurációját, benne annak a tárolási fióknak a nevét, amelyre a diagnosztikai adatokat küldi a rendszer.</span><span class="sxs-lookup"><span data-stu-id="af581-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="af581-111">A diagnosztikai tárterület-fióknak ugyanazon az előfizetésben kell lennie, mint a virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="af581-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="af581-112">2. példa: a diagnosztika engedélyezése a tárterület-fióknév használatával</span><span class="sxs-lookup"><span data-stu-id="af581-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="af581-113">Ez a parancs a tároló fiók nevét használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="af581-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="af581-114">Ha a diagnosztikai konfiguráció nem ad meg tárterület-fióknevet, vagy ha felül szeretné bírálni a konfigurációs fájlban megadott diagnosztikai tárolási fiók nevét, használja a *StorageAccountName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="af581-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="af581-115">A diagnosztikai tárterület-fióknak ugyanazon az előfizetésben kell lennie, mint a virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="af581-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="af581-116">3. példa: a diagnosztika engedélyezése a tárolási fiók nevével és a kulccsal</span><span class="sxs-lookup"><span data-stu-id="af581-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="af581-117">Ez a parancs a tárolási fiók nevét és kulcsát használja a diagnosztika engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="af581-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="af581-118">Ha a diagnosztikai tárterület-fiók eltérő előfizetéssel rendelkezik, mint a virtuális gép, akkor engedélyezze a diagnosztikai adatok küldését a tárolási fiókba úgy, hogy kifejezetten megadhatja a nevét és a kulcsát.</span><span class="sxs-lookup"><span data-stu-id="af581-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="af581-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af581-119">PARAMETERS</span></span>

### <span data-ttu-id="af581-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af581-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af581-121">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="af581-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af581-122">-DefaultProfile</span></span>
<span data-ttu-id="af581-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af581-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af581-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="af581-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="af581-125">A konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af581-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="af581-126">-Location</span></span>
<span data-ttu-id="af581-127">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af581-128">-Name</span></span>
<span data-ttu-id="af581-129">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-129">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af581-130">-ResourceGroupName</span></span>
<span data-ttu-id="af581-131">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-131">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="af581-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="af581-133">A tárolási fiók végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-133">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="af581-134">-StorageAccountKey</span></span>
<span data-ttu-id="af581-135">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-135">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="af581-136">-StorageAccountName</span></span>
<span data-ttu-id="af581-137">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-137">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="af581-138">-StorageContext</span></span>
<span data-ttu-id="af581-139">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-139">Specifies the Azure storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af581-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="af581-141">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="af581-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="af581-142">A verzió beolvasásához futtassa a Get-AzVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="af581-142">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="af581-143">-VMName</span></span>
<span data-ttu-id="af581-144">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="af581-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af581-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af581-145">CommonParameters</span></span>
<span data-ttu-id="af581-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af581-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af581-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af581-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af581-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af581-148">INPUTS</span></span>

### <span data-ttu-id="af581-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="af581-149">None</span></span>
<span data-ttu-id="af581-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="af581-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af581-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af581-151">OUTPUTS</span></span>

### <span data-ttu-id="af581-152">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af581-152">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af581-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af581-153">NOTES</span></span>

## <span data-ttu-id="af581-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af581-154">RELATED LINKS</span></span>

[<span data-ttu-id="af581-155">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="af581-155">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="af581-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="af581-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="af581-157">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="af581-157">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


