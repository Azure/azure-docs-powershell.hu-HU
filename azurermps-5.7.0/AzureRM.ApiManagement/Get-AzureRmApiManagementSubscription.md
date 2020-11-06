---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492424"
---
# <span data-ttu-id="2f77d-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2f77d-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="2f77d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f77d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f77d-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="2f77d-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f77d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f77d-104">SYNTAX</span></span>

### <span data-ttu-id="2f77d-105">GetAllSubscriptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f77d-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f77d-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f77d-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f77d-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="2f77d-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f77d-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="2f77d-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f77d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f77d-109">DESCRIPTION</span></span>
<span data-ttu-id="2f77d-110">A **Get-AzureRmApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f77d-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="2f77d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2f77d-111">EXAMPLES</span></span>

### <span data-ttu-id="2f77d-112">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="2f77d-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="2f77d-113">Ez a parancs minden előfizetéshez bekerül.</span><span class="sxs-lookup"><span data-stu-id="2f77d-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="2f77d-114">2. példa: előfizetés kérése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="2f77d-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="2f77d-115">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2f77d-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="2f77d-116">3. példa: a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f77d-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="2f77d-117">Ez a parancs a felhasználó előfizetéseit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2f77d-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="2f77d-118">Példa 4: a termékek összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f77d-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="2f77d-119">Ez a parancs beolvassa a szorzat összes előfizetését.</span><span class="sxs-lookup"><span data-stu-id="2f77d-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="2f77d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f77d-120">PARAMETERS</span></span>

### <span data-ttu-id="2f77d-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2f77d-121">-Context</span></span>
<span data-ttu-id="2f77d-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2f77d-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f77d-123">-DefaultProfile</span></span>
<span data-ttu-id="2f77d-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f77d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2f77d-125">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="2f77d-125">-ProductId</span></span>
<span data-ttu-id="2f77d-126">Egy termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2f77d-126">Specifies a product identifier.</span></span>
<span data-ttu-id="2f77d-127">Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="2f77d-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f77d-128">-SubscriptionId</span></span>
<span data-ttu-id="2f77d-129">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f77d-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="2f77d-130">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="2f77d-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="2f77d-131">-UserId</span></span>
<span data-ttu-id="2f77d-132">A felhasználó azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f77d-132">Specifies a user identifier.</span></span>
<span data-ttu-id="2f77d-133">Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="2f77d-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f77d-134">CommonParameters</span></span>
<span data-ttu-id="2f77d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f77d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f77d-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f77d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f77d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f77d-137">INPUTS</span></span>

### <span data-ttu-id="2f77d-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f77d-138">None</span></span>
<span data-ttu-id="2f77d-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2f77d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f77d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f77d-140">OUTPUTS</span></span>

### <span data-ttu-id="2f77d-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2f77d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="2f77d-142">Az előfizetés részletei az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2f77d-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="2f77d-143">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="2f77d-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="2f77d-144">Az előfizetések listája az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2f77d-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="2f77d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f77d-145">NOTES</span></span>

## <span data-ttu-id="2f77d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f77d-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f77d-147">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2f77d-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="2f77d-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2f77d-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="2f77d-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2f77d-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


