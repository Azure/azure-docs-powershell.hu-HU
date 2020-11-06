---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493242"
---
# <span data-ttu-id="92f91-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="92f91-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="92f91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92f91-102">SYNOPSIS</span></span>
<span data-ttu-id="92f91-103">Tanúsítványigénylési fiókok beszerzése</span><span class="sxs-lookup"><span data-stu-id="92f91-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92f91-104">SYNTAX</span></span>

### <span data-ttu-id="92f91-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92f91-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f91-106">Egyetlen</span><span class="sxs-lookup"><span data-stu-id="92f91-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f91-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92f91-107">DESCRIPTION</span></span>
<span data-ttu-id="92f91-108">A **Get-AzureRmEnrollmentAccount** parancsmag tanúsítványigénylési fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="92f91-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="92f91-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92f91-109">EXAMPLES</span></span>

### <span data-ttu-id="92f91-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92f91-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="92f91-111">Az összes rendelkezésre álló tanúsítványigénylő fiók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="92f91-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="92f91-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="92f91-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="92f91-113">A megadott objektumazonosító beszerzése az igénylési fiókból</span><span class="sxs-lookup"><span data-stu-id="92f91-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="92f91-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92f91-114">PARAMETERS</span></span>

### <span data-ttu-id="92f91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f91-115">-DefaultProfile</span></span>
<span data-ttu-id="92f91-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="92f91-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92f91-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="92f91-117">-ObjectId</span></span>
<span data-ttu-id="92f91-118">ObjectId egy adott tanúsítványigénylési fiókból.</span><span class="sxs-lookup"><span data-stu-id="92f91-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f91-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f91-119">CommonParameters</span></span>
<span data-ttu-id="92f91-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92f91-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f91-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f91-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f91-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92f91-122">INPUTS</span></span>

### <span data-ttu-id="92f91-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="92f91-123">None</span></span>

## <span data-ttu-id="92f91-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92f91-124">OUTPUTS</span></span>

### <span data-ttu-id="92f91-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. számlázás. models. PSEnrollmentAccount, Microsoft. Azure. commands. számlázás, verzió = 0.14.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="92f91-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="92f91-126">Microsoft. Azure. commands. számlázás. modellek. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="92f91-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="92f91-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92f91-127">NOTES</span></span>

## <span data-ttu-id="92f91-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92f91-128">RELATED LINKS</span></span>

