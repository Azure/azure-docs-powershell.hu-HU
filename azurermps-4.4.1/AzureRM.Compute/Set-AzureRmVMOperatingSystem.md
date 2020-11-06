---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 2d742a70f1ae95d362d5ceafcc117f1296dc2cb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505616"
---
# <span data-ttu-id="53aff-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="53aff-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="53aff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53aff-102">SYNOPSIS</span></span>
<span data-ttu-id="53aff-103">A virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="53aff-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53aff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53aff-104">SYNTAX</span></span>

### <span data-ttu-id="53aff-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53aff-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53aff-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="53aff-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53aff-107">Linux</span><span class="sxs-lookup"><span data-stu-id="53aff-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53aff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="53aff-108">DESCRIPTION</span></span>
<span data-ttu-id="53aff-109">A **set-AzureRmVMOperatingSystem** parancsmag a virtuális gépek operációs rendszerének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="53aff-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="53aff-110">Megadhatja a bejelentkezési hitelesítő adatait, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="53aff-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="53aff-111">Példák</span><span class="sxs-lookup"><span data-stu-id="53aff-111">EXAMPLES</span></span>

### <span data-ttu-id="53aff-112">1. példa: az operációs rendszer tulajdonságainak beállítása új virtuális gépekhez</span><span class="sxs-lookup"><span data-stu-id="53aff-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="53aff-113">Az első parancs a jelszót egy biztonságos karakterláncba konvertálja, majd a $SecurePassword változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53aff-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="53aff-114">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="53aff-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="53aff-115">A második parancs létrehozza a hitelesítő adatokat a felhasználói FullerP és a $SecurePassword tárolt jelszóhoz, majd a $Credential változóban tárolja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="53aff-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="53aff-116">További információért írja be a következőt: `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="53aff-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="53aff-117">A harmadik parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="53aff-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="53aff-118">A negyedik parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53aff-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="53aff-119">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="53aff-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="53aff-120">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="53aff-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="53aff-121">A következő négy parancs az alábbi parancsban használható változók értékeit társítja.</span><span class="sxs-lookup"><span data-stu-id="53aff-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="53aff-122">Mivel ezeket a karakterláncokat közvetlenül megadhatja a **set-AzureRmVMOperatingSystem** parancsban, ez a megközelítés csak az olvashatóság érdekében használatos.</span><span class="sxs-lookup"><span data-stu-id="53aff-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="53aff-123">Használhatja azonban a parancsfájlokban például ezt a módszert.</span><span class="sxs-lookup"><span data-stu-id="53aff-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="53aff-124">A végleges parancs beállítja az operációs rendszer tulajdonságait az $VirtualMachine tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="53aff-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="53aff-125">A parancs a $Credentialban tárolt hitelesítő adatokat használja.</span><span class="sxs-lookup"><span data-stu-id="53aff-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="53aff-126">A parancs bizonyos paraméterek esetében az előző parancsokban megadott változókat használja.</span><span class="sxs-lookup"><span data-stu-id="53aff-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="53aff-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53aff-127">PARAMETERS</span></span>

### <span data-ttu-id="53aff-128">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="53aff-128">-ComputerName</span></span>
<span data-ttu-id="53aff-129">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53aff-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="53aff-130">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="53aff-130">-Credential</span></span>
<span data-ttu-id="53aff-131">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="53aff-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="53aff-132">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="53aff-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="53aff-133">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="53aff-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="53aff-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="53aff-134">-CustomData</span></span>
<span data-ttu-id="53aff-135">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="53aff-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="53aff-136">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="53aff-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="53aff-137">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="53aff-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="53aff-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53aff-138">-DefaultProfile</span></span>
<span data-ttu-id="53aff-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53aff-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53aff-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="53aff-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="53aff-141">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="53aff-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="53aff-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="53aff-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="53aff-143">Jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="53aff-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="53aff-144">-Linux</span></span>
<span data-ttu-id="53aff-145">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="53aff-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="53aff-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="53aff-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="53aff-147">Azt jelzi, hogy a beállítások megkövetelik, hogy a virtuálisgép-ügynök telepítve legyen a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="53aff-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="53aff-148">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="53aff-148">-TimeZone</span></span>
<span data-ttu-id="53aff-149">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53aff-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-150">-VM</span><span class="sxs-lookup"><span data-stu-id="53aff-150">-VM</span></span>
<span data-ttu-id="53aff-151">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe az operációs rendszer tulajdonságait be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="53aff-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="53aff-152">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="53aff-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="53aff-153">Virtuális gép objektum létrehozása az New-AzureRmVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="53aff-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="53aff-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="53aff-154">-Windows</span></span>
<span data-ttu-id="53aff-155">Azt jelzi, hogy a Windows operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="53aff-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="53aff-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="53aff-157">A WinRM-tanúsítványok URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53aff-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="53aff-158">Ezt egy fontos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="53aff-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="53aff-159">-WinRMHttp</span></span>
<span data-ttu-id="53aff-160">Azt jelzi, hogy az operációs rendszer a HTTP WinRM szolgáltatást használja.</span><span class="sxs-lookup"><span data-stu-id="53aff-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="53aff-161">-WinRMHttps</span></span>
<span data-ttu-id="53aff-162">Azt jelzi, hogy ez az operációs rendszer HTTPS-WinRM protokollt használ.</span><span class="sxs-lookup"><span data-stu-id="53aff-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53aff-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53aff-163">CommonParameters</span></span>
<span data-ttu-id="53aff-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53aff-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53aff-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53aff-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53aff-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53aff-166">INPUTS</span></span>

## <span data-ttu-id="53aff-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53aff-167">OUTPUTS</span></span>

## <span data-ttu-id="53aff-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53aff-168">NOTES</span></span>

## <span data-ttu-id="53aff-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53aff-169">RELATED LINKS</span></span>

[<span data-ttu-id="53aff-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="53aff-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="53aff-171">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="53aff-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


