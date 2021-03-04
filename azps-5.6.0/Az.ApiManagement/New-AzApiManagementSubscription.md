---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 00186ae370b7f5ccaac14bbdc85ba6b1f7aaa762
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940609"
---
# <span data-ttu-id="8311a-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8311a-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="8311a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8311a-102">SYNOPSIS</span></span>
<span data-ttu-id="8311a-103">Létrehoz egy előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8311a-103">Creates a subscription.</span></span>

## <span data-ttu-id="8311a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8311a-104">SYNTAX</span></span>

### <span data-ttu-id="8311a-105">OldSubscriptionModel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8311a-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8311a-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="8311a-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8311a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8311a-107">DESCRIPTION</span></span>
<span data-ttu-id="8311a-108">A **New-AzApiManagementSubscription** parancsmag létrehoz egy előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8311a-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="8311a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8311a-109">EXAMPLES</span></span>

### <span data-ttu-id="8311a-110">1. példa: Felhasználó előfizetése termékre</span><span class="sxs-lookup"><span data-stu-id="8311a-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="8311a-111">Ez a parancs előfizet egy meglévő felhasználót egy termékre.</span><span class="sxs-lookup"><span data-stu-id="8311a-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="8311a-112">2. példa: Előfizetés létrehozása az összes Api-hatókör számára</span><span class="sxs-lookup"><span data-stu-id="8311a-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="8311a-113">3. példa: Előfizetés létrehozása termékhatókörre</span><span class="sxs-lookup"><span data-stu-id="8311a-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="8311a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8311a-114">PARAMETERS</span></span>

### <span data-ttu-id="8311a-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="8311a-115">-AllowTracing</span></span>
<span data-ttu-id="8311a-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span><span class="sxs-lookup"><span data-stu-id="8311a-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="8311a-117">Ez nem kötelező paraméter, és alapértelmezés szerint $null.</span><span class="sxs-lookup"><span data-stu-id="8311a-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="8311a-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8311a-118">-Context</span></span>
<span data-ttu-id="8311a-119">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8311a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8311a-120">-DefaultProfile</span></span>
<span data-ttu-id="8311a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8311a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8311a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8311a-122">-Name</span></span>
<span data-ttu-id="8311a-123">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="8311a-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="8311a-124">-PrimaryKey</span></span>
<span data-ttu-id="8311a-125">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="8311a-126">Ha nincs megadva ez a paraméter, a kulcs automatikusan létrejön.</span><span class="sxs-lookup"><span data-stu-id="8311a-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="8311a-127">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8311a-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="8311a-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8311a-128">-ProductId</span></span>
<span data-ttu-id="8311a-129">Annak a terméknek az azonosítója, amelyre elő szeretne fizetni.</span><span class="sxs-lookup"><span data-stu-id="8311a-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="8311a-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="8311a-130">-Scope</span></span>
<span data-ttu-id="8311a-131">Az előfizetés hatóköre, legyen az Api Scope /apis/{apiId} vagy Product Scope /products/{productId} vagy Global API Scope /apis vagy Global scope /.</span><span class="sxs-lookup"><span data-stu-id="8311a-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="8311a-132">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8311a-132">This parameter is required.</span></span>

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

### <span data-ttu-id="8311a-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="8311a-133">-SecondaryKey</span></span>
<span data-ttu-id="8311a-134">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="8311a-135">Ez a paraméter automatikusan létrejön, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="8311a-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="8311a-136">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8311a-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="8311a-137">-State</span><span class="sxs-lookup"><span data-stu-id="8311a-137">-State</span></span>
<span data-ttu-id="8311a-138">Az előfizetés állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-138">Specifies the subscription state.</span></span>
<span data-ttu-id="8311a-139">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="8311a-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="8311a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8311a-140">-SubscriptionId</span></span>
<span data-ttu-id="8311a-141">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="8311a-142">Ez a paraméter akkor jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="8311a-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="8311a-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="8311a-143">-UserId</span></span>
<span data-ttu-id="8311a-144">Az előfizetői azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8311a-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="8311a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8311a-145">CommonParameters</span></span>
<span data-ttu-id="8311a-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8311a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8311a-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8311a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8311a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8311a-148">INPUTS</span></span>

### <span data-ttu-id="8311a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8311a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8311a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8311a-150">System.String</span></span>

### <span data-ttu-id="8311a-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8311a-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8311a-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8311a-152">OUTPUTS</span></span>

### <span data-ttu-id="8311a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8311a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="8311a-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8311a-154">NOTES</span></span>

## <span data-ttu-id="8311a-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8311a-155">RELATED LINKS</span></span>

[<span data-ttu-id="8311a-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8311a-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="8311a-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8311a-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="8311a-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8311a-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


