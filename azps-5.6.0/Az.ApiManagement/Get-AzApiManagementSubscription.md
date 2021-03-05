---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 26e555be760a71defc7f21f5ffc84cada7a21d04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012854"
---
# <span data-ttu-id="b2717-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b2717-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="b2717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2717-102">SYNOPSIS</span></span>
<span data-ttu-id="b2717-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="b2717-103">Gets subscriptions.</span></span>

## <span data-ttu-id="b2717-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2717-104">SYNTAX</span></span>

### <span data-ttu-id="b2717-105">GetAllSubscriptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2717-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2717-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2717-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2717-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="b2717-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2717-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="b2717-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2717-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="b2717-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2717-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="b2717-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2717-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2717-111">DESCRIPTION</span></span>
<span data-ttu-id="b2717-112">A **Get-AzApiManagementSubscription** parancsmag kap egy adott előfizetést, vagy ha nincs előfizetés megadva, az összes előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b2717-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="b2717-113">A billentyűk nem szerepelnek az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="b2717-113">Keys will not be included into result details.</span></span> <span data-ttu-id="b2717-114">A kulcsok lekérthez használja a **Get-AzApiManagementSubscriptionKey fájlt.**</span><span class="sxs-lookup"><span data-stu-id="b2717-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="b2717-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2717-115">EXAMPLES</span></span>

### <span data-ttu-id="b2717-116">1. példa: Az összes előfizetés lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="b2717-117">Ez a parancs az összes előfizetést megkapja.</span><span class="sxs-lookup"><span data-stu-id="b2717-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="b2717-118">2. példa: Előfizetés lekérte egy megadott azonosítóval</span><span class="sxs-lookup"><span data-stu-id="b2717-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="b2717-119">Ez a parancs azonosító szerint kap egy előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b2717-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="b2717-120">3. példa: Egy felhasználó összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="b2717-121">Ez a parancs a felhasználó előfizetését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2717-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="b2717-122">4. példa: Termék összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="b2717-123">Ez a parancs a termék összes előfizetését megkapja.</span><span class="sxs-lookup"><span data-stu-id="b2717-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="b2717-124">5. példa: Hatókörre vonatkozó összes előfizetés lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-124">Example 5: Get all subscriptions for a Scope</span></span>
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

<span data-ttu-id="b2717-125">Ez a parancs a globális API-hatókörre konfigurált összes előfizetést lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="b2717-126">6. példa: Termék- és felhasználókör összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-126">Example 6: Get all subscriptions for a product and user scope</span></span>
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

<span data-ttu-id="b2717-127">Ez a parancs a globális API-hatókörre konfigurált összes előfizetést lekérte</span><span class="sxs-lookup"><span data-stu-id="b2717-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="b2717-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2717-128">PARAMETERS</span></span>

### <span data-ttu-id="b2717-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b2717-129">-Context</span></span>
<span data-ttu-id="b2717-130">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2717-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b2717-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2717-131">-DefaultProfile</span></span>
<span data-ttu-id="b2717-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2717-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2717-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b2717-133">-ProductId</span></span>
<span data-ttu-id="b2717-134">Termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2717-134">Specifies a product identifier.</span></span>
<span data-ttu-id="b2717-135">Ha meg van adva, ez a parancsmag az összes előfizetést megtalálja a termékazonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="b2717-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="b2717-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="b2717-136">-Scope</span></span>
<span data-ttu-id="b2717-137">Hatókör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b2717-137">Scope identifier.</span></span> <span data-ttu-id="b2717-138">Az előfizetés hatóköre, legyen az Api Scope /apis/{apiId} vagy Product Scope /products/{productId} vagy Global API Scope /apis vagy Global scope /.</span><span class="sxs-lookup"><span data-stu-id="b2717-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="b2717-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2717-139">-SubscriptionId</span></span>
<span data-ttu-id="b2717-140">Egy előfizetés-azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2717-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="b2717-141">Ha meg van adva, ez a parancsmag megtalálja az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="b2717-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="b2717-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="b2717-142">-UserId</span></span>
<span data-ttu-id="b2717-143">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2717-143">Specifies a user identifier.</span></span>
<span data-ttu-id="b2717-144">Ha meg van adva, ez a parancsmag az összes előfizetést megtalálja a felhasználói azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="b2717-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="b2717-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2717-145">CommonParameters</span></span>
<span data-ttu-id="b2717-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2717-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2717-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2717-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2717-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2717-148">INPUTS</span></span>

### <span data-ttu-id="b2717-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2717-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b2717-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b2717-150">System.String</span></span>

## <span data-ttu-id="b2717-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2717-151">OUTPUTS</span></span>

### <span data-ttu-id="b2717-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b2717-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="b2717-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2717-153">NOTES</span></span>

## <span data-ttu-id="b2717-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2717-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2717-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b2717-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="b2717-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b2717-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="b2717-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b2717-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


