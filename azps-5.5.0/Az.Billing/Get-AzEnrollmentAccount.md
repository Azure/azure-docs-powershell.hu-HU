---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149235"
---
# <span data-ttu-id="7adee-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="7adee-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="7adee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adee-102">SYNOPSIS</span></span>
<span data-ttu-id="7adee-103">Regisztrációs fiókok igénylése.</span><span class="sxs-lookup"><span data-stu-id="7adee-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="7adee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7adee-104">SYNTAX</span></span>

### <span data-ttu-id="7adee-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7adee-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7adee-106">Single</span><span class="sxs-lookup"><span data-stu-id="7adee-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7adee-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7adee-107">DESCRIPTION</span></span>
<span data-ttu-id="7adee-108">A **Get-AzEnrollmentAccount** parancsmag regisztrációs fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="7adee-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="7adee-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7adee-109">EXAMPLES</span></span>

### <span data-ttu-id="7adee-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7adee-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="7adee-111">Szerezze be az összes elérhető regisztrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="7adee-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="7adee-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7adee-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="7adee-113">A megadott objektumazonosítóval szerezze be a regisztrációs fiókot.</span><span class="sxs-lookup"><span data-stu-id="7adee-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="7adee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7adee-114">PARAMETERS</span></span>

### <span data-ttu-id="7adee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adee-115">-DefaultProfile</span></span>
<span data-ttu-id="7adee-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7adee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7adee-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7adee-117">-ObjectId</span></span>
<span data-ttu-id="7adee-118">ObjectId of a specific enrollment account to get.</span><span class="sxs-lookup"><span data-stu-id="7adee-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="7adee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adee-119">CommonParameters</span></span>
<span data-ttu-id="7adee-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adee-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adee-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adee-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7adee-122">INPUTS</span></span>

### <span data-ttu-id="7adee-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7adee-123">None</span></span>

## <span data-ttu-id="7adee-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adee-124">OUTPUTS</span></span>

### <span data-ttu-id="7adee-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="7adee-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="7adee-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7adee-126">NOTES</span></span>

## <span data-ttu-id="7adee-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7adee-127">RELATED LINKS</span></span>
