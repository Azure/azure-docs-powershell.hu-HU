---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: fb64d30618eb736434c34ae1d47059433b336779
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835725"
---
# <span data-ttu-id="5cef4-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="5cef4-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="5cef4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cef4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cef4-103">A "memória" tanúsítvány rendszergazdája adatai objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5cef4-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="5cef4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cef4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cef4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cef4-105">DESCRIPTION</span></span>
<span data-ttu-id="5cef4-106">A **New-AzKeyVaultCertificateAdministratorDetail** parancsmag egy memóriabeli tanúsítvány-rendszergazdai részletek objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5cef4-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="5cef4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5cef4-107">EXAMPLES</span></span>

### <span data-ttu-id="5cef4-108">Példa 1: tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5cef4-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="5cef4-109">A parancs a memória-tanúsítvány rendszergazdája adatai objektumot hozza létre, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5cef4-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="5cef4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cef4-110">PARAMETERS</span></span>

### <span data-ttu-id="5cef4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cef4-111">-DefaultProfile</span></span>
<span data-ttu-id="5cef4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5cef4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cef4-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5cef4-113">-EmailAddress</span></span>
<span data-ttu-id="5cef4-114">A tanúsítvány rendszergazdája e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cef4-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="5cef4-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="5cef4-115">-FirstName</span></span>
<span data-ttu-id="5cef4-116">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cef4-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="5cef4-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="5cef4-117">-LastName</span></span>
<span data-ttu-id="5cef4-118">A tanúsítvány rendszergazdája vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cef4-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="5cef4-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5cef4-119">-PhoneNumber</span></span>
<span data-ttu-id="5cef4-120">A hitelességi tanúsítvány rendszergazdája által megadott telefonszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cef4-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="5cef4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cef4-121">-Confirm</span></span>
<span data-ttu-id="5cef4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cef4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cef4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cef4-123">-WhatIf</span></span>
<span data-ttu-id="5cef4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cef4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cef4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cef4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cef4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cef4-126">CommonParameters</span></span>
<span data-ttu-id="5cef4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cef4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cef4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cef4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cef4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cef4-129">INPUTS</span></span>

### <span data-ttu-id="5cef4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5cef4-130">System.String</span></span>

## <span data-ttu-id="5cef4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cef4-131">OUTPUTS</span></span>

### <span data-ttu-id="5cef4-132">Microsoft. Azure. Command. PSKeyVaultCertificateAdministratorDetails. models.</span><span class="sxs-lookup"><span data-stu-id="5cef4-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="5cef4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cef4-133">NOTES</span></span>

## <span data-ttu-id="5cef4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cef4-134">RELATED LINKS</span></span>

[<span data-ttu-id="5cef4-135">Új – AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="5cef4-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

