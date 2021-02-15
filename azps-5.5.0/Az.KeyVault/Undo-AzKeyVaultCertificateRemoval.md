---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152690"
---
# <span data-ttu-id="fceba-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="fceba-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="fceba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fceba-102">SYNOPSIS</span></span>
<span data-ttu-id="fceba-103">Egy kulcstároló törölt tanúsítványát aktív állapotba visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="fceba-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="fceba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fceba-104">SYNTAX</span></span>

### <span data-ttu-id="fceba-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fceba-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fceba-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fceba-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fceba-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fceba-107">DESCRIPTION</span></span>
<span data-ttu-id="fceba-108">Az **Undo-AzKeyVaultCertificateRemoval** parancsmag helyreállít egy korábban törölt tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="fceba-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="fceba-109">A helyreállított tanúsítvány aktív lesz, és minden művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="fceba-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="fceba-110">A művelet végrehajtásához a hívónak "helyreállítás" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="fceba-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fceba-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fceba-111">EXAMPLES</span></span>

### <span data-ttu-id="fceba-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="fceba-112">Example 1</span></span>
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

<span data-ttu-id="fceba-113">Ez a parancs aktív és használható állapotba visszaállítja a korábban törölt MyCertificate tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="fceba-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fceba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fceba-114">PARAMETERS</span></span>

### <span data-ttu-id="fceba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fceba-115">-DefaultProfile</span></span>
<span data-ttu-id="fceba-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fceba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fceba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fceba-117">-InputObject</span></span>
<span data-ttu-id="fceba-118">Törölt tanúsítvány objektum</span><span class="sxs-lookup"><span data-stu-id="fceba-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="fceba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fceba-119">-Name</span></span>
<span data-ttu-id="fceba-120">Tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="fceba-120">Certificate name.</span></span>
<span data-ttu-id="fceba-121">A parancsmag egy tanúsítvány teljes tartománynevét (FQDN) építi fel a tároló nevéből, amely jelenleg ki van jelölve a környezetben és a tanúsítványnévben.</span><span class="sxs-lookup"><span data-stu-id="fceba-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="fceba-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fceba-122">-VaultName</span></span>
<span data-ttu-id="fceba-123">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="fceba-123">Vault name.</span></span>
<span data-ttu-id="fceba-124">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="fceba-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fceba-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fceba-125">-Confirm</span></span>
<span data-ttu-id="fceba-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fceba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fceba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fceba-127">-WhatIf</span></span>
<span data-ttu-id="fceba-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fceba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fceba-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fceba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fceba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fceba-130">CommonParameters</span></span>
<span data-ttu-id="fceba-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fceba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fceba-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fceba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fceba-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fceba-133">INPUTS</span></span>

### <span data-ttu-id="fceba-134">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fceba-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="fceba-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fceba-135">OUTPUTS</span></span>

### <span data-ttu-id="fceba-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fceba-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="fceba-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fceba-137">NOTES</span></span>

## <span data-ttu-id="fceba-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fceba-138">RELATED LINKS</span></span>

[<span data-ttu-id="fceba-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fceba-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="fceba-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fceba-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
