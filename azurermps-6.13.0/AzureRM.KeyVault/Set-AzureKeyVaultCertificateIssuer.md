---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493678"
---
# <span data-ttu-id="b3233-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b3233-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b3233-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3233-102">SYNOPSIS</span></span>
<span data-ttu-id="b3233-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="b3233-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3233-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3233-104">SYNTAX</span></span>

### <span data-ttu-id="b3233-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3233-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3233-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="b3233-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3233-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3233-107">DESCRIPTION</span></span>
<span data-ttu-id="b3233-108">A Set-AzureKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="b3233-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="b3233-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b3233-109">EXAMPLES</span></span>

### <span data-ttu-id="b3233-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="b3233-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="b3233-111">Ez a parancs beállítja a tanúsítvány-kiállítók tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b3233-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="b3233-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3233-112">PARAMETERS</span></span>

### <span data-ttu-id="b3233-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b3233-113">-AccountId</span></span>
<span data-ttu-id="b3233-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3233-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="b3233-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="b3233-115">-ApiKey</span></span>
<span data-ttu-id="b3233-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3233-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="b3233-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3233-117">-DefaultProfile</span></span>
<span data-ttu-id="b3233-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b3233-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3233-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3233-119">-InputObject</span></span>
<span data-ttu-id="b3233-120">Adja meg a beállítani kívánt tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b3233-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="b3233-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="b3233-121">-IssuerProvider</span></span>
<span data-ttu-id="b3233-122">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3233-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="b3233-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b3233-123">-Name</span></span>
<span data-ttu-id="b3233-124">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3233-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="b3233-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b3233-125">-OrganizationDetails</span></span>
<span data-ttu-id="b3233-126">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="b3233-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="b3233-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3233-127">-PassThru</span></span>
<span data-ttu-id="b3233-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b3233-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3233-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b3233-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3233-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3233-130">-VaultName</span></span>
<span data-ttu-id="b3233-131">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3233-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b3233-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3233-132">-Confirm</span></span>
<span data-ttu-id="b3233-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3233-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3233-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3233-134">-WhatIf</span></span>
<span data-ttu-id="b3233-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3233-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3233-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3233-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3233-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3233-137">CommonParameters</span></span>
<span data-ttu-id="b3233-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3233-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3233-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3233-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3233-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3233-140">INPUTS</span></span>

### <span data-ttu-id="b3233-141">Microsoft. Azure. Command. PSKeyVaultCertificateOrganizationDetails. models.</span><span class="sxs-lookup"><span data-stu-id="b3233-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="b3233-142">Paraméterek: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3233-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="b3233-143">Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="b3233-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="b3233-144">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3233-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b3233-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3233-145">OUTPUTS</span></span>

### <span data-ttu-id="b3233-146">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="b3233-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b3233-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3233-147">NOTES</span></span>

## <span data-ttu-id="b3233-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3233-148">RELATED LINKS</span></span>

[<span data-ttu-id="b3233-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b3233-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b3233-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b3233-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

