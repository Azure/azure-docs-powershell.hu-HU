---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842130"
---
# <span data-ttu-id="ead49-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ead49-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="ead49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ead49-102">SYNOPSIS</span></span>
<span data-ttu-id="ead49-103">A "memória" tanúsítvány rendszergazdája adatai objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ead49-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="ead49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ead49-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ead49-105">DESCRIPTION</span></span>
<span data-ttu-id="ead49-106">A **New-AzKeyVaultCertificateAdministratorDetails** parancsmag egy memóriabeli tanúsítvány-rendszergazdai részletek objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ead49-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="ead49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ead49-107">EXAMPLES</span></span>

### <span data-ttu-id="ead49-108">Példa 1: tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ead49-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="ead49-109">A parancs a memória-tanúsítvány rendszergazdája adatai objektumot hozza létre, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ead49-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="ead49-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ead49-110">PARAMETERS</span></span>

### <span data-ttu-id="ead49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead49-111">-DefaultProfile</span></span>
<span data-ttu-id="ead49-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ead49-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ead49-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ead49-113">-EmailAddress</span></span>
<span data-ttu-id="ead49-114">A tanúsítvány rendszergazdája e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ead49-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="ead49-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="ead49-115">-FirstName</span></span>
<span data-ttu-id="ead49-116">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ead49-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ead49-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="ead49-117">-LastName</span></span>
<span data-ttu-id="ead49-118">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ead49-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ead49-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="ead49-119">-PhoneNumber</span></span>
<span data-ttu-id="ead49-120">A hitelességi tanúsítvány rendszergazdája által megadott telefonszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ead49-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="ead49-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ead49-121">-Confirm</span></span>
<span data-ttu-id="ead49-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ead49-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead49-123">-WhatIf</span></span>
<span data-ttu-id="ead49-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ead49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead49-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ead49-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead49-126">CommonParameters</span></span>
<span data-ttu-id="ead49-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ead49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead49-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead49-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead49-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ead49-129">INPUTS</span></span>

### <span data-ttu-id="ead49-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ead49-130">None</span></span>
<span data-ttu-id="ead49-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ead49-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ead49-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ead49-132">OUTPUTS</span></span>

### <span data-ttu-id="ead49-133">Microsoft. Azure. Command. KeyVaultCertificateAdministratorDetails. models.</span><span class="sxs-lookup"><span data-stu-id="ead49-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="ead49-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ead49-134">NOTES</span></span>

## <span data-ttu-id="ead49-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ead49-135">RELATED LINKS</span></span>

[<span data-ttu-id="ead49-136">Új – AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="ead49-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

