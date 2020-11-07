---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 804606f854ab3375d7a40d364d5af9c9179e8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672623"
---
# <span data-ttu-id="ac9c1-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac9c1-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="ac9c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9c1-103">A virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac9c1-104">SYNTAX</span></span>

### <span data-ttu-id="ac9c1-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac9c1-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9c1-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ac9c1-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9c1-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ac9c1-107">WindowsDisableVMAgent</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9c1-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ac9c1-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9c1-109">Linux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-109">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9c1-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac9c1-110">DESCRIPTION</span></span>
<span data-ttu-id="ac9c1-111">A **set-AzureRmVMOperatingSystem** parancsmag a virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-111">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="ac9c1-112">Megadhatja a bejelentkezési hitelesítő adatait, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="ac9c1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ac9c1-113">EXAMPLES</span></span>

### <span data-ttu-id="ac9c1-114">1. példa: az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez</span><span class="sxs-lookup"><span data-stu-id="ac9c1-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="ac9c1-115">Az első parancs a jelszót egy biztonságos karakterláncba konvertálja, majd a $SecurePassword változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="ac9c1-116">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ac9c1-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="ac9c1-117">A második parancs létrehozza a hitelesítő adatokat a felhasználói FullerP és a $SecurePassword tárolt jelszóhoz, majd a $Credential változóban tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="ac9c1-118">További információért írja be a következőt: `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="ac9c1-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="ac9c1-119">A harmadik parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-119">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ac9c1-120">A negyedik parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ac9c1-121">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ac9c1-122">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ac9c1-123">A következő négy parancs az alábbi parancsban használható változók értékeit társítja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="ac9c1-124">Mivel ezeket a karakterláncokat közvetlenül megadhatja a **set-AzureRmVMOperatingSystem** parancsban, ez a megközelítés csak az olvashatóság érdekében használatos.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-124">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="ac9c1-125">Használhatja azonban a parancsfájlokban például ezt a módszert.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="ac9c1-126">A végleges parancs beállítja az operációs rendszer tulajdonságait az $VirtualMachine tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ac9c1-127">A parancs a $Credentialban tárolt hitelesítő adatokat használja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="ac9c1-128">A parancs bizonyos paraméterek esetében az előző parancsokban megadott változókat használja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="ac9c1-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac9c1-129">PARAMETERS</span></span>

### <span data-ttu-id="ac9c1-130">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="ac9c1-130">-ComputerName</span></span>
<span data-ttu-id="ac9c1-131">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="ac9c1-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ac9c1-132">-Credential</span></span>
<span data-ttu-id="ac9c1-133">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ac9c1-134">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ac9c1-135">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ac9c1-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="ac9c1-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ac9c1-136">-CustomData</span></span>
<span data-ttu-id="ac9c1-137">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ac9c1-138">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ac9c1-139">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ac9c1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9c1-140">-DefaultProfile</span></span>
<span data-ttu-id="ac9c1-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9c1-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ac9c1-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ac9c1-143">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="ac9c1-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ac9c1-144">-DisableVMAgent</span></span>
<span data-ttu-id="ac9c1-145">Tiltsa le a létesítés VM Agent-ügynököt.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="ac9c1-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ac9c1-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="ac9c1-147">Jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="ac9c1-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="ac9c1-148">-Linux</span></span>
<span data-ttu-id="ac9c1-149">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="ac9c1-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ac9c1-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="ac9c1-151">Azt jelzi, hogy a beállítások megkövetelik, hogy a virtuálisgép-ügynök telepítve legyen a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="ac9c1-152">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="ac9c1-152">-TimeZone</span></span>
<span data-ttu-id="ac9c1-153">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="ac9c1-154">-VM</span><span class="sxs-lookup"><span data-stu-id="ac9c1-154">-VM</span></span>
<span data-ttu-id="ac9c1-155">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe az operációs rendszer tulajdonságait be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="ac9c1-156">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-156">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="ac9c1-157">Virtuális gép objektum létrehozása az New-AzureRmVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-157">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="ac9c1-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="ac9c1-158">-Windows</span></span>
<span data-ttu-id="ac9c1-159">Azt jelzi, hogy a Windows operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="ac9c1-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ac9c1-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="ac9c1-161">A WinRM-tanúsítványok URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="ac9c1-162">Ezt egy fontos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="ac9c1-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ac9c1-163">-WinRMHttp</span></span>
<span data-ttu-id="ac9c1-164">Azt jelzi, hogy az operációs rendszer a HTTP WinRM szolgáltatást használja.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="ac9c1-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ac9c1-165">-WinRMHttps</span></span>
<span data-ttu-id="ac9c1-166">Azt jelzi, hogy ez az operációs rendszer HTTPS-WinRM protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="ac9c1-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="ac9c1-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9c1-167">CommonParameters</span></span>
<span data-ttu-id="ac9c1-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac9c1-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9c1-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9c1-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9c1-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac9c1-170">INPUTS</span></span>

### <span data-ttu-id="ac9c1-171">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ac9c1-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ac9c1-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac9c1-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ac9c1-173">System. String</span><span class="sxs-lookup"><span data-stu-id="ac9c1-173">System.String</span></span>

### <span data-ttu-id="ac9c1-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ac9c1-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ac9c1-175">System. URI</span><span class="sxs-lookup"><span data-stu-id="ac9c1-175">System.Uri</span></span>

## <span data-ttu-id="ac9c1-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac9c1-176">OUTPUTS</span></span>

### <span data-ttu-id="ac9c1-177">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ac9c1-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ac9c1-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac9c1-178">NOTES</span></span>

## <span data-ttu-id="ac9c1-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac9c1-179">RELATED LINKS</span></span>

[<span data-ttu-id="ac9c1-180">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ac9c1-180">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ac9c1-181">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ac9c1-181">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


