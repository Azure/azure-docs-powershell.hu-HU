---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668094"
---
# <span data-ttu-id="2a35e-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a35e-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="2a35e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a35e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a35e-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="2a35e-103">Gets subscriptions.</span></span>

## <span data-ttu-id="2a35e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a35e-104">SYNTAX</span></span>

### <span data-ttu-id="2a35e-105">GetAllSubscriptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a35e-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a35e-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a35e-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a35e-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="2a35e-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a35e-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="2a35e-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a35e-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="2a35e-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a35e-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="2a35e-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a35e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a35e-111">DESCRIPTION</span></span>
<span data-ttu-id="2a35e-112">A **Get-AzApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a35e-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="2a35e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2a35e-113">EXAMPLES</span></span>

### <span data-ttu-id="2a35e-114">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="2a35e-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="2a35e-115">Ez a parancs minden előfizetéshez bekerül.</span><span class="sxs-lookup"><span data-stu-id="2a35e-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="2a35e-116">2. példa: előfizetés kérése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="2a35e-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="2a35e-117">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2a35e-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="2a35e-118">3. példa: a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a35e-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="2a35e-119">Ez a parancs a felhasználó előfizetéseit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2a35e-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="2a35e-120">Példa 4: a termékek összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a35e-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="2a35e-121">Ez a parancs beolvassa a szorzat összes előfizetését.</span><span class="sxs-lookup"><span data-stu-id="2a35e-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="2a35e-122">Példa 5: a hatókör összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a35e-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="2a35e-123">Ez a parancs a globális API-tartományhoz konfigurált összes előfizetést megkapja</span><span class="sxs-lookup"><span data-stu-id="2a35e-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="2a35e-124">Példa 5: a termékek és a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2a35e-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="2a35e-125">Ez a parancs a globális API-tartományhoz konfigurált összes előfizetést megkapja</span><span class="sxs-lookup"><span data-stu-id="2a35e-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="2a35e-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a35e-126">PARAMETERS</span></span>

### <span data-ttu-id="2a35e-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2a35e-127">-Context</span></span>
<span data-ttu-id="2a35e-128">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a35e-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a35e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a35e-129">-DefaultProfile</span></span>
<span data-ttu-id="2a35e-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a35e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a35e-131">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="2a35e-131">-ProductId</span></span>
<span data-ttu-id="2a35e-132">Egy termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a35e-132">Specifies a product identifier.</span></span>
<span data-ttu-id="2a35e-133">Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="2a35e-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a35e-134">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="2a35e-134">-Scope</span></span>
<span data-ttu-id="2a35e-135">Hatókör-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2a35e-135">Scope identifier.</span></span> <span data-ttu-id="2a35e-136">Az előfizetés hatóköre, függetlenül attól, hogy az API-/apis/{apiId} vagy a/products/{productId}, illetve a globális API-tartomány/Apis vagy globális hatókör/.</span><span class="sxs-lookup"><span data-stu-id="2a35e-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a35e-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a35e-137">-SubscriptionId</span></span>
<span data-ttu-id="2a35e-138">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a35e-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="2a35e-139">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="2a35e-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a35e-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="2a35e-140">-UserId</span></span>
<span data-ttu-id="2a35e-141">A felhasználó azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a35e-141">Specifies a user identifier.</span></span>
<span data-ttu-id="2a35e-142">Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="2a35e-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a35e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a35e-143">CommonParameters</span></span>
<span data-ttu-id="2a35e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a35e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a35e-145">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a35e-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a35e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a35e-146">INPUTS</span></span>

### <span data-ttu-id="2a35e-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a35e-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a35e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2a35e-148">System.String</span></span>

## <span data-ttu-id="2a35e-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a35e-149">OUTPUTS</span></span>

### <span data-ttu-id="2a35e-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a35e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="2a35e-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a35e-151">NOTES</span></span>

## <span data-ttu-id="2a35e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a35e-152">RELATED LINKS</span></span>

[<span data-ttu-id="2a35e-153">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a35e-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="2a35e-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a35e-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="2a35e-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a35e-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


