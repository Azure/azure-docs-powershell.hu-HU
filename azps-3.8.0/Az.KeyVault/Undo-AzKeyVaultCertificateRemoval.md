---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846050"
---
# <span data-ttu-id="c9f7a-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="c9f7a-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="c9f7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f7a-103">Visszanyeri a törölt tanúsítványokat egy kulcsos boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="c9f7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9f7a-104">SYNTAX</span></span>

### <span data-ttu-id="c9f7a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9f7a-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f7a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f7a-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f7a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9f7a-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f7a-108">A **Visszavonás-AzKeyVaultCertificateRemoval** parancsmag egy korábban törölt tanúsítványt fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="c9f7a-109">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="c9f7a-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="c9f7a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c9f7a-111">EXAMPLES</span></span>

### <span data-ttu-id="c9f7a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9f7a-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="c9f7a-113">Ez a parancs visszaállítja a korábban törölt "MyCertificate" tanúsítványt aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="c9f7a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9f7a-114">PARAMETERS</span></span>

### <span data-ttu-id="c9f7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f7a-115">-DefaultProfile</span></span>
<span data-ttu-id="c9f7a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c9f7a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9f7a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f7a-117">-InputObject</span></span>
<span data-ttu-id="c9f7a-118">A törölt tanúsítvány objektum</span><span class="sxs-lookup"><span data-stu-id="c9f7a-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="c9f7a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9f7a-119">-Name</span></span>
<span data-ttu-id="c9f7a-120">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="c9f7a-120">Certificate name.</span></span>
<span data-ttu-id="c9f7a-121">Parancsmag: egy tanúsítvány teljes tartománynevét építi fel a Vault neve, a kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="c9f7a-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c9f7a-122">-VaultName</span></span>
<span data-ttu-id="c9f7a-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-123">Vault name.</span></span>
<span data-ttu-id="c9f7a-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c9f7a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9f7a-125">-Confirm</span></span>
<span data-ttu-id="c9f7a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f7a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f7a-127">-WhatIf</span></span>
<span data-ttu-id="c9f7a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f7a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f7a-130">CommonParameters</span></span>
<span data-ttu-id="c9f7a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9f7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f7a-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f7a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f7a-133">INPUTS</span></span>

### <span data-ttu-id="c9f7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c9f7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c9f7a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f7a-135">OUTPUTS</span></span>

### <span data-ttu-id="c9f7a-136">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="c9f7a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="c9f7a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9f7a-137">NOTES</span></span>

## <span data-ttu-id="c9f7a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9f7a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9f7a-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c9f7a-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="c9f7a-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c9f7a-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
