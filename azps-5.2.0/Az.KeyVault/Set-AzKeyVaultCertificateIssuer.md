---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334134"
---
# <span data-ttu-id="1ae90-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1ae90-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1ae90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae90-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae90-103">Egy kulcstárolóban beállítja a tanúsítvány kibocsátóját.</span><span class="sxs-lookup"><span data-stu-id="1ae90-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1ae90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ae90-104">SYNTAX</span></span>

### <span data-ttu-id="1ae90-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ae90-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae90-106">Érték szerint</span><span class="sxs-lookup"><span data-stu-id="1ae90-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae90-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ae90-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae90-108">A Set-AzKeyVaultCertificateIssuer parancsmag egy kulcstárolóban állítja be a tanúsítvány kibocsátóját.</span><span class="sxs-lookup"><span data-stu-id="1ae90-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1ae90-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ae90-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae90-110">1. példa: Tanúsítvány kibocsátójának beállítása</span><span class="sxs-lookup"><span data-stu-id="1ae90-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="1ae90-111">Ez a parancs beállítja egy tanúsítvány kibocsátójának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1ae90-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="1ae90-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ae90-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae90-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1ae90-113">-AccountId</span></span>
<span data-ttu-id="1ae90-114">A tanúsítvány kibocsátójának számlaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="1ae90-115">-ApiKey</span></span>
<span data-ttu-id="1ae90-116">A tanúsítvány kibocsátójának API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae90-117">-DefaultProfile</span></span>
<span data-ttu-id="1ae90-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ae90-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ae90-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ae90-119">-InputObject</span></span>
<span data-ttu-id="1ae90-120">A beállítani szükséges tanúsítvány kibocsátóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="1ae90-121">-IssuerProvider</span></span>
<span data-ttu-id="1ae90-122">A tanúsítvány kibocsátójának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae90-123">-Name</span></span>
<span data-ttu-id="1ae90-124">A kibocsátó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1ae90-125">-OrganizationDetails</span></span>
<span data-ttu-id="1ae90-126">A kibocsátóval együtt használható szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="1ae90-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ae90-127">-PassThru</span></span>
<span data-ttu-id="1ae90-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="1ae90-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1ae90-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1ae90-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ae90-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1ae90-130">-VaultName</span></span>
<span data-ttu-id="1ae90-131">A kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ae90-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae90-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ae90-132">-Confirm</span></span>
<span data-ttu-id="1ae90-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ae90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae90-134">-WhatIf</span></span>
<span data-ttu-id="1ae90-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ae90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae90-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ae90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae90-137">CommonParameters</span></span>
<span data-ttu-id="1ae90-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae90-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ae90-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae90-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ae90-140">INPUTS</span></span>

### <span data-ttu-id="1ae90-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1ae90-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="1ae90-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1ae90-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="1ae90-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae90-143">OUTPUTS</span></span>

### <span data-ttu-id="1ae90-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1ae90-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1ae90-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ae90-145">NOTES</span></span>

## <span data-ttu-id="1ae90-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ae90-146">RELATED LINKS</span></span>

[<span data-ttu-id="1ae90-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1ae90-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="1ae90-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1ae90-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

