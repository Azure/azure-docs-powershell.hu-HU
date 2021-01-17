---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352097"
---
# <span data-ttu-id="02119-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="02119-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="02119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02119-102">SYNOPSIS</span></span>
<span data-ttu-id="02119-103">Hozzáad egy titkos értéket egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02119-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="02119-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02119-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02119-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02119-105">DESCRIPTION</span></span>
<span data-ttu-id="02119-106">Az **Add-AzVMSecret** parancsmag hozzáad egy titkos értéket egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02119-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="02119-107">Ez az érték lehetővé teszi egy tanúsítvány hozzáadását a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02119-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="02119-108">A titkos kulcsot egy kulcstárolóban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="02119-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="02119-109">A kulcstárról további információt a [Mi az Azure-kulcstár?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="02119-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="02119-110">A parancsmagokkal kapcsolatos további információkért lásd az [Azure Key Vault](/powershell/module/az.keyvault) parancsmagokat vagy a [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02119-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="02119-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02119-111">EXAMPLES</span></span>

### <span data-ttu-id="02119-112">1. példa: Titkos titkos gép hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="02119-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="02119-113">Az első parancs létrehoz egy virtuális gépi objektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="02119-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="02119-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02119-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="02119-115">A második parancs létrehoz egy hitelesítőadat-objektumot a Get-Credential parancsmag használatával, majd az eredményt a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02119-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="02119-116">A parancs felhasználónevet és jelszót kér.</span><span class="sxs-lookup"><span data-stu-id="02119-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="02119-117">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="02119-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="02119-118">A harmadik parancs a **Set-AzVMOperatingSystem** parancsmag használatával konfigurálja a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="02119-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="02119-119">A negyedik parancs hozzárendel egy forrástár-azonosítót a $SourceVaultId változóhoz későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="02119-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="02119-120">A parancs feltételezi, hogy a $SubscriptionId megfelelő értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="02119-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="02119-121">Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="02119-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="02119-122">A hatodik parancs egy tanúsítványtároló URL-címét rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="02119-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="02119-123">A hetedik parancs hozzáad egy titkos értéket a virtuális géphez, amely a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="02119-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="02119-124">A SourceVaultId paraméter a kulcstárat adja meg.</span><span class="sxs-lookup"><span data-stu-id="02119-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="02119-125">A parancs a tanúsítványtároló nevét és a tanúsítvány URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02119-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="02119-126">Az **Add-AzVMSecret** bővítményt többször is futtatva további tanúsítványokat is felvehet.</span><span class="sxs-lookup"><span data-stu-id="02119-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="02119-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02119-127">PARAMETERS</span></span>

### <span data-ttu-id="02119-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="02119-128">-CertificateStore</span></span>
<span data-ttu-id="02119-129">A Windows operációs rendszert futtató virtuális gépen található tanúsítványtároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02119-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="02119-130">Ez a parancsmag hozzáadja a tanúsítványt a tárolóhoz, amit ez a paraméter megad.</span><span class="sxs-lookup"><span data-stu-id="02119-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="02119-131">Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="02119-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="02119-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="02119-132">-CertificateUrl</span></span>
<span data-ttu-id="02119-133">Megadja azt az URL-címet, amely egy tanúsítványt tartalmazó kulcstároló-kódra mutat.</span><span class="sxs-lookup"><span data-stu-id="02119-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="02119-134">A tanúsítvány a következő JavaScript Object Notation (JSON) objektum Base64 kódolású kódolása, amely UTF-8 kódolású: { "data": " \<Base64-encoded-file\> ", "dataType": " ", "password": " " } Jelenleg a dataType csak .pfx fájlokat fogad \<file-format\> \<pfx-file-password\> el.</span><span class="sxs-lookup"><span data-stu-id="02119-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="02119-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02119-135">-DefaultProfile</span></span>
<span data-ttu-id="02119-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02119-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02119-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="02119-137">-SourceVaultId</span></span>
<span data-ttu-id="02119-138">Annak a kulcstárnak az erőforrás-azonosítója, amely a virtuális géphez hozzáadhatja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="02119-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="02119-139">Ez az érték egyben a több tanúsítvány hozzáadásának kulcsa is.</span><span class="sxs-lookup"><span data-stu-id="02119-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="02119-140">Ez azt jelenti, hogy ugyanazt az értéket használhatja *a SourceVaultId* értékhez, ha több tanúsítványt ad hozzá ugyanattól a kulcstártól.</span><span class="sxs-lookup"><span data-stu-id="02119-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="02119-141">-VM</span><span class="sxs-lookup"><span data-stu-id="02119-141">-VM</span></span>
<span data-ttu-id="02119-142">Azt a virtuális gépobjektumot adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="02119-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="02119-143">Virtuális gépi objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02119-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="02119-144">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal virtuális gépi objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="02119-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="02119-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02119-145">CommonParameters</span></span>
<span data-ttu-id="02119-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02119-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02119-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02119-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02119-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02119-148">INPUTS</span></span>

### <span data-ttu-id="02119-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="02119-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="02119-150">System.String</span><span class="sxs-lookup"><span data-stu-id="02119-150">System.String</span></span>

## <span data-ttu-id="02119-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02119-151">OUTPUTS</span></span>

### <span data-ttu-id="02119-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="02119-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="02119-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02119-153">NOTES</span></span>

## <span data-ttu-id="02119-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02119-154">RELATED LINKS</span></span>

[<span data-ttu-id="02119-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="02119-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="02119-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="02119-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="02119-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="02119-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
