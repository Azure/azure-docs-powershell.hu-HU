---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504411"
---
# <span data-ttu-id="e26c5-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="e26c5-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="e26c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e26c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e26c5-103">Visszanyeri a törölt tanúsítványokat egy kulcsos boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="e26c5-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e26c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e26c5-104">SYNTAX</span></span>

### <span data-ttu-id="e26c5-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e26c5-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e26c5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e26c5-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e26c5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e26c5-107">DESCRIPTION</span></span>
<span data-ttu-id="e26c5-108">A **Visszavonás-AzureKeyVaultCertificateRemoval** parancsmag egy korábban törölt tanúsítványt fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="e26c5-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="e26c5-109">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="e26c5-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="e26c5-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="e26c5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e26c5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e26c5-111">EXAMPLES</span></span>

### <span data-ttu-id="e26c5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e26c5-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="e26c5-113">Ez a parancs visszaállítja a korábban törölt "MyCertificate" tanúsítványt aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="e26c5-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e26c5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e26c5-114">PARAMETERS</span></span>

### <span data-ttu-id="e26c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26c5-115">-DefaultProfile</span></span>
<span data-ttu-id="e26c5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e26c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e26c5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e26c5-117">-InputObject</span></span>
<span data-ttu-id="e26c5-118">A törölt tanúsítvány objektum</span><span class="sxs-lookup"><span data-stu-id="e26c5-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e26c5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e26c5-119">-Name</span></span>
<span data-ttu-id="e26c5-120">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="e26c5-120">Certificate name.</span></span>
<span data-ttu-id="e26c5-121">Parancsmag: egy tanúsítvány teljes tartománynevét építi fel a Vault neve, a kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="e26c5-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26c5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e26c5-122">-VaultName</span></span>
<span data-ttu-id="e26c5-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="e26c5-123">Vault name.</span></span>
<span data-ttu-id="e26c5-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="e26c5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26c5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e26c5-125">-Confirm</span></span>
<span data-ttu-id="e26c5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e26c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e26c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e26c5-127">-WhatIf</span></span>
<span data-ttu-id="e26c5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e26c5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e26c5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e26c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e26c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26c5-130">CommonParameters</span></span>
<span data-ttu-id="e26c5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e26c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26c5-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26c5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26c5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e26c5-133">INPUTS</span></span>

### <span data-ttu-id="e26c5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e26c5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="e26c5-135">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e26c5-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e26c5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e26c5-136">OUTPUTS</span></span>

### <span data-ttu-id="e26c5-137">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="e26c5-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="e26c5-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e26c5-138">NOTES</span></span>

## <span data-ttu-id="e26c5-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e26c5-139">RELATED LINKS</span></span>

[<span data-ttu-id="e26c5-140">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26c5-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e26c5-141">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e26c5-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
