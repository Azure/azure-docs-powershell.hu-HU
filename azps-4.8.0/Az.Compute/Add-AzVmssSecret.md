---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395255"
---
# <span data-ttu-id="fd9a3-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="fd9a3-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="fd9a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9a3-103">Titkot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="fd9a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd9a3-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd9a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd9a3-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9a3-106">Az **Add-AzVmssSecret** parancsmag titkot ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fd9a3-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fd9a3-107">A titkot az Azure Key Vault-ban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="fd9a3-108">A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="fd9a3-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="fd9a3-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="fd9a3-110">A parancsmagokkal kapcsolatos további tudnivalók az [Azure Key Vault parancsmagok](/powershell/module/az.keyvault) vagy a [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmag című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="fd9a3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fd9a3-111">EXAMPLES</span></span>

### <span data-ttu-id="fd9a3-112">1. példa: titkos érték hozzáadása a VMSS</span><span class="sxs-lookup"><span data-stu-id="fd9a3-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="fd9a3-113">Ez a példa titkot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="fd9a3-114">Az első parancs az Get-AzKeyVault parancsmagot használja a ContosoVault nevű Vault-titok kiválasztásához, és az eredményt a $Vault nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="fd9a3-115">A második parancs a **New-AzVmssVaultCertificateConfig** parancsmagot használja a tanúsítványok nevű tanúsítvány URL-címének megadására a megadott tanúsítvány URL-címének használatával, és az eredményt a $CertConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="fd9a3-116">A harmadik parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="fd9a3-117">A negyedik parancs a VMSS a $Vault és a $CertConfig változóban tárolt fő erőforrás-azonosítóval és a pince-tanúsítvánnyal titkos azonosítót ad.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="fd9a3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd9a3-118">PARAMETERS</span></span>

### <span data-ttu-id="fd9a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9a3-119">-DefaultProfile</span></span>
<span data-ttu-id="fd9a3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd9a3-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fd9a3-121">-SourceVaultId</span></span>
<span data-ttu-id="fd9a3-122">A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="fd9a3-123">Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="fd9a3-124">Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* paraméterhez, ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="fd9a3-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fd9a3-125">-VaultCertificate</span></span>
<span data-ttu-id="fd9a3-126">A tanúsítvány URL-címét és tanúsítványát tartalmazó pince- **bizonyítvány** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="fd9a3-127">Az objektum létrehozásához használhatja a [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="fd9a3-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd9a3-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd9a3-129">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="fd9a3-130">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="fd9a3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd9a3-131">-Confirm</span></span>
<span data-ttu-id="fd9a3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd9a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9a3-133">-WhatIf</span></span>
<span data-ttu-id="fd9a3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd9a3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd9a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9a3-136">CommonParameters</span></span>
<span data-ttu-id="fd9a3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd9a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9a3-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fd9a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9a3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd9a3-139">INPUTS</span></span>

### <span data-ttu-id="fd9a3-140">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd9a3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fd9a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fd9a3-141">System.String</span></span>

### <span data-ttu-id="fd9a3-142">Microsoft. Azure. Management. számítás. models. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="fd9a3-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="fd9a3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd9a3-143">OUTPUTS</span></span>

### <span data-ttu-id="fd9a3-144">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd9a3-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fd9a3-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd9a3-145">NOTES</span></span>

## <span data-ttu-id="fd9a3-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd9a3-146">RELATED LINKS</span></span>

[<span data-ttu-id="fd9a3-147">Új – AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="fd9a3-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="fd9a3-148">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fd9a3-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
