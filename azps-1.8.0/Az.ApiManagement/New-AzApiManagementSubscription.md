---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836988"
---
# <span data-ttu-id="70771-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="70771-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="70771-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70771-102">SYNOPSIS</span></span>
<span data-ttu-id="70771-103">Előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="70771-103">Creates a subscription.</span></span>

## <span data-ttu-id="70771-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70771-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70771-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70771-105">DESCRIPTION</span></span>
<span data-ttu-id="70771-106">A **New-AzApiManagementSubscription** parancsmag előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="70771-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="70771-107">Példák</span><span class="sxs-lookup"><span data-stu-id="70771-107">EXAMPLES</span></span>

### <span data-ttu-id="70771-108">1. példa: felhasználó előfizetése egy termékké</span><span class="sxs-lookup"><span data-stu-id="70771-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="70771-109">A parancs előfizet egy meglévő felhasználót egy terméket.</span><span class="sxs-lookup"><span data-stu-id="70771-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="70771-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70771-110">PARAMETERS</span></span>

### <span data-ttu-id="70771-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="70771-111">-Context</span></span>
<span data-ttu-id="70771-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="70771-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70771-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70771-113">-DefaultProfile</span></span>
<span data-ttu-id="70771-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70771-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70771-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70771-115">-Name</span></span>
<span data-ttu-id="70771-116">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="70771-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="70771-117">-PrimaryKey</span></span>
<span data-ttu-id="70771-118">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="70771-119">Ha ez a paraméter nincs megadva, a kulcs automatikusan jön létre.</span><span class="sxs-lookup"><span data-stu-id="70771-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="70771-120">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="70771-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="70771-121">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="70771-121">-ProductId</span></span>
<span data-ttu-id="70771-122">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyre fel szeretné venni a terméket.</span><span class="sxs-lookup"><span data-stu-id="70771-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="70771-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="70771-123">-SecondaryKey</span></span>
<span data-ttu-id="70771-124">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="70771-125">Ez a paraméter automatikusan jön létre, ha az nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="70771-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="70771-126">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="70771-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="70771-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="70771-127">-State</span></span>
<span data-ttu-id="70771-128">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-128">Specifies the subscription state.</span></span>
<span data-ttu-id="70771-129">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="70771-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="70771-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70771-130">-SubscriptionId</span></span>
<span data-ttu-id="70771-131">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="70771-132">Ez a paraméter akkor jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="70771-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="70771-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="70771-133">-UserId</span></span>
<span data-ttu-id="70771-134">Az előfizetői azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="70771-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="70771-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70771-135">CommonParameters</span></span>
<span data-ttu-id="70771-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70771-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70771-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70771-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70771-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70771-138">INPUTS</span></span>

### <span data-ttu-id="70771-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="70771-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="70771-140">System. String</span><span class="sxs-lookup"><span data-stu-id="70771-140">System.String</span></span>

### <span data-ttu-id="70771-141">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70771-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="70771-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70771-142">OUTPUTS</span></span>

### <span data-ttu-id="70771-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="70771-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="70771-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70771-144">NOTES</span></span>

## <span data-ttu-id="70771-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70771-145">RELATED LINKS</span></span>

[<span data-ttu-id="70771-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="70771-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="70771-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="70771-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="70771-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="70771-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


