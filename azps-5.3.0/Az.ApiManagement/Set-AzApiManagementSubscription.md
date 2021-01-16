---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381624"
---
# <span data-ttu-id="6bb85-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6bb85-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="6bb85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb85-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb85-103">Beállítja a meglévő előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="6bb85-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="6bb85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6bb85-104">SYNTAX</span></span>

### <span data-ttu-id="6bb85-105">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bb85-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb85-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="6bb85-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb85-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6bb85-107">DESCRIPTION</span></span>
<span data-ttu-id="6bb85-108">A **Set-AzApiManagementSubscription** parancsmag beállítja a meglévő előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="6bb85-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="6bb85-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6bb85-109">EXAMPLES</span></span>

### <span data-ttu-id="6bb85-110">1. példa: Az előfizetés állapotának, elsődleges és másodlagos kulcsának beállítása</span><span class="sxs-lookup"><span data-stu-id="6bb85-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="6bb85-111">Ez a parancs beállítja az előfizetés elsődleges és másodlagos kulcsait, és aktiválja azt.</span><span class="sxs-lookup"><span data-stu-id="6bb85-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="6bb85-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bb85-112">PARAMETERS</span></span>

### <span data-ttu-id="6bb85-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6bb85-113">-Context</span></span>
<span data-ttu-id="6bb85-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6bb85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb85-115">-DefaultProfile</span></span>
<span data-ttu-id="6bb85-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bb85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bb85-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="6bb85-117">-ExpiresOn</span></span>
<span data-ttu-id="6bb85-118">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="6bb85-119">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="6bb85-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="6bb85-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bb85-120">-InputObject</span></span>
<span data-ttu-id="6bb85-121">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="6bb85-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="6bb85-122">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="6bb85-122">This parameter is required.</span></span>

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

### <span data-ttu-id="6bb85-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6bb85-123">-Name</span></span>
<span data-ttu-id="6bb85-124">Megadja az előfizetés nevét.</span><span class="sxs-lookup"><span data-stu-id="6bb85-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="6bb85-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bb85-125">-PassThru</span></span>
<span data-ttu-id="6bb85-126">passthru</span><span class="sxs-lookup"><span data-stu-id="6bb85-126">passthru</span></span>

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

### <span data-ttu-id="6bb85-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="6bb85-127">-PrimaryKey</span></span>
<span data-ttu-id="6bb85-128">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="6bb85-129">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6bb85-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="6bb85-130">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6bb85-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="6bb85-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="6bb85-131">-Scope</span></span>
<span data-ttu-id="6bb85-132">Az előfizetés hatóköre, legyen az Api Scope /apis/{apiId} vagy Product Scope /products/{productId} vagy Global API Scope /apis vagy Global scope /.</span><span class="sxs-lookup"><span data-stu-id="6bb85-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="6bb85-133">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="6bb85-133">This parameter is required.</span></span>

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

### <span data-ttu-id="6bb85-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="6bb85-134">-SecondaryKey</span></span>
<span data-ttu-id="6bb85-135">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="6bb85-136">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6bb85-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="6bb85-137">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6bb85-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="6bb85-138">-State</span><span class="sxs-lookup"><span data-stu-id="6bb85-138">-State</span></span>
<span data-ttu-id="6bb85-139">Az előfizetés állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-139">Specifies the subscription state.</span></span>
<span data-ttu-id="6bb85-140">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="6bb85-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="6bb85-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="6bb85-141">-StateComment</span></span>
<span data-ttu-id="6bb85-142">Az előfizetés állapotát ékes megjegyzésként adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="6bb85-143">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="6bb85-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="6bb85-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bb85-144">-SubscriptionId</span></span>
<span data-ttu-id="6bb85-145">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bb85-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="6bb85-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="6bb85-146">-UserId</span></span>
<span data-ttu-id="6bb85-147">Az előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="6bb85-147">The owner of the subscription.</span></span> <span data-ttu-id="6bb85-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6bb85-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bb85-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bb85-149">-Confirm</span></span>
<span data-ttu-id="6bb85-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6bb85-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb85-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb85-151">-WhatIf</span></span>
<span data-ttu-id="6bb85-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6bb85-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bb85-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bb85-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb85-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb85-154">CommonParameters</span></span>
<span data-ttu-id="6bb85-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb85-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb85-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bb85-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb85-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb85-157">INPUTS</span></span>

### <span data-ttu-id="6bb85-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6bb85-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bb85-159">System.String</span><span class="sxs-lookup"><span data-stu-id="6bb85-159">System.String</span></span>

### <span data-ttu-id="6bb85-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="6bb85-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6bb85-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6bb85-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6bb85-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bb85-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bb85-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bb85-163">OUTPUTS</span></span>

### <span data-ttu-id="6bb85-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6bb85-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="6bb85-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6bb85-165">NOTES</span></span>

## <span data-ttu-id="6bb85-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bb85-166">RELATED LINKS</span></span>

[<span data-ttu-id="6bb85-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6bb85-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="6bb85-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6bb85-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="6bb85-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6bb85-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


