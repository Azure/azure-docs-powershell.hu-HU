---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346338"
---
# <span data-ttu-id="69daf-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="69daf-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="69daf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69daf-102">SYNOPSIS</span></span>
<span data-ttu-id="69daf-103">Hozzáad egy titkos értéket a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="69daf-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="69daf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69daf-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69daf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69daf-105">DESCRIPTION</span></span>
<span data-ttu-id="69daf-106">Az **Add-AzVmssSecret** parancsmag hozzáad egy titkos halmazt a virtuálisgép-mérethalmazhoz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="69daf-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="69daf-107">A titkos kulcsot egy Azure-kulcstárolóban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="69daf-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="69daf-108">A kulcstárra vonatkozó további információkért lásd: [Mi az Azure-kulcstár?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="69daf-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="69daf-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="69daf-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="69daf-110">A parancsmagokkal kapcsolatos további információkért lásd az [Azure Key Vault](/powershell/module/az.keyvault) parancsmagokat vagy a [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69daf-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="69daf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69daf-111">EXAMPLES</span></span>

### <span data-ttu-id="69daf-112">1. példa: Titkos hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="69daf-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="69daf-113">Ebben a példában egy titkos értéket ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="69daf-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="69daf-114">Az első parancs a Get-AzKeyVault parancsmagot használva leküld egy ContosoVault nevű tárolót, és az eredményt a $Vault.</span><span class="sxs-lookup"><span data-stu-id="69daf-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="69daf-115">A második parancs a **New-AzVmssVaultCertificateConfig** parancsmaggal hoz létre egy kulcstároló tanúsítványkonfigurációt a Tanúsítványok nevű tanúsítványtár megadott tanúsítvány-URL-címével, és az eredményeket a $CertConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="69daf-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="69daf-116">A harmadik parancs a **New-AzVmssConfig** parancsmaggal hoz létre egy VMSS-konfigurációs objektumot, és az eredményt a következő nevű változóban $VMSS.</span><span class="sxs-lookup"><span data-stu-id="69daf-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="69daf-117">A negyedik parancs egy titkos kulcsot ad a VMSS-hez a tárolókulcs használatával, a kulcserőforrás-azonosító és a $Vault és $CertConfig tárolóban tárolt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="69daf-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="69daf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69daf-118">PARAMETERS</span></span>

### <span data-ttu-id="69daf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69daf-119">-DefaultProfile</span></span>
<span data-ttu-id="69daf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69daf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69daf-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="69daf-121">-SourceVaultId</span></span>
<span data-ttu-id="69daf-122">Annak a kulcstárnak az erőforrás-azonosítója, amely a virtuális géphez hozzáadhatja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="69daf-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="69daf-123">Ez az érték egyben a több tanúsítvány hozzáadásának kulcsa is.</span><span class="sxs-lookup"><span data-stu-id="69daf-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="69daf-124">Ez azt jelenti, hogy ugyanazt az értéket használhatja a *SourceVaultId* paraméterhez, ha több tanúsítványt ad hozzá ugyanattól a kulcstártól.</span><span class="sxs-lookup"><span data-stu-id="69daf-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69daf-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="69daf-125">-VaultCertificate</span></span>
<span data-ttu-id="69daf-126">Megadja a tároló **tanúsítványobjektumát,** amely a tanúsítvány URL-címét és a tanúsítvány nevét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="69daf-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="69daf-127">Az objektum létrehozásához használhatja a [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69daf-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69daf-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69daf-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="69daf-129">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69daf-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="69daf-130">Ezt az objektumot a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="69daf-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69daf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69daf-131">-Confirm</span></span>
<span data-ttu-id="69daf-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69daf-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69daf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69daf-133">-WhatIf</span></span>
<span data-ttu-id="69daf-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69daf-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69daf-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69daf-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69daf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69daf-136">CommonParameters</span></span>
<span data-ttu-id="69daf-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69daf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69daf-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69daf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69daf-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69daf-139">INPUTS</span></span>

### <span data-ttu-id="69daf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69daf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="69daf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="69daf-141">System.String</span></span>

### <span data-ttu-id="69daf-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="69daf-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="69daf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69daf-143">OUTPUTS</span></span>

### <span data-ttu-id="69daf-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69daf-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="69daf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69daf-145">NOTES</span></span>

## <span data-ttu-id="69daf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69daf-146">RELATED LINKS</span></span>

[<span data-ttu-id="69daf-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="69daf-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="69daf-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="69daf-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
