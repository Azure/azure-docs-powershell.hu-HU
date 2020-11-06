---
external help file: Microsoft.Azure.Commands.Subscription.dll-Help.xml
Module Name: AzureRM.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription/new-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
ms.openlocfilehash: cc88f762f1e965eb4e46462f7d43074fa3fe4646
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504252"
---
# <span data-ttu-id="43f56-101">New-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="43f56-101">New-AzureRmSubscription</span></span>

## <span data-ttu-id="43f56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43f56-102">SYNOPSIS</span></span>
<span data-ttu-id="43f56-103">Azure-előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="43f56-103">Creates an Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43f56-104">SYNTAX</span></span>

```
New-AzureRmSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43f56-105">DESCRIPTION</span></span>
<span data-ttu-id="43f56-106">A **New-AzureRmSubscription** parancsmag Azure-előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="43f56-106">The **New-AzureRmSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="43f56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43f56-107">EXAMPLES</span></span>

### <span data-ttu-id="43f56-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43f56-108">Example 1</span></span>
```
PS C:\> New-AzureRmSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzureRmEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="43f56-109">Azure-előfizetést hoz létre a megadott ajánlat típussal rendelkező megadott tanúsítványigénylési fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="43f56-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="43f56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43f56-110">PARAMETERS</span></span>

### <span data-ttu-id="43f56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43f56-111">-AsJob</span></span>
<span data-ttu-id="43f56-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43f56-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f56-113">-DefaultProfile</span></span>
<span data-ttu-id="43f56-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43f56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43f56-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="43f56-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="43f56-116">Az előfizetés létrehozásakor használandó tanúsítványigénylő fiók neve.</span><span class="sxs-lookup"><span data-stu-id="43f56-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43f56-117">-Name</span></span>
<span data-ttu-id="43f56-118">A létrehozandó előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="43f56-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="43f56-119">-OfferType</span></span>
<span data-ttu-id="43f56-120">Az előfizetés létrehozásakor használandó ajánlat típusa.</span><span class="sxs-lookup"><span data-stu-id="43f56-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="43f56-121">-OwnerApplicationId</span></span>
<span data-ttu-id="43f56-122">Az alkalmazás SPN-ek (SPN-ek) tulajdonosi hozzáférést kapnak az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="43f56-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="43f56-123">-OwnerObjectId</span></span>
<span data-ttu-id="43f56-124">A felhasználó (k) vagy a csoport objektum (ok) azonosító (k) a tulajdonos hozzáférését az előfizetéshez kell adni.</span><span class="sxs-lookup"><span data-stu-id="43f56-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="43f56-125">-OwnerSignInName</span></span>
<span data-ttu-id="43f56-126">A felhasználó (k) hozzáférést kell biztosítani az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="43f56-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f56-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43f56-127">-Confirm</span></span>
<span data-ttu-id="43f56-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43f56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f56-129">-WhatIf</span></span>
<span data-ttu-id="43f56-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43f56-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43f56-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43f56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f56-132">CommonParameters</span></span>
<span data-ttu-id="43f56-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43f56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f56-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f56-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f56-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43f56-135">INPUTS</span></span>

### <span data-ttu-id="43f56-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="43f56-136">None</span></span>

## <span data-ttu-id="43f56-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43f56-137">OUTPUTS</span></span>

### <span data-ttu-id="43f56-138">Microsoft. Azure. Command. előfizetés. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="43f56-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="43f56-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43f56-139">NOTES</span></span>

## <span data-ttu-id="43f56-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43f56-140">RELATED LINKS</span></span>
