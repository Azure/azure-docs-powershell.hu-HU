---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 01d0718e4efeae093b7bd9ed4fc2c6bca4cf7f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680707"
---
# <span data-ttu-id="2b3c3-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="2b3c3-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="2b3c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3c3-103">A "memória" tanúsítvány rendszergazdája adatai objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b3c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b3c3-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b3c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b3c3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3c3-106">A **New-AzureKeyVaultCertificateAdministratorDetails** parancsmag egy memóriabeli tanúsítvány-rendszergazdai részletek objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="2b3c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b3c3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3c3-108">Példa 1: tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="2b3c3-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="2b3c3-109">A parancs a memória-tanúsítvány rendszergazdája adatai objektumot hozza létre, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="2b3c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b3c3-110">PARAMETERS</span></span>

### <span data-ttu-id="2b3c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3c3-111">-DefaultProfile</span></span>
<span data-ttu-id="2b3c3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b3c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b3c3-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="2b3c3-113">-EmailAddress</span></span>
<span data-ttu-id="2b3c3-114">A tanúsítvány rendszergazdája e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3c3-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="2b3c3-115">-FirstName</span></span>
<span data-ttu-id="2b3c3-116">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3c3-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="2b3c3-117">-LastName</span></span>
<span data-ttu-id="2b3c3-118">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3c3-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2b3c3-119">-PhoneNumber</span></span>
<span data-ttu-id="2b3c3-120">A hitelességi tanúsítvány rendszergazdája által megadott telefonszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3c3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b3c3-121">-Confirm</span></span>
<span data-ttu-id="2b3c3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b3c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3c3-123">-WhatIf</span></span>
<span data-ttu-id="2b3c3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3c3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b3c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3c3-126">CommonParameters</span></span>
<span data-ttu-id="2b3c3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b3c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3c3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3c3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b3c3-129">INPUTS</span></span>

### <span data-ttu-id="2b3c3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b3c3-130">None</span></span>
<span data-ttu-id="2b3c3-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b3c3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b3c3-132">OUTPUTS</span></span>

### <span data-ttu-id="2b3c3-133">Microsoft. Azure. Command. PSKeyVaultCertificateAdministratorDetails. models.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="2b3c3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b3c3-134">NOTES</span></span>

## <span data-ttu-id="2b3c3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b3c3-135">RELATED LINKS</span></span>

[<span data-ttu-id="2b3c3-136">Új – AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2b3c3-136">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

