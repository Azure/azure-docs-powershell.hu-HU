---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350585"
---
# <span data-ttu-id="766d3-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="766d3-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="766d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766d3-102">SYNOPSIS</span></span>
<span data-ttu-id="766d3-103">Beállítja a meglévő előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="766d3-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="766d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="766d3-104">SYNTAX</span></span>

### <span data-ttu-id="766d3-105">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="766d3-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766d3-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="766d3-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="766d3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="766d3-107">DESCRIPTION</span></span>
<span data-ttu-id="766d3-108">A **Set-AzApiManagementSubscription** parancsmag beállítja a meglévő előfizetési adatokat.</span><span class="sxs-lookup"><span data-stu-id="766d3-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="766d3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="766d3-109">EXAMPLES</span></span>

### <span data-ttu-id="766d3-110">1. példa: Az előfizetés állapotának, elsődleges és másodlagos kulcsának beállítása</span><span class="sxs-lookup"><span data-stu-id="766d3-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="766d3-111">Ez a parancs beállítja az előfizetés elsődleges és másodlagos kulcsait, és aktiválja azt.</span><span class="sxs-lookup"><span data-stu-id="766d3-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="766d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766d3-112">PARAMETERS</span></span>

### <span data-ttu-id="766d3-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="766d3-113">-Context</span></span>
<span data-ttu-id="766d3-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="766d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766d3-115">-DefaultProfile</span></span>
<span data-ttu-id="766d3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="766d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766d3-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="766d3-117">-ExpiresOn</span></span>
<span data-ttu-id="766d3-118">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="766d3-119">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="766d3-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="766d3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="766d3-120">-InputObject</span></span>
<span data-ttu-id="766d3-121">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="766d3-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="766d3-122">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="766d3-122">This parameter is required.</span></span>

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

### <span data-ttu-id="766d3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="766d3-123">-Name</span></span>
<span data-ttu-id="766d3-124">Megadja az előfizetés nevét.</span><span class="sxs-lookup"><span data-stu-id="766d3-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="766d3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="766d3-125">-PassThru</span></span>
<span data-ttu-id="766d3-126">passthru</span><span class="sxs-lookup"><span data-stu-id="766d3-126">passthru</span></span>

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

### <span data-ttu-id="766d3-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="766d3-127">-PrimaryKey</span></span>
<span data-ttu-id="766d3-128">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="766d3-129">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="766d3-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="766d3-130">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="766d3-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="766d3-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="766d3-131">-Scope</span></span>
<span data-ttu-id="766d3-132">Az előfizetés hatóköre, legyen az Api Scope /apis/{apiId} vagy Product Scope /products/{productId} vagy Global API Scope /apis vagy Global scope /.</span><span class="sxs-lookup"><span data-stu-id="766d3-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="766d3-133">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="766d3-133">This parameter is required.</span></span>

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

### <span data-ttu-id="766d3-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="766d3-134">-SecondaryKey</span></span>
<span data-ttu-id="766d3-135">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="766d3-136">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="766d3-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="766d3-137">A paraméternek 1–300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="766d3-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="766d3-138">-State</span><span class="sxs-lookup"><span data-stu-id="766d3-138">-State</span></span>
<span data-ttu-id="766d3-139">Az előfizetés állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-139">Specifies the subscription state.</span></span>
<span data-ttu-id="766d3-140">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="766d3-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="766d3-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="766d3-141">-StateComment</span></span>
<span data-ttu-id="766d3-142">Az előfizetés állapota megjegyzést ad meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="766d3-143">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="766d3-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="766d3-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="766d3-144">-SubscriptionId</span></span>
<span data-ttu-id="766d3-145">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="766d3-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="766d3-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="766d3-146">-UserId</span></span>
<span data-ttu-id="766d3-147">Az előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="766d3-147">The owner of the subscription.</span></span> <span data-ttu-id="766d3-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="766d3-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="766d3-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="766d3-149">-Confirm</span></span>
<span data-ttu-id="766d3-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="766d3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766d3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766d3-151">-WhatIf</span></span>
<span data-ttu-id="766d3-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="766d3-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="766d3-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="766d3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766d3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766d3-154">CommonParameters</span></span>
<span data-ttu-id="766d3-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766d3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766d3-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="766d3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766d3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="766d3-157">INPUTS</span></span>

### <span data-ttu-id="766d3-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="766d3-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="766d3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="766d3-159">System.String</span></span>

### <span data-ttu-id="766d3-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="766d3-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="766d3-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="766d3-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="766d3-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="766d3-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="766d3-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="766d3-163">OUTPUTS</span></span>

### <span data-ttu-id="766d3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="766d3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="766d3-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="766d3-165">NOTES</span></span>

## <span data-ttu-id="766d3-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="766d3-166">RELATED LINKS</span></span>

[<span data-ttu-id="766d3-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="766d3-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="766d3-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="766d3-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="766d3-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="766d3-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


