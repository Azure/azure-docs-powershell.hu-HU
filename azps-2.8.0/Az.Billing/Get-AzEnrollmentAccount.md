---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667656"
---
# <span data-ttu-id="5128c-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="5128c-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="5128c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5128c-102">SYNOPSIS</span></span>
<span data-ttu-id="5128c-103">Tanúsítványigénylési fiókok beszerzése</span><span class="sxs-lookup"><span data-stu-id="5128c-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="5128c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5128c-104">SYNTAX</span></span>

### <span data-ttu-id="5128c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5128c-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5128c-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="5128c-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5128c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5128c-107">DESCRIPTION</span></span>
<span data-ttu-id="5128c-108">A **Get-AzEnrollmentAccount** parancsmag tanúsítványigénylési fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="5128c-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="5128c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5128c-109">EXAMPLES</span></span>

### <span data-ttu-id="5128c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5128c-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="5128c-111">Az összes rendelkezésre álló tanúsítványigénylő fiók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="5128c-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="5128c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5128c-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="5128c-113">A megadott objektumazonosító beszerzése az igénylési fiókból</span><span class="sxs-lookup"><span data-stu-id="5128c-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="5128c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5128c-114">PARAMETERS</span></span>

### <span data-ttu-id="5128c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5128c-115">-DefaultProfile</span></span>
<span data-ttu-id="5128c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5128c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5128c-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5128c-117">-ObjectId</span></span>
<span data-ttu-id="5128c-118">ObjectId egy adott tanúsítványigénylési fiókból.</span><span class="sxs-lookup"><span data-stu-id="5128c-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5128c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5128c-119">CommonParameters</span></span>
<span data-ttu-id="5128c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5128c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5128c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5128c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5128c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5128c-122">INPUTS</span></span>

### <span data-ttu-id="5128c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="5128c-123">None</span></span>

## <span data-ttu-id="5128c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5128c-124">OUTPUTS</span></span>

### <span data-ttu-id="5128c-125">Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5128c-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5128c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5128c-126">NOTES</span></span>

## <span data-ttu-id="5128c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5128c-127">RELATED LINKS</span></span>
