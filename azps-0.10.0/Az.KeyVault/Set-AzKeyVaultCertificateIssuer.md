---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843862"
---
# <span data-ttu-id="5abe7-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5abe7-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5abe7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5abe7-102">SYNOPSIS</span></span>
<span data-ttu-id="5abe7-103">Tanúsítvány-gyártót állít be a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="5abe7-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="5abe7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5abe7-104">SYNTAX</span></span>

### <span data-ttu-id="5abe7-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5abe7-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5abe7-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="5abe7-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5abe7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5abe7-107">DESCRIPTION</span></span>
<span data-ttu-id="5abe7-108">A Set-AzKeyVaultCertificateIssuer parancsmag a tanúsítvány kibocsátását a kulcs boltozatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="5abe7-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="5abe7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5abe7-109">EXAMPLES</span></span>

### <span data-ttu-id="5abe7-110">1. példa: tanúsítvány-kibocsátási beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="5abe7-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="5abe7-111">Ez a parancs beállítja a tanúsítvány kiállító tulajdonságait, majd a $Issuer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5abe7-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="5abe7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5abe7-112">PARAMETERS</span></span>

### <span data-ttu-id="5abe7-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5abe7-113">-AccountId</span></span>
<span data-ttu-id="5abe7-114">A tanúsítvány-leadási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5abe7-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="5abe7-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="5abe7-115">-ApiKey</span></span>
<span data-ttu-id="5abe7-116">A tanúsítvány-kibocsátási API-kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5abe7-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="5abe7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abe7-117">-DefaultProfile</span></span>
<span data-ttu-id="5abe7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5abe7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abe7-119">-A kibocsátás</span><span class="sxs-lookup"><span data-stu-id="5abe7-119">-Issuer</span></span>
<span data-ttu-id="5abe7-120">A frissítendő tanúsítvány kijavítása.</span><span class="sxs-lookup"><span data-stu-id="5abe7-120">Specifies the certificate issuer to update.</span></span>

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

### <span data-ttu-id="5abe7-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="5abe7-121">-IssuerProvider</span></span>
<span data-ttu-id="5abe7-122">A tanúsítvány-kibocsátási típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="5abe7-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="5abe7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5abe7-123">-Name</span></span>
<span data-ttu-id="5abe7-124">A leválasztó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5abe7-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="5abe7-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="5abe7-125">-OrganizationDetails</span></span>
<span data-ttu-id="5abe7-126">A jogszolgáltatónál használatos szervezeti adatok.</span><span class="sxs-lookup"><span data-stu-id="5abe7-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="5abe7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5abe7-127">-PassThru</span></span>
<span data-ttu-id="5abe7-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5abe7-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5abe7-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5abe7-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5abe7-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5abe7-130">-VaultName</span></span>
<span data-ttu-id="5abe7-131">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5abe7-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="5abe7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5abe7-132">-Confirm</span></span>
<span data-ttu-id="5abe7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5abe7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5abe7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5abe7-134">-WhatIf</span></span>
<span data-ttu-id="5abe7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5abe7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5abe7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5abe7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5abe7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abe7-137">CommonParameters</span></span>
<span data-ttu-id="5abe7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5abe7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abe7-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5abe7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abe7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5abe7-140">INPUTS</span></span>

### <span data-ttu-id="5abe7-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="5abe7-141">None</span></span>
<span data-ttu-id="5abe7-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5abe7-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5abe7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5abe7-143">OUTPUTS</span></span>

### <span data-ttu-id="5abe7-144">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="5abe7-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5abe7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5abe7-145">NOTES</span></span>

## <span data-ttu-id="5abe7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5abe7-146">RELATED LINKS</span></span>

[<span data-ttu-id="5abe7-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5abe7-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="5abe7-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5abe7-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

