---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010682"
---
# <span data-ttu-id="49df7-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="49df7-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="49df7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49df7-102">SYNOPSIS</span></span>
<span data-ttu-id="49df7-103">Létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="49df7-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="49df7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49df7-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49df7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49df7-105">DESCRIPTION</span></span>
<span data-ttu-id="49df7-106">A **New-AzKeyVaultCertificateOrganizationDetail** parancsmag létrehoz egy memóriabeli tanúsítvány-szervezeti adatok objektumát.</span><span class="sxs-lookup"><span data-stu-id="49df7-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="49df7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49df7-107">EXAMPLES</span></span>

### <span data-ttu-id="49df7-108">Példa 1: szervezet adatai objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="49df7-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="49df7-109">Az első parancs létrehoz egy tanúsítvány-rendszergazdai részletek objektumot, majd a $AdminDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="49df7-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="49df7-110">A második parancs létrehoz egy Certificate Organization details objektumot, majd a $OrgDetails változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="49df7-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="49df7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49df7-111">PARAMETERS</span></span>

### <span data-ttu-id="49df7-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="49df7-112">-AdministratorDetails</span></span>
<span data-ttu-id="49df7-113">A tanúsítványok szervezeti rendszergazdáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="49df7-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="49df7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49df7-114">-DefaultProfile</span></span>
<span data-ttu-id="49df7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49df7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49df7-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="49df7-116">-Id</span></span>
<span data-ttu-id="49df7-117">A szervezet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49df7-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="49df7-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49df7-118">-Confirm</span></span>
<span data-ttu-id="49df7-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49df7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49df7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49df7-120">-WhatIf</span></span>
<span data-ttu-id="49df7-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49df7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49df7-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49df7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49df7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49df7-123">CommonParameters</span></span>
<span data-ttu-id="49df7-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49df7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49df7-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49df7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49df7-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49df7-126">INPUTS</span></span>

### <span data-ttu-id="49df7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="49df7-127">System.String</span></span>

### <span data-ttu-id="49df7-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. PSKeyVaultCertificateAdministratorDetails..................., Microsoft. Azure. PowerShell. parancsmagok. a</span><span class="sxs-lookup"><span data-stu-id="49df7-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="49df7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49df7-129">OUTPUTS</span></span>

### <span data-ttu-id="49df7-130">Microsoft. Azure. Command. PSKeyVaultCertificateOrganizationDetails. models.</span><span class="sxs-lookup"><span data-stu-id="49df7-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="49df7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49df7-131">NOTES</span></span>

## <span data-ttu-id="49df7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49df7-132">RELATED LINKS</span></span>

[<span data-ttu-id="49df7-133">Új – AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="49df7-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

