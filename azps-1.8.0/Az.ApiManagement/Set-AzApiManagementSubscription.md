---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671666"
---
# <span data-ttu-id="59f93-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59f93-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="59f93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59f93-102">SYNOPSIS</span></span>
<span data-ttu-id="59f93-103">A meglévő előfizetés részleteinek megadása</span><span class="sxs-lookup"><span data-stu-id="59f93-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="59f93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59f93-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59f93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59f93-105">DESCRIPTION</span></span>
<span data-ttu-id="59f93-106">A **set-AzApiManagementSubscription** parancsmag meglévő előfizetés adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="59f93-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="59f93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59f93-107">EXAMPLES</span></span>

### <span data-ttu-id="59f93-108">1. példa: az állapot és az elsődleges és másodlagos kulcsok beállítása az előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="59f93-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="59f93-109">Ez a parancs az előfizetések elsődleges és másodlagos kulcsait állítja be, és aktiválja.</span><span class="sxs-lookup"><span data-stu-id="59f93-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="59f93-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59f93-110">PARAMETERS</span></span>

### <span data-ttu-id="59f93-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59f93-111">-Context</span></span>
<span data-ttu-id="59f93-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59f93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f93-113">-DefaultProfile</span></span>
<span data-ttu-id="59f93-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59f93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f93-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="59f93-115">-ExpiresOn</span></span>
<span data-ttu-id="59f93-116">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="59f93-117">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="59f93-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="59f93-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59f93-118">-Name</span></span>
<span data-ttu-id="59f93-119">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="59f93-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59f93-120">-PassThru</span></span>
<span data-ttu-id="59f93-121">passthru</span><span class="sxs-lookup"><span data-stu-id="59f93-121">passthru</span></span>

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

### <span data-ttu-id="59f93-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="59f93-122">-PrimaryKey</span></span>
<span data-ttu-id="59f93-123">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="59f93-124">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="59f93-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="59f93-125">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="59f93-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="59f93-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="59f93-126">-SecondaryKey</span></span>
<span data-ttu-id="59f93-127">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="59f93-128">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="59f93-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="59f93-129">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="59f93-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="59f93-130">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="59f93-130">-State</span></span>
<span data-ttu-id="59f93-131">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-131">Specifies the subscription state.</span></span>
<span data-ttu-id="59f93-132">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="59f93-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="59f93-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="59f93-133">-StateComment</span></span>
<span data-ttu-id="59f93-134">Az előfizetés állapotának megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="59f93-135">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="59f93-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="59f93-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59f93-136">-SubscriptionId</span></span>
<span data-ttu-id="59f93-137">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="59f93-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="59f93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f93-138">CommonParameters</span></span>
<span data-ttu-id="59f93-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59f93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f93-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f93-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f93-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59f93-141">INPUTS</span></span>

### <span data-ttu-id="59f93-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59f93-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59f93-143">System. String</span><span class="sxs-lookup"><span data-stu-id="59f93-143">System.String</span></span>

### <span data-ttu-id="59f93-144">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="59f93-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="59f93-145">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59f93-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59f93-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59f93-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59f93-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59f93-147">OUTPUTS</span></span>

### <span data-ttu-id="59f93-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59f93-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="59f93-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59f93-149">NOTES</span></span>

## <span data-ttu-id="59f93-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59f93-150">RELATED LINKS</span></span>

[<span data-ttu-id="59f93-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59f93-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="59f93-152">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59f93-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="59f93-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59f93-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


