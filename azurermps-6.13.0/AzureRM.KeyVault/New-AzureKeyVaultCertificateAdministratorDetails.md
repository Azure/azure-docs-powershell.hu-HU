---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 7af47e41d019c758ff3810c8cf1fa08fc305fead
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679551"
---
# <span data-ttu-id="6e8a5-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="6e8a5-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="6e8a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8a5-103">A "memória" tanúsítvány rendszergazdája adatai objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e8a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e8a5-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8a5-106">A **New-AzureKeyVaultCertificateAdministratorDetails** parancsmag egy memóriabeli tanúsítvány-rendszergazdai részletek objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="6e8a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e8a5-107">EXAMPLES</span></span>

### <span data-ttu-id="6e8a5-108">Példa 1: tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="6e8a5-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="6e8a5-109">A parancs a memória-tanúsítvány rendszergazdája adatai objektumot hozza létre, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="6e8a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e8a5-110">PARAMETERS</span></span>

### <span data-ttu-id="6e8a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8a5-111">-DefaultProfile</span></span>
<span data-ttu-id="6e8a5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e8a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e8a5-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6e8a5-113">-EmailAddress</span></span>
<span data-ttu-id="6e8a5-114">A tanúsítvány rendszergazdája e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8a5-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="6e8a5-115">-FirstName</span></span>
<span data-ttu-id="6e8a5-116">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8a5-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="6e8a5-117">-LastName</span></span>
<span data-ttu-id="6e8a5-118">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8a5-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6e8a5-119">-PhoneNumber</span></span>
<span data-ttu-id="6e8a5-120">A hitelességi tanúsítvány rendszergazdája által megadott telefonszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8a5-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e8a5-121">-Confirm</span></span>
<span data-ttu-id="6e8a5-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8a5-123">-WhatIf</span></span>
<span data-ttu-id="6e8a5-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8a5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8a5-126">CommonParameters</span></span>
<span data-ttu-id="6e8a5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e8a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8a5-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8a5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e8a5-129">INPUTS</span></span>

### <span data-ttu-id="6e8a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6e8a5-130">System.String</span></span>

## <span data-ttu-id="6e8a5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e8a5-131">OUTPUTS</span></span>

### <span data-ttu-id="6e8a5-132">Microsoft. Azure. Command. PSKeyVaultCertificateAdministratorDetails. models.</span><span class="sxs-lookup"><span data-stu-id="6e8a5-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="6e8a5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e8a5-133">NOTES</span></span>

## <span data-ttu-id="6e8a5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e8a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="6e8a5-135">Új – AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6e8a5-135">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

