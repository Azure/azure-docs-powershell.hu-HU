---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187874"
---
# <span data-ttu-id="f1c33-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1c33-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="f1c33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1c33-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c33-103">Előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f1c33-103">Creates a subscription.</span></span>

## <span data-ttu-id="f1c33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1c33-104">SYNTAX</span></span>

### <span data-ttu-id="f1c33-105">OldSubscriptionModel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1c33-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c33-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="f1c33-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c33-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1c33-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c33-108">A **New-AzApiManagementSubscription** parancsmag előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f1c33-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="f1c33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f1c33-109">EXAMPLES</span></span>

### <span data-ttu-id="f1c33-110">1. példa: felhasználó előfizetése egy termékké</span><span class="sxs-lookup"><span data-stu-id="f1c33-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="f1c33-111">A parancs előfizet egy meglévő felhasználót egy terméket.</span><span class="sxs-lookup"><span data-stu-id="f1c33-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="f1c33-112">2. példa: előfizetés létrehozása az API összes hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="f1c33-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="f1c33-113">3. példa: előfizetés létrehozása a termékek hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="f1c33-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="f1c33-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1c33-114">PARAMETERS</span></span>

### <span data-ttu-id="f1c33-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="f1c33-115">-AllowTracing</span></span>
<span data-ttu-id="f1c33-116">Megjelölés, amely meghatározza, hogy a nyomkövetés engedélyezve van-e az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="f1c33-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="f1c33-117">Ez a választható paraméter és az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="f1c33-117">This is optional parameter and default is $null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f1c33-118">-Context</span></span>
<span data-ttu-id="f1c33-119">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1c33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c33-120">-DefaultProfile</span></span>
<span data-ttu-id="f1c33-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1c33-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c33-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1c33-122">-Name</span></span>
<span data-ttu-id="f1c33-123">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-123">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f1c33-124">-PrimaryKey</span></span>
<span data-ttu-id="f1c33-125">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="f1c33-126">Ha ez a paraméter nincs megadva, a kulcs automatikusan jön létre.</span><span class="sxs-lookup"><span data-stu-id="f1c33-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="f1c33-127">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f1c33-127">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-128">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="f1c33-128">-ProductId</span></span>
<span data-ttu-id="f1c33-129">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyre fel szeretné venni a terméket.</span><span class="sxs-lookup"><span data-stu-id="f1c33-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-130">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="f1c33-130">-Scope</span></span>
<span data-ttu-id="f1c33-131">Az előfizetés hatóköre, függetlenül attól, hogy az API-/apis/{apiId} vagy a/products/{productId}, illetve a globális API-tartomány/Apis vagy globális hatókör/.</span><span class="sxs-lookup"><span data-stu-id="f1c33-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="f1c33-132">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f1c33-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f1c33-133">-SecondaryKey</span></span>
<span data-ttu-id="f1c33-134">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="f1c33-135">Ez a paraméter automatikusan jön létre, ha az nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f1c33-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="f1c33-136">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f1c33-136">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-137">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f1c33-137">-State</span></span>
<span data-ttu-id="f1c33-138">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-138">Specifies the subscription state.</span></span>
<span data-ttu-id="f1c33-139">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="f1c33-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1c33-140">-SubscriptionId</span></span>
<span data-ttu-id="f1c33-141">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="f1c33-142">Ez a paraméter akkor jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f1c33-142">This parameter is generated if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="f1c33-143">-UserId</span></span>
<span data-ttu-id="f1c33-144">Az előfizetői azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1c33-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c33-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c33-145">CommonParameters</span></span>
<span data-ttu-id="f1c33-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1c33-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c33-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1c33-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c33-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c33-148">INPUTS</span></span>

### <span data-ttu-id="f1c33-149">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1c33-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1c33-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c33-150">System.String</span></span>

### <span data-ttu-id="f1c33-151">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f1c33-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f1c33-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c33-152">OUTPUTS</span></span>

### <span data-ttu-id="f1c33-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1c33-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="f1c33-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1c33-154">NOTES</span></span>

## <span data-ttu-id="f1c33-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1c33-155">RELATED LINKS</span></span>

[<span data-ttu-id="f1c33-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1c33-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="f1c33-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1c33-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="f1c33-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1c33-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)

