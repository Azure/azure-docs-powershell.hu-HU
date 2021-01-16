---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367777"
---
# <span data-ttu-id="40df1-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="40df1-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="40df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40df1-102">SYNOPSIS</span></span>
<span data-ttu-id="40df1-103">Létrehoz egy memória-tanúsítvány rendszergazdai részleteket tartalmazó objektumát.</span><span class="sxs-lookup"><span data-stu-id="40df1-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="40df1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40df1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40df1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40df1-105">DESCRIPTION</span></span>
<span data-ttu-id="40df1-106">A **New-AzKeyVaultCertificateAdministratorDetail** parancsmag létrehoz egy memória-tanúsítvány rendszergazdai adatait tartalmazó objektumot.</span><span class="sxs-lookup"><span data-stu-id="40df1-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="40df1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40df1-107">EXAMPLES</span></span>

### <span data-ttu-id="40df1-108">1. példa: Tanúsítvány-rendszergazdai részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="40df1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="40df1-109">Ez a parancs létrehoz egy memória-tanúsítvány rendszergazdai részleteket tartalmazó objektumot, majd tárolja azt a $AdminDetails változóban.</span><span class="sxs-lookup"><span data-stu-id="40df1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="40df1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40df1-110">PARAMETERS</span></span>

### <span data-ttu-id="40df1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40df1-111">-DefaultProfile</span></span>
<span data-ttu-id="40df1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="40df1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40df1-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="40df1-113">-EmailAddress</span></span>
<span data-ttu-id="40df1-114">A tanúsítvány-rendszergazda e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40df1-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="40df1-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="40df1-115">-FirstName</span></span>
<span data-ttu-id="40df1-116">A tanúsítvány-rendszergazda vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="40df1-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="40df1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="40df1-117">-LastName</span></span>
<span data-ttu-id="40df1-118">A tanúsítvány-rendszergazda vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="40df1-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="40df1-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="40df1-119">-PhoneNumber</span></span>
<span data-ttu-id="40df1-120">A tanúsítvány rendszergazdájának telefonszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40df1-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="40df1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40df1-121">-Confirm</span></span>
<span data-ttu-id="40df1-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40df1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40df1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40df1-123">-WhatIf</span></span>
<span data-ttu-id="40df1-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40df1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40df1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40df1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40df1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40df1-126">CommonParameters</span></span>
<span data-ttu-id="40df1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40df1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40df1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40df1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40df1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40df1-129">INPUTS</span></span>

### <span data-ttu-id="40df1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="40df1-130">System.String</span></span>

## <span data-ttu-id="40df1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40df1-131">OUTPUTS</span></span>

### <span data-ttu-id="40df1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="40df1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="40df1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40df1-133">NOTES</span></span>

## <span data-ttu-id="40df1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40df1-134">RELATED LINKS</span></span>

[<span data-ttu-id="40df1-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="40df1-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

