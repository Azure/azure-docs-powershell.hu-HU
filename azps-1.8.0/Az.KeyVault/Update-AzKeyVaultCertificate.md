---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 7c3ad97a2896104d9c60c1e24b7ea844b3a090a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835614"
---
# <span data-ttu-id="791c4-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="791c4-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="791c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="791c4-102">SYNOPSIS</span></span>
<span data-ttu-id="791c4-103">Módosítja a tanúsítványok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="791c4-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="791c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="791c4-104">SYNTAX</span></span>

### <span data-ttu-id="791c4-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="791c4-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="791c4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="791c4-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="791c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="791c4-107">DESCRIPTION</span></span>
<span data-ttu-id="791c4-108">Az **Update-AzKeyVaultCertificate** parancsmag módosította a tanúsítványok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="791c4-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="791c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="791c4-109">EXAMPLES</span></span>

### <span data-ttu-id="791c4-110">Példa 1: a tanúsítvánnyal társított címkék módosítása</span><span class="sxs-lookup"><span data-stu-id="791c4-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="791c4-111">Az első parancs kulcs/érték párok tömbjét rendeli hozzá a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="791c4-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="791c4-112">A második parancs beállítja a TestCert01 nevű tanúsítvány címkék értékét $Tags.</span><span class="sxs-lookup"><span data-stu-id="791c4-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="791c4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="791c4-113">PARAMETERS</span></span>

### <span data-ttu-id="791c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791c4-114">-DefaultProfile</span></span>
<span data-ttu-id="791c4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="791c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="791c4-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="791c4-116">-Enable</span></span>
<span data-ttu-id="791c4-117">Ha van, engedélyezze a tanúsítványt, ha az érték igaz.</span><span class="sxs-lookup"><span data-stu-id="791c4-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="791c4-118">Tanúsítvány letiltása, ha az érték hamis.</span><span class="sxs-lookup"><span data-stu-id="791c4-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="791c4-119">Ha nem adja meg, akkor a tanúsítvány engedélyezett/letiltott állapotának meglévő értéke változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="791c4-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="791c4-120">-InputObject</span></span>
<span data-ttu-id="791c4-121">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="791c4-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="791c4-122">-Name</span></span>
<span data-ttu-id="791c4-123">Tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="791c4-123">Certificate name.</span></span>
<span data-ttu-id="791c4-124">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="791c4-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="791c4-125">-PassThru</span></span>
<span data-ttu-id="791c4-126">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="791c4-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="791c4-127">Ha ez a kapcsoló van megadva, a Return Certificate objektum.</span><span class="sxs-lookup"><span data-stu-id="791c4-127">If this switch is specified, return certificate object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="791c4-128">-Tag</span></span>
<span data-ttu-id="791c4-129">A Hashtable képviselő címke.</span><span class="sxs-lookup"><span data-stu-id="791c4-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="791c4-130">Ha nem adja meg, akkor a sertificate meglévő címkéi változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="791c4-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="791c4-131">Címke eltávolítása: üres Hashtable megadásával.</span><span class="sxs-lookup"><span data-stu-id="791c4-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="791c4-132">-VaultName</span></span>
<span data-ttu-id="791c4-133">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="791c4-133">Vault name.</span></span>
<span data-ttu-id="791c4-134">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="791c4-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-135">-Verzió</span><span class="sxs-lookup"><span data-stu-id="791c4-135">-Version</span></span>
<span data-ttu-id="791c4-136">Tanúsítvány verziója.</span><span class="sxs-lookup"><span data-stu-id="791c4-136">Certificate version.</span></span>
<span data-ttu-id="791c4-137">Parancsmag: egy tanúsítvány teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi ki.</span><span class="sxs-lookup"><span data-stu-id="791c4-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791c4-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="791c4-138">-Confirm</span></span>
<span data-ttu-id="791c4-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="791c4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="791c4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791c4-140">-WhatIf</span></span>
<span data-ttu-id="791c4-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="791c4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="791c4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="791c4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="791c4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791c4-143">CommonParameters</span></span>
<span data-ttu-id="791c4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="791c4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791c4-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791c4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791c4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="791c4-146">INPUTS</span></span>

### <span data-ttu-id="791c4-147">Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="791c4-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="791c4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="791c4-148">OUTPUTS</span></span>

### <span data-ttu-id="791c4-149">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="791c4-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="791c4-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="791c4-150">NOTES</span></span>

## <span data-ttu-id="791c4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="791c4-151">RELATED LINKS</span></span>
