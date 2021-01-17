---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480694"
---
# <span data-ttu-id="5a7fa-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5a7fa-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="5a7fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7fa-103">Beállítja az operációs rendszer tulajdonságait egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="5a7fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a7fa-104">SYNTAX</span></span>

### <span data-ttu-id="5a7fa-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a7fa-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7fa-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="5a7fa-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7fa-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="5a7fa-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7fa-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="5a7fa-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7fa-109">Linux</span><span class="sxs-lookup"><span data-stu-id="5a7fa-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a7fa-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a7fa-110">DESCRIPTION</span></span>
<span data-ttu-id="5a7fa-111">A **Set-AzVMOperatingSystem** parancsmag beállítja egy virtuális gép operációs rendszerének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="5a7fa-112">Megadhatja a bejelentkezési hitelesítő adatokat, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="5a7fa-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a7fa-113">EXAMPLES</span></span>

### <span data-ttu-id="5a7fa-114">1. példa: Az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez</span><span class="sxs-lookup"><span data-stu-id="5a7fa-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="5a7fa-115">Az első parancs biztonságos karakterláncra konvertálja a jelszót, majd tárolja azt a $SecurePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="5a7fa-116">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5a7fa-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="5a7fa-117">A második parancs létrehoz egy hitelesítő adatokat a felhasználó FullerP-hez és a $SecurePassword-ban tárolt jelszóhoz, majd a hitelesítő adatokat a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="5a7fa-118">További információért írja be a `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="5a7fa-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="5a7fa-119">A harmadik parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja meg, majd az objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5a7fa-120">A negyedik parancs létrehoz egy virtuális gépobjektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5a7fa-121">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5a7fa-122">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="5a7fa-123">A következő négy parancs értékeket rendel a változókhoz, amelyek az alábbi parancsban használhatók.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="5a7fa-124">Mivel ezeket a karakterláncokat közvetlenül a **Set-AzVMOperatingSystem** parancsban is megadhatja, ezt a módszert csak az olvashatóság érdekében használjuk.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="5a7fa-125">A parancsfájlok azonban ehhez hasonló módszert is használhatnak.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="5a7fa-126">Az utolsó parancs beállítja az operációs rendszer tulajdonságait a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5a7fa-127">A parancs a $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="5a7fa-128">A parancs bizonyos paraméterekhez a korábbi parancsokban hozzárendelt változókat használja.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="5a7fa-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a7fa-129">PARAMETERS</span></span>

