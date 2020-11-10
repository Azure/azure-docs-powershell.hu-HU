---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: f17da705ed65484e789a803308bcaddb60e409f3
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395135"
---
# <span data-ttu-id="09db1-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="09db1-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="09db1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09db1-102">SYNOPSIS</span></span>
<span data-ttu-id="09db1-103">Titkos kulcsot ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="09db1-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="09db1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09db1-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09db1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09db1-105">DESCRIPTION</span></span>
<span data-ttu-id="09db1-106">Az **Add-AzVMSecret** parancsmag titkot ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="09db1-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="09db1-107">Ezzel az értékkel adhat hozzá tanúsítványt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="09db1-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="09db1-108">A titkot egy kulcsos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="09db1-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="09db1-109">A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="09db1-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="09db1-110">A parancsmagokkal kapcsolatos további tudnivalók az [Azure Key Vault parancsmagok](/powershell/module/az.keyvault) vagy a [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmag című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="09db1-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="09db1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="09db1-111">EXAMPLES</span></span>

### <span data-ttu-id="09db1-112">1. példa: titok hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="09db1-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="09db1-113">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09db1-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="09db1-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="09db1-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="09db1-115">A második parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09db1-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="09db1-116">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="09db1-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="09db1-117">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="09db1-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="09db1-118">A harmadik parancs a **set-AzVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="09db1-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="09db1-119">A negyedik parancs a Forrásobjektum-azonosítót a $SourceVaultId változóhoz rendeli későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="09db1-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="09db1-120">A parancs feltételezi, hogy a $SubscriptionId változó megfelelő értékű.</span><span class="sxs-lookup"><span data-stu-id="09db1-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="09db1-121">Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használat céljából.</span><span class="sxs-lookup"><span data-stu-id="09db1-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="09db1-122">A hatodik parancs a tanúsítványtároló URL-címét rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="09db1-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="09db1-123">A hetedik parancs egy titkot ad a $VirtualMachine-ban tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="09db1-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="09db1-124">A SourceVaultId paraméter a kulcs boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09db1-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="09db1-125">A parancs a tanúsítványtároló nevét és a tanúsítvány URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09db1-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="09db1-126">A **bővítményt** többször is futtathatja, ha más tanúsítványok titkát is hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="09db1-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="09db1-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09db1-127">PARAMETERS</span></span>

### <span data-ttu-id="09db1-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="09db1-128">-CertificateStore</span></span>
<span data-ttu-id="09db1-129">A Windows operációs rendszert futtató virtuális számítógépen a tanúsítványtároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09db1-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="09db1-130">Ez a parancsmag hozzáadja a tanúsítványt a paraméter által megadott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="09db1-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="09db1-131">Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="09db1-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="09db1-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="09db1-132">-CertificateUrl</span></span>
<span data-ttu-id="09db1-133">Itt adhatja meg azt az URL-címet, amely a tanúsítványokat tartalmazó kulcs-boltozati titokra mutat.</span><span class="sxs-lookup"><span data-stu-id="09db1-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="09db1-134">A tanúsítvány az alábbi, UTF-8 kódolású JavaScript-objektum (JSON) objektum Base64 kódolása:</span><span class="sxs-lookup"><span data-stu-id="09db1-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="09db1-135">{"Data": " \<Base64-encoded-file\> "; "adattípus": "" \<file-format\> ; "jelszó": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="09db1-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="09db1-136">Az adattípusok jelenleg csak a. pfx fájlokat fogadják el.</span><span class="sxs-lookup"><span data-stu-id="09db1-136">Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="09db1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09db1-137">-DefaultProfile</span></span>
<span data-ttu-id="09db1-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09db1-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09db1-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="09db1-139">-SourceVaultId</span></span>
<span data-ttu-id="09db1-140">A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09db1-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="09db1-141">Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="09db1-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="09db1-142">Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* , ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.</span><span class="sxs-lookup"><span data-stu-id="09db1-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="09db1-143">-VM</span><span class="sxs-lookup"><span data-stu-id="09db1-143">-VM</span></span>
<span data-ttu-id="09db1-144">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="09db1-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="09db1-145">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09db1-145">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="09db1-146">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="09db1-146">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="09db1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09db1-147">CommonParameters</span></span>
<span data-ttu-id="09db1-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09db1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09db1-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09db1-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09db1-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09db1-150">INPUTS</span></span>

### <span data-ttu-id="09db1-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="09db1-151">PSVirtualMachine</span></span>
<span data-ttu-id="09db1-152">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09db1-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="09db1-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09db1-153">OUTPUTS</span></span>

### <span data-ttu-id="09db1-154">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="09db1-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="09db1-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09db1-155">NOTES</span></span>

## <span data-ttu-id="09db1-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09db1-156">RELATED LINKS</span></span>

[<span data-ttu-id="09db1-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="09db1-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="09db1-158">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="09db1-158">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="09db1-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="09db1-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
