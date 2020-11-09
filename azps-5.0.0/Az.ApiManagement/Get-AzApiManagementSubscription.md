---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301649"
---
# <span data-ttu-id="ecb3e-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecb3e-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ecb3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb3e-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-103">Gets subscriptions.</span></span>

## <span data-ttu-id="ecb3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecb3e-104">SYNTAX</span></span>

### <span data-ttu-id="ecb3e-105">GetAllSubscriptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ecb3e-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb3e-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecb3e-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb3e-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="ecb3e-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb3e-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ecb3e-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb3e-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="ecb3e-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb3e-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="ecb3e-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb3e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecb3e-111">DESCRIPTION</span></span>
<span data-ttu-id="ecb3e-112">A **Get-AzApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="ecb3e-113">A billentyűk nem jelennek meg az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-113">Keys will not be included into result details.</span></span> <span data-ttu-id="ecb3e-114">A kulcsok beszerzéséhez használja a **Get-AzApiManagementSubscriptionKey**.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="ecb3e-115">Példák</span><span class="sxs-lookup"><span data-stu-id="ecb3e-115">EXAMPLES</span></span>

### <span data-ttu-id="ecb3e-116">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="ecb3e-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="ecb3e-117">Ez a parancs minden előfizetéshez bekerül.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="ecb3e-118">2. példa: előfizetés kérése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ecb3e-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="ecb3e-119">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="ecb3e-120">3. példa: a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ecb3e-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="ecb3e-121">Ez a parancs a felhasználó előfizetéseit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="ecb3e-122">Példa 4: a termékek összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ecb3e-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="ecb3e-123">Ez a parancs beolvassa a szorzat összes előfizetését.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="ecb3e-124">Példa 5: a hatókör összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ecb3e-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="ecb3e-125">Ez a parancs a globális API-tartományhoz konfigurált összes előfizetést megkapja</span><span class="sxs-lookup"><span data-stu-id="ecb3e-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="ecb3e-126">Példa 6: a termékek és a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ecb3e-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="ecb3e-127">Ez a parancs a globális API-tartományhoz konfigurált összes előfizetést megkapja</span><span class="sxs-lookup"><span data-stu-id="ecb3e-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="ecb3e-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecb3e-128">PARAMETERS</span></span>

### <span data-ttu-id="ecb3e-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ecb3e-129">-Context</span></span>
<span data-ttu-id="ecb3e-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ecb3e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb3e-131">-DefaultProfile</span></span>
<span data-ttu-id="ecb3e-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb3e-133">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="ecb3e-133">-ProductId</span></span>
<span data-ttu-id="ecb3e-134">Egy termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-134">Specifies a product identifier.</span></span>
<span data-ttu-id="ecb3e-135">Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="ecb3e-136">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ecb3e-136">-Scope</span></span>
<span data-ttu-id="ecb3e-137">Hatókör-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-137">Scope identifier.</span></span> <span data-ttu-id="ecb3e-138">Az előfizetés hatóköre, függetlenül attól, hogy az API-/apis/{apiId} vagy a/products/{productId}, illetve a globális API-tartomány/Apis vagy globális hatókör/.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="ecb3e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecb3e-139">-SubscriptionId</span></span>
<span data-ttu-id="ecb3e-140">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="ecb3e-141">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="ecb3e-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="ecb3e-142">-UserId</span></span>
<span data-ttu-id="ecb3e-143">A felhasználó azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-143">Specifies a user identifier.</span></span>
<span data-ttu-id="ecb3e-144">Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="ecb3e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb3e-145">CommonParameters</span></span>
<span data-ttu-id="ecb3e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecb3e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb3e-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ecb3e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb3e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecb3e-148">INPUTS</span></span>

### <span data-ttu-id="ecb3e-149">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecb3e-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecb3e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ecb3e-150">System.String</span></span>

## <span data-ttu-id="ecb3e-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecb3e-151">OUTPUTS</span></span>

### <span data-ttu-id="ecb3e-152">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecb3e-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ecb3e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecb3e-153">NOTES</span></span>

## <span data-ttu-id="ecb3e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecb3e-154">RELATED LINKS</span></span>

[<span data-ttu-id="ecb3e-155">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecb3e-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ecb3e-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecb3e-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="ecb3e-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecb3e-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


