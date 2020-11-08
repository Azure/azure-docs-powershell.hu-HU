---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194130"
---
# <span data-ttu-id="808cc-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="808cc-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="808cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="808cc-102">SYNOPSIS</span></span>
<span data-ttu-id="808cc-103">Tanúsítványigénylési fiókok beszerzése</span><span class="sxs-lookup"><span data-stu-id="808cc-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="808cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="808cc-104">SYNTAX</span></span>

### <span data-ttu-id="808cc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="808cc-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808cc-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="808cc-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808cc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="808cc-107">DESCRIPTION</span></span>
<span data-ttu-id="808cc-108">A **Get-AzEnrollmentAccount** parancsmag tanúsítványigénylési fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="808cc-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="808cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="808cc-109">EXAMPLES</span></span>

### <span data-ttu-id="808cc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="808cc-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="808cc-111">Az összes rendelkezésre álló tanúsítványigénylő fiók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="808cc-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="808cc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="808cc-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="808cc-113">A megadott objektumazonosító beszerzése az igénylési fiókból</span><span class="sxs-lookup"><span data-stu-id="808cc-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="808cc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="808cc-114">PARAMETERS</span></span>

### <span data-ttu-id="808cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808cc-115">-DefaultProfile</span></span>
<span data-ttu-id="808cc-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="808cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="808cc-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="808cc-117">-ObjectId</span></span>
<span data-ttu-id="808cc-118">ObjectId egy adott tanúsítványigénylési fiókból.</span><span class="sxs-lookup"><span data-stu-id="808cc-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="808cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808cc-119">CommonParameters</span></span>
<span data-ttu-id="808cc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="808cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808cc-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808cc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808cc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="808cc-122">INPUTS</span></span>

### <span data-ttu-id="808cc-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="808cc-123">None</span></span>

## <span data-ttu-id="808cc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="808cc-124">OUTPUTS</span></span>

### <span data-ttu-id="808cc-125">Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="808cc-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="808cc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="808cc-126">NOTES</span></span>

## <span data-ttu-id="808cc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="808cc-127">RELATED LINKS</span></span>
