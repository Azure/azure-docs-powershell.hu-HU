---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: fdb90d670034e87c4a08c316b73d4bd15614d872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835658"
---
# <span data-ttu-id="4e1e0-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4e1e0-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4e1e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1e0-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="4e1e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e1e0-104">SYNTAX</span></span>

### <span data-ttu-id="4e1e0-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e1e0-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e1e0-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="4e1e0-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e1e0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="4e1e0-108">A Set-AzKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="4e1e0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4e1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="4e1e0-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="4e1e0-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="4e1e0-111">Ez a parancs beállítja a tanúsítvány-kiállítók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="4e1e0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e1e0-112">PARAMETERS</span></span>

### <span data-ttu-id="4e1e0-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="4e1e0-113">-AccountId</span></span>
<span data-ttu-id="4e1e0-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="4e1e0-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="4e1e0-115">-ApiKey</span></span>
<span data-ttu-id="4e1e0-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="4e1e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1e0-117">-DefaultProfile</span></span>
<span data-ttu-id="4e1e0-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e1e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e1e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e1e0-119">-InputObject</span></span>
<span data-ttu-id="4e1e0-120">Adja meg a beállítani kívánt tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="4e1e0-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="4e1e0-121">-IssuerProvider</span></span>
<span data-ttu-id="4e1e0-122">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="4e1e0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e1e0-123">-Name</span></span>
<span data-ttu-id="4e1e0-124">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="4e1e0-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="4e1e0-125">-OrganizationDetails</span></span>
<span data-ttu-id="4e1e0-126">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="4e1e0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e1e0-127">-PassThru</span></span>
<span data-ttu-id="4e1e0-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e1e0-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e1e0-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4e1e0-130">-VaultName</span></span>
<span data-ttu-id="4e1e0-131">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="4e1e0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e1e0-132">-Confirm</span></span>
<span data-ttu-id="4e1e0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e1e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e1e0-134">-WhatIf</span></span>
<span data-ttu-id="4e1e0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e1e0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e1e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1e0-137">CommonParameters</span></span>
<span data-ttu-id="4e1e0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e1e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1e0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e1e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1e0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e1e0-140">INPUTS</span></span>

### <span data-ttu-id="4e1e0-141">Microsoft. Azure. Command. PSKeyVaultCertificateOrganizationDetails. models.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="4e1e0-142">Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="4e1e0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e1e0-143">OUTPUTS</span></span>

### <span data-ttu-id="4e1e0-144">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4e1e0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e1e0-145">NOTES</span></span>

## <span data-ttu-id="4e1e0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e1e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="4e1e0-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4e1e0-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4e1e0-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4e1e0-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

