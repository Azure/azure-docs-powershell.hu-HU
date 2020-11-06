---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492904"
---
# <span data-ttu-id="9ddc5-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9ddc5-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9ddc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ddc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddc5-103">A meglévő előfizetés részleteinek megadása</span><span class="sxs-lookup"><span data-stu-id="9ddc5-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ddc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ddc5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ddc5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ddc5-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddc5-106">A **set-AzureRmApiManagementSubscription** parancsmag meglévő előfizetés adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="9ddc5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ddc5-107">EXAMPLES</span></span>

### <span data-ttu-id="9ddc5-108">1. példa: az állapot és az elsődleges és másodlagos kulcsok beállítása az előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="9ddc5-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="9ddc5-109">Ez a parancs az előfizetések elsődleges és másodlagos kulcsait állítja be, és aktiválja.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="9ddc5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ddc5-110">PARAMETERS</span></span>

### <span data-ttu-id="9ddc5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9ddc5-111">-Context</span></span>
<span data-ttu-id="9ddc5-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9ddc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddc5-113">-DefaultProfile</span></span>
<span data-ttu-id="9ddc5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc5-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="9ddc5-115">-ExpiresOn</span></span>
<span data-ttu-id="9ddc5-116">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="9ddc5-117">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9ddc5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ddc5-118">-Name</span></span>
<span data-ttu-id="9ddc5-119">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="9ddc5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ddc5-120">-PassThru</span></span>
<span data-ttu-id="9ddc5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="9ddc5-121">passthru</span></span>

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

### <span data-ttu-id="9ddc5-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9ddc5-122">-PrimaryKey</span></span>
<span data-ttu-id="9ddc5-123">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="9ddc5-124">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="9ddc5-125">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9ddc5-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9ddc5-126">-SecondaryKey</span></span>
<span data-ttu-id="9ddc5-127">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="9ddc5-128">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="9ddc5-129">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9ddc5-130">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="9ddc5-130">-State</span></span>
<span data-ttu-id="9ddc5-131">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-131">Specifies the subscription state.</span></span>
<span data-ttu-id="9ddc5-132">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9ddc5-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="9ddc5-133">-StateComment</span></span>
<span data-ttu-id="9ddc5-134">Az előfizetés állapotának megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="9ddc5-135">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9ddc5-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ddc5-136">-SubscriptionId</span></span>
<span data-ttu-id="9ddc5-137">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ddc5-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="9ddc5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddc5-138">CommonParameters</span></span>
<span data-ttu-id="9ddc5-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ddc5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddc5-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddc5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddc5-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ddc5-141">INPUTS</span></span>

### <span data-ttu-id="9ddc5-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ddc5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ddc5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ddc5-143">System.String</span></span>

### <span data-ttu-id="9ddc5-144">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0</span><span class="sxs-lookup"><span data-stu-id="9ddc5-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9ddc5-145">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9ddc5-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9ddc5-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ddc5-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ddc5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ddc5-147">OUTPUTS</span></span>

### <span data-ttu-id="9ddc5-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9ddc5-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="9ddc5-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ddc5-149">NOTES</span></span>

## <span data-ttu-id="9ddc5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ddc5-150">RELATED LINKS</span></span>

[<span data-ttu-id="9ddc5-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9ddc5-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9ddc5-152">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9ddc5-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9ddc5-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9ddc5-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


