---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500015"
---
# <span data-ttu-id="a5291-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a5291-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a5291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5291-102">SYNOPSIS</span></span>
<span data-ttu-id="a5291-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="a5291-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5291-104">SYNTAX</span></span>

### <span data-ttu-id="a5291-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5291-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5291-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="a5291-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5291-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5291-107">DESCRIPTION</span></span>
<span data-ttu-id="a5291-108">A Set-AzureKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="a5291-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="a5291-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5291-109">EXAMPLES</span></span>

### <span data-ttu-id="a5291-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="a5291-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="a5291-111">Ez a parancs beállítja a tanúsítvány kiállító tulajdonságait, majd a $Issuer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5291-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="a5291-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5291-112">PARAMETERS</span></span>

### <span data-ttu-id="a5291-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="a5291-113">-AccountId</span></span>
<span data-ttu-id="a5291-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5291-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="a5291-115">-ApiKey</span></span>
<span data-ttu-id="a5291-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5291-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-117">-A kibocsátás</span><span class="sxs-lookup"><span data-stu-id="a5291-117">-Issuer</span></span>
<span data-ttu-id="a5291-118">A frissítendő tanúsítvány kijavítása.</span><span class="sxs-lookup"><span data-stu-id="a5291-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="a5291-119">-IssuerProvider</span></span>
<span data-ttu-id="a5291-120">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5291-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5291-121">-Name</span></span>
<span data-ttu-id="a5291-122">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5291-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a5291-123">-OrganizationDetails</span></span>
<span data-ttu-id="a5291-124">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="a5291-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5291-125">-PassThru</span></span>
<span data-ttu-id="a5291-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a5291-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5291-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a5291-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5291-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5291-128">-VaultName</span></span>
<span data-ttu-id="a5291-129">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5291-129">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5291-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5291-130">-Confirm</span></span>
<span data-ttu-id="a5291-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5291-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5291-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5291-132">-WhatIf</span></span>
<span data-ttu-id="a5291-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5291-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5291-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5291-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5291-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5291-135">-DefaultProfile</span></span>
<span data-ttu-id="a5291-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5291-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5291-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5291-137">CommonParameters</span></span>
<span data-ttu-id="a5291-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5291-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5291-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5291-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5291-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5291-140">INPUTS</span></span>

## <span data-ttu-id="a5291-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5291-141">OUTPUTS</span></span>

### <span data-ttu-id="a5291-142">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="a5291-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a5291-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5291-143">NOTES</span></span>

## <span data-ttu-id="a5291-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5291-144">RELATED LINKS</span></span>

[<span data-ttu-id="a5291-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a5291-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a5291-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a5291-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

