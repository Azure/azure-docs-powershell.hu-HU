---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 423cb695e4dedb978c3902e9c2f2c891a977464c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671984"
---
# <span data-ttu-id="4f2b6-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="4f2b6-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="4f2b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2b6-103">Titkot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f2b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f2b6-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f2b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f2b6-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2b6-106">Az **Add-AzureRmVmssSecret** parancsmag titkot ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4f2b6-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4f2b6-107">A titkot az Azure Key Vault-ban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="4f2b6-108">A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="4f2b6-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="4f2b6-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="4f2b6-110">A parancsmagokról további információt az [Azure Key Vault-parancsmagok](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) a Microsoft Developer Network Library vagy a [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) parancsmag) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="4f2b6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4f2b6-111">EXAMPLES</span></span>

### <span data-ttu-id="4f2b6-112">1. példa: titkos érték hozzáadása a VMSS</span><span class="sxs-lookup"><span data-stu-id="4f2b6-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="4f2b6-113">Ez a példa titkot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="4f2b6-114">Az első parancs az Get-AzureRmKeyVault parancsmagot használja a ContosoVault nevű Vault-titok kiválasztásához, és az eredményt a $Vault nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="4f2b6-115">A második parancs a **New-AzureRmVmssVaultCertificateConfig** parancsmagot használja a tanúsítványok nevű tanúsítvány URL-címének megadására a megadott tanúsítvány URL-címének használatával, és az eredményt a $CertConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="4f2b6-116">A harmadik parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="4f2b6-117">A negyedik parancs a VMSS a $Vault és a $CertConfig változóban tárolt fő erőforrás-azonosítóval és a pince-tanúsítvánnyal titkos azonosítót ad.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="4f2b6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f2b6-118">PARAMETERS</span></span>

### <span data-ttu-id="4f2b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2b6-119">-DefaultProfile</span></span>
<span data-ttu-id="4f2b6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f2b6-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4f2b6-121">-SourceVaultId</span></span>
<span data-ttu-id="4f2b6-122">A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="4f2b6-123">Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="4f2b6-124">Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* paraméterhez, ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="4f2b6-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4f2b6-125">-VaultCertificate</span></span>
<span data-ttu-id="4f2b6-126">A tanúsítvány URL-címét és tanúsítványát tartalmazó pince- **bizonyítvány** objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="4f2b6-127">Az objektum létrehozásához használhatja a [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="4f2b6-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4f2b6-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4f2b6-129">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="4f2b6-130">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="4f2b6-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f2b6-131">-Confirm</span></span>
<span data-ttu-id="4f2b6-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f2b6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f2b6-133">-WhatIf</span></span>
<span data-ttu-id="4f2b6-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f2b6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f2b6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f2b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2b6-136">CommonParameters</span></span>
<span data-ttu-id="4f2b6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f2b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2b6-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f2b6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2b6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f2b6-139">INPUTS</span></span>

### <span data-ttu-id="4f2b6-140">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4f2b6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4f2b6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4f2b6-141">System.String</span></span>

### <span data-ttu-id="4f2b6-142">Microsoft. Azure. Management. számítás. models. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="4f2b6-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="4f2b6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f2b6-143">OUTPUTS</span></span>

### <span data-ttu-id="4f2b6-144">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4f2b6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4f2b6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f2b6-145">NOTES</span></span>

## <span data-ttu-id="4f2b6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f2b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="4f2b6-147">Új – AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="4f2b6-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="4f2b6-148">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4f2b6-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
