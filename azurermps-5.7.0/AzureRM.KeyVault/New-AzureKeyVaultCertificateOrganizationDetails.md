---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 3ece43bb0c1d4c97c5d1956a25707c920215781c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505503"
---
# <span data-ttu-id="ddc37-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="ddc37-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="ddc37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddc37-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc37-103">Létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="ddc37-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddc37-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddc37-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc37-106">A **New-AzureKeyVaultCertificateOrganizationDetails** parancsmag létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="ddc37-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="ddc37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ddc37-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc37-108">Példa 1: szervezet adatai objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ddc37-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="ddc37-109">Az első parancs létrehoz egy tanúsítvány-rendszergazdai részletek objektumot, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ddc37-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="ddc37-110">A második parancs létrehoz egy Certificate Organization details objektumot, majd a $OrgDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ddc37-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="ddc37-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddc37-111">PARAMETERS</span></span>

### <span data-ttu-id="ddc37-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ddc37-112">-AdministratorDetails</span></span>
<span data-ttu-id="ddc37-113">A tanúsítványok szervezeti rendszergazdáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddc37-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc37-114">-DefaultProfile</span></span>
<span data-ttu-id="ddc37-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ddc37-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddc37-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ddc37-116">-Id</span></span>
<span data-ttu-id="ddc37-117">A szervezet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddc37-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="ddc37-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddc37-118">-Confirm</span></span>
<span data-ttu-id="ddc37-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddc37-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc37-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc37-120">-WhatIf</span></span>
<span data-ttu-id="ddc37-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddc37-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc37-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddc37-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc37-123">CommonParameters</span></span>
<span data-ttu-id="ddc37-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddc37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc37-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc37-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc37-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddc37-126">INPUTS</span></span>

### <span data-ttu-id="ddc37-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ddc37-127">None</span></span>
<span data-ttu-id="ddc37-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ddc37-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ddc37-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddc37-129">OUTPUTS</span></span>

### <span data-ttu-id="ddc37-130">Microsoft. Azure. Command. PSKeyVaultCertificateOrganizationDetails. models.</span><span class="sxs-lookup"><span data-stu-id="ddc37-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="ddc37-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddc37-131">NOTES</span></span>

## <span data-ttu-id="ddc37-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddc37-132">RELATED LINKS</span></span>

[<span data-ttu-id="ddc37-133">Új – AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ddc37-133">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

