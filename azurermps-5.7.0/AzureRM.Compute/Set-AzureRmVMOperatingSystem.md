---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497703"
---
# <span data-ttu-id="49384-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="49384-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="49384-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49384-102">SYNOPSIS</span></span>
<span data-ttu-id="49384-103">A virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="49384-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49384-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49384-104">SYNTAX</span></span>

### <span data-ttu-id="49384-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49384-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="49384-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="49384-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="49384-107">Linux</span><span class="sxs-lookup"><span data-stu-id="49384-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="49384-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49384-108">DESCRIPTION</span></span>
<span data-ttu-id="49384-109">A **set-AzureRmVMOperatingSystem** parancsmag a virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="49384-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="49384-110">Megadhatja a bejelentkezési hitelesítő adatait, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="49384-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="49384-111">Példák</span><span class="sxs-lookup"><span data-stu-id="49384-111">EXAMPLES</span></span>

### <span data-ttu-id="49384-112">1. példa: az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez</span><span class="sxs-lookup"><span data-stu-id="49384-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="49384-113">Az első parancs a jelszót egy biztonságos karakterláncba konvertálja, majd a $SecurePassword változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="49384-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="49384-114">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="49384-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="49384-115">A második parancs létrehozza a hitelesítő adatokat a felhasználói FullerP és a $SecurePassword tárolt jelszóhoz, majd a $Credential változóban tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="49384-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="49384-116">További információért írja be a következőt: `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="49384-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="49384-117">A harmadik parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="49384-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="49384-118">A negyedik parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="49384-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="49384-119">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="49384-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="49384-120">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="49384-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="49384-121">A következő négy parancs az alábbi parancsban használható változók értékeit társítja.</span><span class="sxs-lookup"><span data-stu-id="49384-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="49384-122">Mivel ezeket a karakterláncokat közvetlenül megadhatja a **set-AzureRmVMOperatingSystem** parancsban, ez a megközelítés csak az olvashatóság érdekében használatos.</span><span class="sxs-lookup"><span data-stu-id="49384-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="49384-123">Használhatja azonban a parancsfájlokban például ezt a módszert.</span><span class="sxs-lookup"><span data-stu-id="49384-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="49384-124">A végleges parancs beállítja az operációs rendszer tulajdonságait az $VirtualMachine tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="49384-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="49384-125">A parancs a $Credentialban tárolt hitelesítő adatokat használja.</span><span class="sxs-lookup"><span data-stu-id="49384-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="49384-126">A parancs bizonyos paraméterek esetében az előző parancsokban megadott változókat használja.</span><span class="sxs-lookup"><span data-stu-id="49384-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="49384-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49384-127">PARAMETERS</span></span>

### <span data-ttu-id="49384-128">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="49384-128">-ComputerName</span></span>
<span data-ttu-id="49384-129">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49384-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="49384-130">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="49384-130">-Credential</span></span>
<span data-ttu-id="49384-131">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49384-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="49384-132">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="49384-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="49384-133">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="49384-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="49384-134">-CustomData</span></span>
<span data-ttu-id="49384-135">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="49384-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="49384-136">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="49384-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="49384-137">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="49384-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="49384-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="49384-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="49384-139">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="49384-139">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-140">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="49384-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="49384-141">Jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="49384-141">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="49384-142">-Linux</span></span>
<span data-ttu-id="49384-143">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="49384-143">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="49384-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="49384-145">Azt jelzi, hogy a beállítások megkövetelik, hogy a virtuálisgép-ügynök telepítve legyen a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="49384-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-146">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="49384-146">-TimeZone</span></span>
<span data-ttu-id="49384-147">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49384-147">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-148">-VM</span><span class="sxs-lookup"><span data-stu-id="49384-148">-VM</span></span>
<span data-ttu-id="49384-149">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe az operációs rendszer tulajdonságait be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="49384-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="49384-150">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="49384-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="49384-151">Virtuális gép objektum létrehozása az New-AzureRmVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="49384-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="49384-152">-Windows</span></span>
<span data-ttu-id="49384-153">Azt jelzi, hogy a Windows operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="49384-153">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-154">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="49384-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="49384-155">A WinRM-tanúsítványok URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49384-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="49384-156">Ezt egy fontos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="49384-156">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="49384-157">-WinRMHttp</span></span>
<span data-ttu-id="49384-158">Azt jelzi, hogy az operációs rendszer a HTTP WinRM szolgáltatást használja.</span><span class="sxs-lookup"><span data-stu-id="49384-158">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="49384-159">-WinRMHttps</span></span>
<span data-ttu-id="49384-160">Azt jelzi, hogy ez az operációs rendszer HTTPS-WinRM protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="49384-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49384-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49384-161">CommonParameters</span></span>
<span data-ttu-id="49384-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49384-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49384-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49384-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49384-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49384-164">INPUTS</span></span>

### <span data-ttu-id="49384-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="49384-165">None</span></span>
<span data-ttu-id="49384-166">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="49384-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49384-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49384-167">OUTPUTS</span></span>

## <span data-ttu-id="49384-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49384-168">NOTES</span></span>

## <span data-ttu-id="49384-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49384-169">RELATED LINKS</span></span>

[<span data-ttu-id="49384-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="49384-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="49384-171">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="49384-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


