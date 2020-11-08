---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: b2209b3e9d7c7dcf01a05af277dd5106e70fd8b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181767"
---
# <span data-ttu-id="a3f5f-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="a3f5f-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="a3f5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f5f-103">Titkos kulcsot ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="a3f5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3f5f-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f5f-106">Az **Add-AzVMSecret** parancsmag titkot ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="a3f5f-107">Ezzel az értékkel adhat hozzá tanúsítványt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="a3f5f-108">A titkot egy kulcsos boltozaton kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="a3f5f-109">A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="a3f5f-110">A parancsmagokról további információt az [Azure Key Vault-parancsmagok](https://msdn.microsoft.com/library/azure/dn868052.aspx) a Microsoft Developer Network műsortárában vagy a [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmagban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="a3f5f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a3f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="a3f5f-112">1. példa: titok hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="a3f5f-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="a3f5f-113">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a3f5f-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a3f5f-115">A második parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="a3f5f-116">A parancs a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="a3f5f-117">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a3f5f-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="a3f5f-118">A harmadik parancs a **set-AzVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a3f5f-119">A negyedik parancs a Forrásobjektum-azonosítót a $SourceVaultId változóhoz rendeli későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="a3f5f-120">A parancs feltételezi, hogy a $SubscriptionId változó megfelelő értékű.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="a3f5f-121">Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használat céljából.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="a3f5f-122">A hatodik parancs a tanúsítványtároló URL-címét rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="a3f5f-123">A hetedik parancs egy titkot ad a $VirtualMachine-ban tárolt virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a3f5f-124">A SourceVaultId paraméter a kulcs boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="a3f5f-125">A parancs a tanúsítványtároló nevét és a tanúsítvány URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="a3f5f-126">A **bővítményt** többször is futtathatja, ha más tanúsítványok titkát is hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="a3f5f-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3f5f-127">PARAMETERS</span></span>

### <span data-ttu-id="a3f5f-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="a3f5f-128">-CertificateStore</span></span>
<span data-ttu-id="a3f5f-129">A Windows operációs rendszert futtató virtuális számítógépen a tanúsítványtároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="a3f5f-130">Ez a parancsmag hozzáadja a tanúsítványt a paraméter által megadott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="a3f5f-131">Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5f-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a3f5f-132">-CertificateUrl</span></span>
<span data-ttu-id="a3f5f-133">Itt adhatja meg azt az URL-címet, amely a tanúsítványokat tartalmazó kulcs-boltozati titokra mutat.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="a3f5f-134">A tanúsítvány a következő JavaScript-objektum (JSON) objektum Base64 kódolása, amely UTF-8-ban kódolt: {"Data": " \<Base64-encoded-file\> "; "adattípus": " \<file-format\> "; "password": "" \<pfx-file-password\> } jelenleg az adattípus csak a. pfx fájlokat fogadja el.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="a3f5f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f5f-135">-DefaultProfile</span></span>
<span data-ttu-id="a3f5f-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f5f-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a3f5f-137">-SourceVaultId</span></span>
<span data-ttu-id="a3f5f-138">A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="a3f5f-139">Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="a3f5f-140">Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* , ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5f-141">-VM</span><span class="sxs-lookup"><span data-stu-id="a3f5f-141">-VM</span></span>
<span data-ttu-id="a3f5f-142">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="a3f5f-143">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="a3f5f-144">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="a3f5f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f5f-145">CommonParameters</span></span>
<span data-ttu-id="a3f5f-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3f5f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f5f-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3f5f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f5f-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3f5f-148">INPUTS</span></span>

### <span data-ttu-id="a3f5f-149">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a3f5f-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a3f5f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f5f-150">System.String</span></span>

## <span data-ttu-id="a3f5f-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3f5f-151">OUTPUTS</span></span>

### <span data-ttu-id="a3f5f-152">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a3f5f-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a3f5f-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3f5f-153">NOTES</span></span>

## <span data-ttu-id="a3f5f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3f5f-154">RELATED LINKS</span></span>

[<span data-ttu-id="a3f5f-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a3f5f-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a3f5f-156">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a3f5f-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="a3f5f-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a3f5f-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
