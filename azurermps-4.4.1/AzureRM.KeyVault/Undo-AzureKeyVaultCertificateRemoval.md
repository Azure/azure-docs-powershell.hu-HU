---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504088"
---
# <span data-ttu-id="e35c1-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="e35c1-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="e35c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e35c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e35c1-103">Visszanyeri a törölt tanúsítványokat egy kulcsos boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="e35c1-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e35c1-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e35c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e35c1-106">A **Visszavonás-AzureKeyVaultCertificateRemoval** parancsmag egy korábban törölt tanúsítványt fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="e35c1-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="e35c1-107">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="e35c1-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="e35c1-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="e35c1-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e35c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e35c1-109">EXAMPLES</span></span>

### <span data-ttu-id="e35c1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e35c1-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="e35c1-111">Ez a parancs visszaállítja a korábban törölt "MyCertificate" tanúsítványt aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="e35c1-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e35c1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e35c1-112">PARAMETERS</span></span>

### <span data-ttu-id="e35c1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e35c1-113">-Name</span></span>
<span data-ttu-id="e35c1-114">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="e35c1-114">Certificate name.</span></span>
<span data-ttu-id="e35c1-115">Parancsmag: egy tanúsítvány teljes tartománynevét építi fel a Vault neve, a kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="e35c1-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35c1-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e35c1-116">-VaultName</span></span>
<span data-ttu-id="e35c1-117">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="e35c1-117">Vault name.</span></span>
<span data-ttu-id="e35c1-118">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="e35c1-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35c1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e35c1-119">-Confirm</span></span>
<span data-ttu-id="e35c1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e35c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35c1-121">-WhatIf</span></span>
<span data-ttu-id="e35c1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e35c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35c1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e35c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35c1-124">-DefaultProfile</span></span>
<span data-ttu-id="e35c1-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e35c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e35c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35c1-126">CommonParameters</span></span>
<span data-ttu-id="e35c1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e35c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35c1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35c1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35c1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35c1-129">INPUTS</span></span>

### <span data-ttu-id="e35c1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e35c1-130">System.String</span></span>

## <span data-ttu-id="e35c1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35c1-131">OUTPUTS</span></span>

### <span data-ttu-id="e35c1-132">Microsoft. Azure. Command. Vault. models. Certificate</span><span class="sxs-lookup"><span data-stu-id="e35c1-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="e35c1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e35c1-133">NOTES</span></span>

## <span data-ttu-id="e35c1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e35c1-134">RELATED LINKS</span></span>

[<span data-ttu-id="e35c1-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e35c1-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e35c1-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e35c1-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
