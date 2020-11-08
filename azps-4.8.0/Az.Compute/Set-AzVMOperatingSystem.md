---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024103"
---
# <span data-ttu-id="c02d1-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c02d1-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="c02d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c02d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c02d1-103">A virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="c02d1-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="c02d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c02d1-104">SYNTAX</span></span>

### <span data-ttu-id="c02d1-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c02d1-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c02d1-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="c02d1-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02d1-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="c02d1-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c02d1-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="c02d1-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02d1-109">Linux</span><span class="sxs-lookup"><span data-stu-id="c02d1-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c02d1-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="c02d1-110">DESCRIPTION</span></span>
<span data-ttu-id="c02d1-111">A **set-AzVMOperatingSystem** parancsmag a virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="c02d1-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="c02d1-112">Megadhatja a bejelentkezési hitelesítő adatait, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="c02d1-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="c02d1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c02d1-113">EXAMPLES</span></span>

### <span data-ttu-id="c02d1-114">1. példa: az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez</span><span class="sxs-lookup"><span data-stu-id="c02d1-114">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="c02d1-115">Az első parancs a jelszót egy biztonságos karakterláncba konvertálja, majd a $SecurePassword változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="c02d1-116">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="c02d1-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="c02d1-117">A második parancs létrehozza a hitelesítő adatokat a felhasználói FullerP és a $SecurePassword tárolt jelszóhoz, majd a $Credential változóban tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="c02d1-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="c02d1-118">További információért írja be a következőt: `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="c02d1-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="c02d1-119">A harmadik parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="c02d1-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="c02d1-120">A negyedik parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c02d1-121">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="c02d1-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c02d1-122">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="c02d1-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="c02d1-123">A következő négy parancs az alábbi parancsban használható változók értékeit társítja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="c02d1-124">Mivel ezeket a karakterláncokat közvetlenül megadhatja a **set-AzVMOperatingSystem** parancsban, ez a megközelítés csak az olvashatóság érdekében használatos.</span><span class="sxs-lookup"><span data-stu-id="c02d1-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="c02d1-125">Használhatja azonban a parancsfájlokban például ezt a módszert.</span><span class="sxs-lookup"><span data-stu-id="c02d1-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="c02d1-126">A végleges parancs beállítja az operációs rendszer tulajdonságait az $VirtualMachine tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="c02d1-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c02d1-127">A parancs a $Credentialban tárolt hitelesítő adatokat használja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="c02d1-128">A parancs bizonyos paraméterek esetében az előző parancsokban megadott változókat használja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="c02d1-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c02d1-129">PARAMETERS</span></span>

