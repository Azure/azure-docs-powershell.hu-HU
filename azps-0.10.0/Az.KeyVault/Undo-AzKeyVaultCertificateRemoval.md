---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842089"
---
# <span data-ttu-id="90a92-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="90a92-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="90a92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a92-102">SYNOPSIS</span></span>
<span data-ttu-id="90a92-103">Visszanyeri a törölt tanúsítványokat egy kulcsos boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="90a92-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="90a92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a92-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a92-105">DESCRIPTION</span></span>
<span data-ttu-id="90a92-106">A **Visszavonás-AzKeyVaultCertificateRemoval** parancsmag egy korábban törölt tanúsítványt fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="90a92-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="90a92-107">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="90a92-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="90a92-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="90a92-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="90a92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="90a92-109">EXAMPLES</span></span>

### <span data-ttu-id="90a92-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90a92-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="90a92-111">Ez a parancs visszaállítja a korábban törölt "MyCertificate" tanúsítványt aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="90a92-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="90a92-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a92-112">PARAMETERS</span></span>

### <span data-ttu-id="90a92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a92-113">-DefaultProfile</span></span>
<span data-ttu-id="90a92-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90a92-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a92-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90a92-115">-Name</span></span>
<span data-ttu-id="90a92-116">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="90a92-116">Certificate name.</span></span>
<span data-ttu-id="90a92-117">Parancsmag: egy tanúsítvány teljes tartománynevét építi fel a Vault neve, a kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="90a92-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a92-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="90a92-118">-VaultName</span></span>
<span data-ttu-id="90a92-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="90a92-119">Vault name.</span></span>
<span data-ttu-id="90a92-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="90a92-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a92-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90a92-121">-Confirm</span></span>
<span data-ttu-id="90a92-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90a92-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a92-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a92-123">-WhatIf</span></span>
<span data-ttu-id="90a92-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90a92-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a92-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90a92-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a92-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a92-126">CommonParameters</span></span>
<span data-ttu-id="90a92-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a92-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a92-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a92-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a92-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a92-129">INPUTS</span></span>

### <span data-ttu-id="90a92-130">System. String</span><span class="sxs-lookup"><span data-stu-id="90a92-130">System.String</span></span>

## <span data-ttu-id="90a92-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a92-131">OUTPUTS</span></span>

### <span data-ttu-id="90a92-132">Microsoft. Azure. Command. Vault. models. Certificate</span><span class="sxs-lookup"><span data-stu-id="90a92-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="90a92-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a92-133">NOTES</span></span>

## <span data-ttu-id="90a92-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a92-134">RELATED LINKS</span></span>

[<span data-ttu-id="90a92-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90a92-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="90a92-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90a92-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
