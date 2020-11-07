---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 430a909e76c08ba0c19c18072fdf019cd2fa7b29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849650"
---
# <span data-ttu-id="5d087-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5d087-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5d087-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d087-102">SYNOPSIS</span></span>
<span data-ttu-id="5d087-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="5d087-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d087-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d087-104">SYNTAX</span></span>

### <span data-ttu-id="5d087-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d087-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d087-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="5d087-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d087-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d087-107">DESCRIPTION</span></span>
<span data-ttu-id="5d087-108">A Set-AzureKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="5d087-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="5d087-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5d087-109">EXAMPLES</span></span>

### <span data-ttu-id="5d087-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="5d087-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="5d087-111">Ez a parancs beállítja a tanúsítvány kiállító tulajdonságait, majd a $Issuer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d087-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="5d087-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d087-112">PARAMETERS</span></span>

### <span data-ttu-id="5d087-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5d087-113">-AccountId</span></span>
<span data-ttu-id="5d087-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d087-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="5d087-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="5d087-115">-ApiKey</span></span>
<span data-ttu-id="5d087-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d087-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="5d087-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d087-117">-DefaultProfile</span></span>
<span data-ttu-id="5d087-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d087-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d087-119">-A kibocsátás</span><span class="sxs-lookup"><span data-stu-id="5d087-119">-Issuer</span></span>
<span data-ttu-id="5d087-120">A frissítendő tanúsítvány kijavítása.</span><span class="sxs-lookup"><span data-stu-id="5d087-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d087-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="5d087-121">-IssuerProvider</span></span>
<span data-ttu-id="5d087-122">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d087-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="5d087-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d087-123">-Name</span></span>
<span data-ttu-id="5d087-124">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d087-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="5d087-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="5d087-125">-OrganizationDetails</span></span>
<span data-ttu-id="5d087-126">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="5d087-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d087-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d087-127">-PassThru</span></span>
<span data-ttu-id="5d087-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5d087-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5d087-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5d087-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d087-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5d087-130">-VaultName</span></span>
<span data-ttu-id="5d087-131">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d087-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="5d087-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d087-132">-Confirm</span></span>
<span data-ttu-id="5d087-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d087-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d087-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d087-134">-WhatIf</span></span>
<span data-ttu-id="5d087-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d087-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d087-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d087-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d087-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d087-137">CommonParameters</span></span>
<span data-ttu-id="5d087-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d087-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d087-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d087-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d087-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d087-140">INPUTS</span></span>

## <span data-ttu-id="5d087-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d087-141">OUTPUTS</span></span>

### <span data-ttu-id="5d087-142">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="5d087-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5d087-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d087-143">NOTES</span></span>

## <span data-ttu-id="5d087-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d087-144">RELATED LINKS</span></span>

[<span data-ttu-id="5d087-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5d087-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="5d087-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5d087-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

