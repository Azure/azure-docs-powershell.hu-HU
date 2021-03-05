---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ee2be43882eb434d8bbc533e0d10722f63427a83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001349"
---
# <span data-ttu-id="5fff3-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="5fff3-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="5fff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fff3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fff3-103">Létrehoz egy in-memory certificate organization details object.</span><span class="sxs-lookup"><span data-stu-id="5fff3-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="5fff3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fff3-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fff3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fff3-105">DESCRIPTION</span></span>
<span data-ttu-id="5fff3-106">A **New-AzKeyVaultCertificateOrganizationDetail parancsmag** létrehoz egy memória-tanúsítvány szervezeti részleteit tartalmazó objektumot.</span><span class="sxs-lookup"><span data-stu-id="5fff3-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="5fff3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fff3-107">EXAMPLES</span></span>

### <span data-ttu-id="5fff3-108">1. példa: Szervezeti részletek objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fff3-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="5fff3-109">Az első parancs létrehozza a tanúsítvány-rendszergazda adatait tartalmazó objektumot, majd azt a $AdminDetails tárolja.</span><span class="sxs-lookup"><span data-stu-id="5fff3-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="5fff3-110">A második parancs létrehoz egy tanúsítvány szervezeti részleteket tartalmazó objektumot, majd tárolja azt a $OrgDetails változóban.</span><span class="sxs-lookup"><span data-stu-id="5fff3-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="5fff3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fff3-111">PARAMETERS</span></span>

### <span data-ttu-id="5fff3-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="5fff3-112">-AdministratorDetails</span></span>
<span data-ttu-id="5fff3-113">A tanúsítványt kezelő szervezet rendszergazdáit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5fff3-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="5fff3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fff3-114">-DefaultProfile</span></span>
<span data-ttu-id="5fff3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fff3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fff3-116">-Id</span><span class="sxs-lookup"><span data-stu-id="5fff3-116">-Id</span></span>
<span data-ttu-id="5fff3-117">Megadja a szervezet azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="5fff3-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="5fff3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fff3-118">-Confirm</span></span>
<span data-ttu-id="5fff3-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5fff3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fff3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fff3-120">-WhatIf</span></span>
<span data-ttu-id="5fff3-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5fff3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fff3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fff3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fff3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fff3-123">CommonParameters</span></span>
<span data-ttu-id="5fff3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fff3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fff3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fff3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fff3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fff3-126">INPUTS</span></span>

### <span data-ttu-id="5fff3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5fff3-127">System.String</span></span>

### <span data-ttu-id="5fff3-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5fff3-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5fff3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fff3-129">OUTPUTS</span></span>

### <span data-ttu-id="5fff3-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="5fff3-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="5fff3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fff3-131">NOTES</span></span>

## <span data-ttu-id="5fff3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fff3-132">RELATED LINKS</span></span>

[<span data-ttu-id="5fff3-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="5fff3-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

