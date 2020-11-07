---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849994"
---
# <span data-ttu-id="89bf8-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="89bf8-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="89bf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="89bf8-103">A "memória" tanúsítvány rendszergazdája adatai objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="89bf8-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89bf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89bf8-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89bf8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="89bf8-106">A **New-AzureKeyVaultCertificateAdministratorDetails** parancsmag egy memóriabeli tanúsítvány-rendszergazdai részletek objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89bf8-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="89bf8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="89bf8-108">Példa 1: tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="89bf8-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="89bf8-109">A parancs a memória-tanúsítvány rendszergazdája adatai objektumot hozza létre, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="89bf8-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="89bf8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="89bf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bf8-111">-DefaultProfile</span></span>
<span data-ttu-id="89bf8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89bf8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89bf8-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="89bf8-113">-EmailAddress</span></span>
<span data-ttu-id="89bf8-114">A tanúsítvány rendszergazdája e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89bf8-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="89bf8-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="89bf8-115">-FirstName</span></span>
<span data-ttu-id="89bf8-116">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89bf8-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="89bf8-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="89bf8-117">-LastName</span></span>
<span data-ttu-id="89bf8-118">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89bf8-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="89bf8-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="89bf8-119">-PhoneNumber</span></span>
<span data-ttu-id="89bf8-120">A hitelességi tanúsítvány rendszergazdája által megadott telefonszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="89bf8-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="89bf8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89bf8-121">-Confirm</span></span>
<span data-ttu-id="89bf8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89bf8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89bf8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89bf8-123">-WhatIf</span></span>
<span data-ttu-id="89bf8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89bf8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89bf8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89bf8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89bf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bf8-126">CommonParameters</span></span>
<span data-ttu-id="89bf8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89bf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bf8-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89bf8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bf8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89bf8-129">INPUTS</span></span>

## <span data-ttu-id="89bf8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89bf8-130">OUTPUTS</span></span>

### <span data-ttu-id="89bf8-131">Microsoft. Azure. Command. KeyVaultCertificateAdministratorDetails. models.</span><span class="sxs-lookup"><span data-stu-id="89bf8-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="89bf8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89bf8-132">NOTES</span></span>

## <span data-ttu-id="89bf8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89bf8-133">RELATED LINKS</span></span>

[<span data-ttu-id="89bf8-134">Új – AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="89bf8-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