### <span data-ttu-id="c02d1-130">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="c02d1-130">-ComputerName</span></span>
<span data-ttu-id="c02d1-131">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c02d1-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="c02d1-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="c02d1-132">-Credential</span></span>
<span data-ttu-id="c02d1-133">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c02d1-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="c02d1-134">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c02d1-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="c02d1-135">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c02d1-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="c02d1-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="c02d1-136">-CustomData</span></span>
<span data-ttu-id="c02d1-137">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="c02d1-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="c02d1-138">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="c02d1-139">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="c02d1-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="c02d1-140">**Megjegyzés: ne adjon meg semmilyen titkot vagy jelszót a customData tulajdonságban.**</span><span class="sxs-lookup"><span data-stu-id="c02d1-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="c02d1-141">Ez a tulajdonság nem frissíthető a VM létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="c02d1-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="c02d1-142">a customData-ra a program a VM-re továbbítja a fájlt, további információt az [Egyéni adatok az Azure VMS](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) szolgáltatásban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c02d1-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="c02d1-143">A Cloud-init for your Linux VM használata esetén olvassa el a következő témakört: a [Cloud-init használata a Linux VM testreszabására a létrehozás során](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span><span class="sxs-lookup"><span data-stu-id="c02d1-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="c02d1-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02d1-144">-DefaultProfile</span></span>
<span data-ttu-id="c02d1-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c02d1-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c02d1-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="c02d1-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="c02d1-147">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="c02d1-147">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="c02d1-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="c02d1-148">-DisableVMAgent</span></span>
<span data-ttu-id="c02d1-149">Tiltsa le a létesítés VM Agent-ügynököt.</span><span class="sxs-lookup"><span data-stu-id="c02d1-149">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="c02d1-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c02d1-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="c02d1-151">Jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="c02d1-151">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="c02d1-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="c02d1-152">-Linux</span></span>
<span data-ttu-id="c02d1-153">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="c02d1-153">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="c02d1-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="c02d1-154">-PatchMode</span></span>
<span data-ttu-id="c02d1-155">Itt adhatja meg a IaaS virtuális gépre való frissítésének módját.</span><span class="sxs-lookup"><span data-stu-id="c02d1-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="c02d1-156">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="c02d1-156">Possible values are:</span></span><br>
<span data-ttu-id="c02d1-157">**Manuális** : a javítások alkalmazását egy virtuális gépre irányítja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="c02d1-158">Ezt úgy teheti meg, hogy a VM-ben manuálisan alkalmazza a tapaszokat.</span><span class="sxs-lookup"><span data-stu-id="c02d1-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="c02d1-159">Ebben az üzemmódban az automatikus frissítések le vannak tiltva; a WindowsConfiguration. enableAutomaticUpdates tulajdonságnak false-nak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c02d1-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="c02d1-160">**AutomaticByOS** – a virtuális gépet automatikusan frissíti az operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="c02d1-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="c02d1-161">A WindowsConfiguration. enableAutomaticUpdates tulajdonságnak igaznak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c02d1-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="c02d1-162">**AutomaticByPlatform** – a virtuális gépet automatikusan frissíti az operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="c02d1-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="c02d1-163">A provisionVMAgent és a WindowsConfiguration. enableAutomaticUpdates tulajdonságnak igaznak kell lennie</span><span class="sxs-lookup"><span data-stu-id="c02d1-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="c02d1-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="c02d1-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="c02d1-165">Azt jelzi, hogy a beállítások megkövetelik, hogy a virtuálisgép-ügynök telepítve legyen a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="c02d1-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="c02d1-166">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="c02d1-166">-TimeZone</span></span>
<span data-ttu-id="c02d1-167">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c02d1-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="c02d1-168">például \" Pacific standard Time \" .</span><span class="sxs-lookup"><span data-stu-id="c02d1-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="c02d1-169">A lehetséges értékek a [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)által eredményül adott időzónákban is [TimeZoneInfo.id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) .</span><span class="sxs-lookup"><span data-stu-id="c02d1-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="c02d1-170">-VM</span><span class="sxs-lookup"><span data-stu-id="c02d1-170">-VM</span></span>
<span data-ttu-id="c02d1-171">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe az operációs rendszer tulajdonságait be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="c02d1-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="c02d1-172">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c02d1-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="c02d1-173">Virtuális gép objektum létrehozása az New-AzVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c02d1-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="c02d1-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="c02d1-174">-Windows</span></span>
<span data-ttu-id="c02d1-175">Azt jelzi, hogy a Windows operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="c02d1-175">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="c02d1-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="c02d1-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="c02d1-177">A WinRM-tanúsítványok URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c02d1-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="c02d1-178">Ezt egy fontos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="c02d1-178">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="c02d1-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="c02d1-179">-WinRMHttp</span></span>
<span data-ttu-id="c02d1-180">Azt jelzi, hogy az operációs rendszer a HTTP WinRM szolgáltatást használja.</span><span class="sxs-lookup"><span data-stu-id="c02d1-180">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="c02d1-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="c02d1-181">-WinRMHttps</span></span>
<span data-ttu-id="c02d1-182">Azt jelzi, hogy ez az operációs rendszer HTTPS-WinRM protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="c02d1-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="c02d1-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02d1-183">CommonParameters</span></span>
<span data-ttu-id="c02d1-184">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c02d1-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02d1-185">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c02d1-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02d1-186">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c02d1-186">INPUTS</span></span>

### <span data-ttu-id="c02d1-187">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c02d1-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c02d1-188">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c02d1-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c02d1-189">System. String</span><span class="sxs-lookup"><span data-stu-id="c02d1-189">System.String</span></span>

### <span data-ttu-id="c02d1-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c02d1-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="c02d1-191">System. URI</span><span class="sxs-lookup"><span data-stu-id="c02d1-191">System.Uri</span></span>

## <span data-ttu-id="c02d1-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c02d1-192">OUTPUTS</span></span>

### <span data-ttu-id="c02d1-193">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c02d1-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c02d1-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c02d1-194">NOTES</span></span>

## <span data-ttu-id="c02d1-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c02d1-195">RELATED LINKS</span></span>

[<span data-ttu-id="c02d1-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c02d1-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c02d1-197">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c02d1-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


