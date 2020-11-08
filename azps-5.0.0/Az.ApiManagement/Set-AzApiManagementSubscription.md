---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195431"
---
# <span data-ttu-id="fa311-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fa311-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="fa311-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa311-102">SYNOPSIS</span></span>
<span data-ttu-id="fa311-103">A meglévő előfizetés részleteinek megadása</span><span class="sxs-lookup"><span data-stu-id="fa311-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="fa311-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa311-104">SYNTAX</span></span>

### <span data-ttu-id="fa311-105">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa311-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa311-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="fa311-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa311-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa311-107">DESCRIPTION</span></span>
<span data-ttu-id="fa311-108">A **set-AzApiManagementSubscription** parancsmag meglévő előfizetés adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="fa311-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="fa311-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fa311-109">EXAMPLES</span></span>

### <span data-ttu-id="fa311-110">1. példa: az állapot és az elsődleges és másodlagos kulcsok beállítása az előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="fa311-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="fa311-111">Ez a parancs az előfizetések elsődleges és másodlagos kulcsait állítja be, és aktiválja.</span><span class="sxs-lookup"><span data-stu-id="fa311-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="fa311-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa311-112">PARAMETERS</span></span>

### <span data-ttu-id="fa311-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fa311-113">-Context</span></span>
<span data-ttu-id="fa311-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa311-115">-DefaultProfile</span></span>
<span data-ttu-id="fa311-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa311-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa311-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="fa311-117">-ExpiresOn</span></span>
<span data-ttu-id="fa311-118">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="fa311-119">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="fa311-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa311-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa311-120">-InputObject</span></span>
<span data-ttu-id="fa311-121">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="fa311-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="fa311-122">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fa311-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa311-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa311-123">-Name</span></span>
<span data-ttu-id="fa311-124">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="fa311-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa311-125">-PassThru</span></span>
<span data-ttu-id="fa311-126">passthru</span><span class="sxs-lookup"><span data-stu-id="fa311-126">passthru</span></span>

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

### <span data-ttu-id="fa311-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fa311-127">-PrimaryKey</span></span>
<span data-ttu-id="fa311-128">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="fa311-129">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="fa311-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="fa311-130">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fa311-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="fa311-131">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="fa311-131">-Scope</span></span>
<span data-ttu-id="fa311-132">Az előfizetés hatóköre, függetlenül attól, hogy az API-/apis/{apiId} vagy a/products/{productId}, illetve a globális API-tartomány/Apis vagy globális hatókör/.</span><span class="sxs-lookup"><span data-stu-id="fa311-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="fa311-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fa311-133">This parameter is required.</span></span>

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

### <span data-ttu-id="fa311-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="fa311-134">-SecondaryKey</span></span>
<span data-ttu-id="fa311-135">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="fa311-136">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="fa311-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="fa311-137">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fa311-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="fa311-138">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="fa311-138">-State</span></span>
<span data-ttu-id="fa311-139">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-139">Specifies the subscription state.</span></span>
<span data-ttu-id="fa311-140">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="fa311-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="fa311-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="fa311-141">-StateComment</span></span>
<span data-ttu-id="fa311-142">Az előfizetés állapotának megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="fa311-143">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="fa311-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="fa311-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa311-144">-SubscriptionId</span></span>
<span data-ttu-id="fa311-145">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa311-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa311-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="fa311-146">-UserId</span></span>
<span data-ttu-id="fa311-147">Az előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="fa311-147">The owner of the subscription.</span></span> <span data-ttu-id="fa311-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fa311-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa311-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa311-149">-Confirm</span></span>
<span data-ttu-id="fa311-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa311-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa311-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa311-151">-WhatIf</span></span>
<span data-ttu-id="fa311-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa311-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa311-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa311-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa311-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa311-154">CommonParameters</span></span>
<span data-ttu-id="fa311-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa311-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa311-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa311-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa311-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa311-157">INPUTS</span></span>

### <span data-ttu-id="fa311-158">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fa311-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fa311-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fa311-159">System.String</span></span>

### <span data-ttu-id="fa311-160">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fa311-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fa311-161">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fa311-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fa311-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa311-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa311-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa311-163">OUTPUTS</span></span>

### <span data-ttu-id="fa311-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fa311-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="fa311-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa311-165">NOTES</span></span>

## <span data-ttu-id="fa311-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa311-166">RELATED LINKS</span></span>

[<span data-ttu-id="fa311-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fa311-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="fa311-168">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fa311-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="fa311-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fa311-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

