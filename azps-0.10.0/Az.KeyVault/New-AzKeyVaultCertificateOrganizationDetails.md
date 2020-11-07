---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843885"
---
# <span data-ttu-id="94b7d-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="94b7d-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="94b7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="94b7d-103">Létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="94b7d-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="94b7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94b7d-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="94b7d-106">A **New-AzKeyVaultCertificateOrganizationDetails** parancsmag létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="94b7d-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="94b7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="94b7d-108">Példa 1: szervezet adatai objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="94b7d-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="94b7d-109">Az első parancs létrehoz egy tanúsítvány-rendszergazdai részletek objektumot, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="94b7d-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="94b7d-110">A második parancs létrehoz egy Certificate Organization details objektumot, majd a $OrgDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="94b7d-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="94b7d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94b7d-111">PARAMETERS</span></span>

### <span data-ttu-id="94b7d-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="94b7d-112">-AdministratorDetails</span></span>
<span data-ttu-id="94b7d-113">A tanúsítványok szervezeti rendszergazdáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b7d-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b7d-114">-DefaultProfile</span></span>
<span data-ttu-id="94b7d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="94b7d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94b7d-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="94b7d-116">-Id</span></span>
<span data-ttu-id="94b7d-117">A szervezet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b7d-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="94b7d-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94b7d-118">-Confirm</span></span>
<span data-ttu-id="94b7d-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94b7d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b7d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b7d-120">-WhatIf</span></span>
<span data-ttu-id="94b7d-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94b7d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b7d-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94b7d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b7d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b7d-123">CommonParameters</span></span>
<span data-ttu-id="94b7d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94b7d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b7d-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b7d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b7d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94b7d-126">INPUTS</span></span>

### <span data-ttu-id="94b7d-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="94b7d-127">None</span></span>
<span data-ttu-id="94b7d-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="94b7d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94b7d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94b7d-129">OUTPUTS</span></span>

### <span data-ttu-id="94b7d-130">Microsoft. Azure. Command. KeyVaultCertificateOrganizationDetails. models.</span><span class="sxs-lookup"><span data-stu-id="94b7d-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="94b7d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94b7d-131">NOTES</span></span>

## <span data-ttu-id="94b7d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94b7d-132">RELATED LINKS</span></span>

[<span data-ttu-id="94b7d-133">Új – AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="94b7d-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

