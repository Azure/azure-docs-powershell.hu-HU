---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504555"
---
# <span data-ttu-id="9a8ba-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a8ba-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9a8ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8ba-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a8ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a8ba-104">SYNTAX</span></span>

### <span data-ttu-id="9a8ba-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a8ba-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8ba-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="9a8ba-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a8ba-107">DESCRIPTION</span></span>
<span data-ttu-id="9a8ba-108">A Set-AzureKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="9a8ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9a8ba-109">EXAMPLES</span></span>

### <span data-ttu-id="9a8ba-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="9a8ba-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="9a8ba-111">Ez a parancs beállítja a tanúsítvány kiállító tulajdonságait, majd a $Issuer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="9a8ba-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a8ba-112">PARAMETERS</span></span>

### <span data-ttu-id="9a8ba-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="9a8ba-113">-AccountId</span></span>
<span data-ttu-id="9a8ba-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="9a8ba-115">-ApiKey</span></span>
<span data-ttu-id="9a8ba-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8ba-117">-DefaultProfile</span></span>
<span data-ttu-id="9a8ba-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a8ba-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a8ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a8ba-119">-InputObject</span></span>
<span data-ttu-id="9a8ba-120">Adja meg a beállítani kívánt tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="9a8ba-121">-IssuerProvider</span></span>
<span data-ttu-id="9a8ba-122">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a8ba-123">-Name</span></span>
<span data-ttu-id="9a8ba-124">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="9a8ba-125">-OrganizationDetails</span></span>
<span data-ttu-id="9a8ba-126">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a8ba-127">-PassThru</span></span>
<span data-ttu-id="9a8ba-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a8ba-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ba-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a8ba-130">-VaultName</span></span>
<span data-ttu-id="9a8ba-131">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="9a8ba-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a8ba-132">-Confirm</span></span>
<span data-ttu-id="9a8ba-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8ba-134">-WhatIf</span></span>
<span data-ttu-id="9a8ba-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8ba-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8ba-137">CommonParameters</span></span>
<span data-ttu-id="9a8ba-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a8ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8ba-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8ba-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8ba-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a8ba-140">INPUTS</span></span>

### <span data-ttu-id="9a8ba-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a8ba-141">None</span></span>
<span data-ttu-id="9a8ba-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a8ba-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a8ba-143">OUTPUTS</span></span>

### <span data-ttu-id="9a8ba-144">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9a8ba-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a8ba-145">NOTES</span></span>

## <span data-ttu-id="9a8ba-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a8ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a8ba-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a8ba-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9a8ba-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a8ba-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

