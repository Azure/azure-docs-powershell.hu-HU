---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849289"
---
# <span data-ttu-id="29974-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="29974-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="29974-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29974-102">SYNOPSIS</span></span>
<span data-ttu-id="29974-103">Visszanyeri a törölt tanúsítványokat egy kulcsos boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="29974-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29974-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29974-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29974-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29974-105">DESCRIPTION</span></span>
<span data-ttu-id="29974-106">A **Visszavonás-AzureKeyVaultCertificateRemoval** parancsmag egy korábban törölt tanúsítványt fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="29974-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="29974-107">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="29974-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="29974-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="29974-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="29974-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29974-109">EXAMPLES</span></span>

### <span data-ttu-id="29974-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29974-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="29974-111">Ez a parancs visszaállítja a korábban törölt "MyCertificate" tanúsítványt aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="29974-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="29974-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29974-112">PARAMETERS</span></span>

### <span data-ttu-id="29974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29974-113">-DefaultProfile</span></span>
<span data-ttu-id="29974-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29974-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29974-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29974-115">-Name</span></span>
<span data-ttu-id="29974-116">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="29974-116">Certificate name.</span></span>
<span data-ttu-id="29974-117">Parancsmag: egy tanúsítvány teljes tartománynevét építi fel a Vault neve, a kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="29974-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="29974-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29974-118">-VaultName</span></span>
<span data-ttu-id="29974-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="29974-119">Vault name.</span></span>
<span data-ttu-id="29974-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="29974-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="29974-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29974-121">-Confirm</span></span>
<span data-ttu-id="29974-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29974-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29974-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29974-123">-WhatIf</span></span>
<span data-ttu-id="29974-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29974-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29974-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29974-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29974-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29974-126">CommonParameters</span></span>
<span data-ttu-id="29974-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29974-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29974-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29974-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29974-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29974-129">INPUTS</span></span>

### <span data-ttu-id="29974-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29974-130">System.String</span></span>

## <span data-ttu-id="29974-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29974-131">OUTPUTS</span></span>

### <span data-ttu-id="29974-132">Microsoft. Azure. Command. Vault. models. Certificate</span><span class="sxs-lookup"><span data-stu-id="29974-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="29974-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29974-133">NOTES</span></span>

## <span data-ttu-id="29974-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29974-134">RELATED LINKS</span></span>

[<span data-ttu-id="29974-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="29974-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="29974-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="29974-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
