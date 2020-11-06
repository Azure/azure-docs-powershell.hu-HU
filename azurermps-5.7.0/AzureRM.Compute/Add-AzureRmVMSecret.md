---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 517614e93510aab163f5d632705e4a5a3566186a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495457"
---
# <span data-ttu-id="0e369-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="0e369-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="0e369-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e369-102">SYNOPSIS</span></span>
<span data-ttu-id="0e369-103">Titkos kulcsot ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0e369-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e369-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e369-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0e369-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e369-105">DESCRIPTION</span></span>
<span data-ttu-id="0e369-106">Az **Add-AzureRmVMSecret** parancsmag titkot ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0e369-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="0e369-107">Ezzel az értékkel adhat hozzá tanúsítványt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0e369-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="0e369-108">A titkot egy kulcsos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="0e369-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="0e369-109">A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e369-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="0e369-110">A parancsmagokról további információt az [Azure Key Vault-parancsmagok](https://msdn.microsoft.com/library/azure/dn868052.aspx) a Microsoft Developer Network műsortárában vagy a [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) parancsmagban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e369-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="0e369-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0e369-111">EXAMPLES</span></span>

### <span data-ttu-id="0e369-112">1. példa: titok hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="0e369-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="0e369-113">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e369-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0e369-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0e369-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="0e369-115">A második parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0e369-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="0e369-116">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="0e369-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="0e369-117">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="0e369-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="0e369-118">A harmadik parancs a **set-AzureRmVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="0e369-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="0e369-119">A negyedik parancs a Forrásobjektum-azonosítót a $SourceVaultId változóhoz rendeli későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="0e369-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="0e369-120">A parancs feltételezi, hogy a $SubscriptionId változó megfelelő értékű.</span><span class="sxs-lookup"><span data-stu-id="0e369-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="0e369-121">Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használat céljából.</span><span class="sxs-lookup"><span data-stu-id="0e369-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="0e369-122">A hatodik parancs a tanúsítványtároló URL-címét rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="0e369-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="0e369-123">A hetedik parancs egy titkot ad a $VirtualMachine-ban tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="0e369-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0e369-124">A SourceVaultId paraméter a kulcs boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e369-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="0e369-125">A parancs a tanúsítványtároló nevét és a tanúsítvány URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e369-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="0e369-126">A **bővítményt** többször is futtathatja, ha más tanúsítványok titkát is hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="0e369-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="0e369-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e369-127">PARAMETERS</span></span>

### <span data-ttu-id="0e369-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="0e369-128">-CertificateStore</span></span>
<span data-ttu-id="0e369-129">A Windows operációs rendszert futtató virtuális számítógépen a tanúsítványtároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e369-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="0e369-130">Ez a parancsmag hozzáadja a tanúsítványt a paraméter által megadott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="0e369-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="0e369-131">Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="0e369-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e369-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="0e369-132">-CertificateUrl</span></span>
<span data-ttu-id="0e369-133">Itt adhatja meg azt az URL-címet, amely a tanúsítványokat tartalmazó kulcs-boltozati titokra mutat.</span><span class="sxs-lookup"><span data-stu-id="0e369-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="0e369-134">A tanúsítvány az alábbi, UTF-8 kódolású JavaScript-objektum (JSON) objektum Base64 kódolása:</span><span class="sxs-lookup"><span data-stu-id="0e369-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="0e369-135">{"Data": " \<Base64-encoded-file\> "; "adattípus": "" \<file-format\> ; "jelszó": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="0e369-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="0e369-136">Az adattípusok jelenleg csak a. pfx fájlokat fogadják el.</span><span class="sxs-lookup"><span data-stu-id="0e369-136">Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="0e369-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0e369-137">-SourceVaultId</span></span>
<span data-ttu-id="0e369-138">A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e369-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="0e369-139">Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="0e369-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="0e369-140">Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* , ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.</span><span class="sxs-lookup"><span data-stu-id="0e369-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e369-141">-VM</span><span class="sxs-lookup"><span data-stu-id="0e369-141">-VM</span></span>
<span data-ttu-id="0e369-142">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="0e369-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="0e369-143">Virtuális gép objektum beszerzéséhez használja a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e369-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="0e369-144">A [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="0e369-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="0e369-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e369-145">CommonParameters</span></span>
<span data-ttu-id="0e369-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e369-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e369-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e369-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e369-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e369-148">INPUTS</span></span>

### <span data-ttu-id="0e369-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e369-149">None</span></span>
<span data-ttu-id="0e369-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0e369-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e369-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e369-151">OUTPUTS</span></span>

## <span data-ttu-id="0e369-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e369-152">NOTES</span></span>

## <span data-ttu-id="0e369-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e369-153">RELATED LINKS</span></span>

[<span data-ttu-id="0e369-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0e369-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0e369-155">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0e369-155">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="0e369-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0e369-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