### <span data-ttu-id="5a7fa-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5a7fa-130">-ComputerName</span></span>
<span data-ttu-id="5a7fa-131">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="5a7fa-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5a7fa-132">-Credential</span></span>
<span data-ttu-id="5a7fa-133">A virtuális gép felhasználónevét és jelszavát adja meg **PSCredential objektumként.**</span><span class="sxs-lookup"><span data-stu-id="5a7fa-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5a7fa-134">Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5a7fa-135">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5a7fa-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="5a7fa-136">-CustomData</span></span>
<span data-ttu-id="5a7fa-137">Egy 64-es alapkódolt egyéni adatokat kódolt karakterláncot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="5a7fa-138">Ezt egy bináris tömbbe dekódolja, amely fájlként van mentve a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="5a7fa-139">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="5a7fa-140">**Megjegyzés: Az egyéniData tulajdonságban ne adja át a titkosságokat és jelszavakat**</span><span class="sxs-lookup"><span data-stu-id="5a7fa-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="5a7fa-141">A virtuális gép létrehozása után ez a tulajdonság nem frissíthető.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="5a7fa-142">A customData át van jelölve a VM-nek fájlként való [mentéshez,](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) további információt az Azure virtuális gépeken található Egyéni adatok</span><span class="sxs-lookup"><span data-stu-id="5a7fa-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="5a7fa-143">Ha felhőbeli initet használ LinuxOS VM-hez, tekintse meg [a Linux VM testreszabása felhőbeli init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) használatával a készítés során</span><span class="sxs-lookup"><span data-stu-id="5a7fa-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="5a7fa-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7fa-144">-DefaultProfile</span></span>
<span data-ttu-id="5a7fa-145">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a7fa-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="5a7fa-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="5a7fa-147">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="5a7fa-148">-DisableVMAgent</span></span>
<span data-ttu-id="5a7fa-149">Tiltsa le a Virtuális gép kiépítési ügynökének funkcióját.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="5a7fa-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="5a7fa-151">Azt jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="5a7fa-152">-Linux</span></span>
<span data-ttu-id="5a7fa-153">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="5a7fa-154">-PatchMode</span></span>
<span data-ttu-id="5a7fa-155">A vendégen keresztüli javítás módja az IaaS virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="5a7fa-156">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="5a7fa-156">Possible values are:</span></span><br>
<span data-ttu-id="5a7fa-157">**Kézi** – Ön szabályozhatja a javítások virtuális gépre való alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="5a7fa-158">Ehhez manuálisan kell telepítenie a javításokat a VM-en belül.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="5a7fa-159">Ebben a módban az automatikus frissítések le vannak tiltva; A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak hamisnak kell lennie</span><span class="sxs-lookup"><span data-stu-id="5a7fa-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="5a7fa-160">**AutomaticByOS** – A virtuális gépet automatikusan frissíti az operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="5a7fa-161">A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak igaznak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="5a7fa-162">**AutomaticByPlatform** – a virtuális gép automatikusan frissül az operációs rendszer által.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="5a7fa-163">A provisionVMAgent és a WindowsConfiguration.enableAutomaticUpdates tulajdonságnak teljesülnie kell</span><span class="sxs-lookup"><span data-stu-id="5a7fa-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="5a7fa-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="5a7fa-165">Azt jelzi, hogy a beállításokhoz telepíteni kell a virtuális gép ügynökét a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5a7fa-166">-TimeZone</span></span>
<span data-ttu-id="5a7fa-167">A virtuális gép időzónáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="5a7fa-168">például a \" csendes-óceáni téli \" idő.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="5a7fa-169">Lehetséges értékek a [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [által visszaadott](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) időzónákból származó TimeZoneInfo.Id is beállíthatók.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-170">-VM</span><span class="sxs-lookup"><span data-stu-id="5a7fa-170">-VM</span></span>
<span data-ttu-id="5a7fa-171">Azt a helyi virtuális gépobjektumot adja meg, amelyen meg kell állítani az operációs rendszer tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="5a7fa-172">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="5a7fa-173">Virtuális gépi objektum létrehozása a New-AzVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="5a7fa-174">-Windows</span></span>
<span data-ttu-id="5a7fa-175">Azt jelzi, hogy az operációs rendszer típusa Windows.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="5a7fa-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="5a7fa-177">Egy WinRM-tanúsítvány URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="5a7fa-178">Ezt egy kulcstárolóban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="5a7fa-179">-WinRMHttp</span></span>
<span data-ttu-id="5a7fa-180">Azt jelzi, hogy ez az operációs rendszer HTTP WinRM-et használ.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="5a7fa-181">-WinRMHttps</span></span>
<span data-ttu-id="5a7fa-182">Azt jelzi, hogy ez az operációs rendszer HTTPS WinRM-et használ.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fa-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7fa-183">CommonParameters</span></span>
<span data-ttu-id="5a7fa-184">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7fa-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7fa-185">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a7fa-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7fa-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a7fa-186">INPUTS</span></span>

### <span data-ttu-id="5a7fa-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a7fa-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5a7fa-188">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a7fa-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5a7fa-189">System.String</span><span class="sxs-lookup"><span data-stu-id="5a7fa-189">System.String</span></span>

### <span data-ttu-id="5a7fa-190">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="5a7fa-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5a7fa-191">System.Uri</span><span class="sxs-lookup"><span data-stu-id="5a7fa-191">System.Uri</span></span>

## <span data-ttu-id="5a7fa-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a7fa-192">OUTPUTS</span></span>

### <span data-ttu-id="5a7fa-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a7fa-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5a7fa-194">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a7fa-194">NOTES</span></span>

## <span data-ttu-id="5a7fa-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a7fa-195">RELATED LINKS</span></span>

[<span data-ttu-id="5a7fa-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a7fa-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5a7fa-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5a7fa-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


