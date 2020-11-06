---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503324"
---
# <span data-ttu-id="6db08-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6db08-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="6db08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6db08-102">SYNOPSIS</span></span>
<span data-ttu-id="6db08-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="6db08-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6db08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6db08-104">SYNTAX</span></span>

### <span data-ttu-id="6db08-105">Az összes előfizetés lekérése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6db08-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db08-106">Beolvasás subsctiption-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6db08-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db08-107">Beolvasás felhasználói AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6db08-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db08-108">Get by Product ID</span><span class="sxs-lookup"><span data-stu-id="6db08-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6db08-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6db08-109">DESCRIPTION</span></span>
<span data-ttu-id="6db08-110">A **Get-AzureRmApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6db08-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="6db08-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6db08-111">EXAMPLES</span></span>

### <span data-ttu-id="6db08-112">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="6db08-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="6db08-113">Ez a parancs minden előfizetéshez bekerül.</span><span class="sxs-lookup"><span data-stu-id="6db08-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="6db08-114">2. példa: előfizetés kérése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6db08-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="6db08-115">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6db08-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="6db08-116">3. példa: a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6db08-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="6db08-117">Ez a parancs a felhasználó előfizetéseit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6db08-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="6db08-118">Példa 4: a termékek összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6db08-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="6db08-119">Ez a parancs beolvassa a szorzat összes előfizetését.</span><span class="sxs-lookup"><span data-stu-id="6db08-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="6db08-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6db08-120">PARAMETERS</span></span>

### <span data-ttu-id="6db08-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6db08-121">-Context</span></span>
<span data-ttu-id="6db08-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6db08-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db08-123">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="6db08-123">-ProductId</span></span>
<span data-ttu-id="6db08-124">Egy termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6db08-124">Specifies a product identifier.</span></span>
<span data-ttu-id="6db08-125">Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="6db08-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db08-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db08-126">-SubscriptionId</span></span>
<span data-ttu-id="6db08-127">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6db08-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="6db08-128">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="6db08-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db08-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="6db08-129">-UserId</span></span>
<span data-ttu-id="6db08-130">A felhasználó azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6db08-130">Specifies a user identifier.</span></span>
<span data-ttu-id="6db08-131">Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="6db08-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db08-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db08-132">-DefaultProfile</span></span>
<span data-ttu-id="6db08-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6db08-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db08-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db08-134">CommonParameters</span></span>
<span data-ttu-id="6db08-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6db08-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db08-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db08-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db08-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6db08-137">INPUTS</span></span>

## <span data-ttu-id="6db08-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6db08-138">OUTPUTS</span></span>

### <span data-ttu-id="6db08-139">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="6db08-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="6db08-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6db08-140">NOTES</span></span>

## <span data-ttu-id="6db08-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6db08-141">RELATED LINKS</span></span>

[<span data-ttu-id="6db08-142">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6db08-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6db08-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6db08-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6db08-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6db08-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


