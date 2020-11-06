---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492082"
---
# <span data-ttu-id="a966a-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a966a-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="a966a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a966a-102">SYNOPSIS</span></span>
<span data-ttu-id="a966a-103">Előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a966a-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a966a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a966a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a966a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a966a-105">DESCRIPTION</span></span>
<span data-ttu-id="a966a-106">A **New-AzureRmApiManagementSubscription** parancsmag előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a966a-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="a966a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a966a-107">EXAMPLES</span></span>

### <span data-ttu-id="a966a-108">1. példa: felhasználó előfizetése egy termékké</span><span class="sxs-lookup"><span data-stu-id="a966a-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="a966a-109">A parancs előfizet egy meglévő felhasználót egy terméket.</span><span class="sxs-lookup"><span data-stu-id="a966a-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="a966a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a966a-110">PARAMETERS</span></span>

### <span data-ttu-id="a966a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a966a-111">-Context</span></span>
<span data-ttu-id="a966a-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a966a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a966a-113">-DefaultProfile</span></span>
<span data-ttu-id="a966a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a966a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a966a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a966a-115">-Name</span></span>
<span data-ttu-id="a966a-116">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="a966a-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a966a-117">-PrimaryKey</span></span>
<span data-ttu-id="a966a-118">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="a966a-119">Ha ez a paraméter nincs megadva, a kulcs automatikusan jön létre.</span><span class="sxs-lookup"><span data-stu-id="a966a-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="a966a-120">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a966a-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a966a-121">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="a966a-121">-ProductId</span></span>
<span data-ttu-id="a966a-122">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyre fel szeretné venni a terméket.</span><span class="sxs-lookup"><span data-stu-id="a966a-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="a966a-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a966a-123">-SecondaryKey</span></span>
<span data-ttu-id="a966a-124">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="a966a-125">Ez a paraméter automatikusan jön létre, ha az nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a966a-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="a966a-126">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a966a-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a966a-127">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="a966a-127">-State</span></span>
<span data-ttu-id="a966a-128">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-128">Specifies the subscription state.</span></span>
<span data-ttu-id="a966a-129">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="a966a-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="a966a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a966a-130">-SubscriptionId</span></span>
<span data-ttu-id="a966a-131">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="a966a-132">Ez a paraméter akkor jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a966a-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="a966a-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="a966a-133">-UserId</span></span>
<span data-ttu-id="a966a-134">Az előfizetői azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a966a-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="a966a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a966a-135">CommonParameters</span></span>
<span data-ttu-id="a966a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a966a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a966a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a966a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a966a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a966a-138">INPUTS</span></span>

### <span data-ttu-id="a966a-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a966a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a966a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a966a-140">System.String</span></span>

### <span data-ttu-id="a966a-141">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0</span><span class="sxs-lookup"><span data-stu-id="a966a-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a966a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a966a-142">OUTPUTS</span></span>

### <span data-ttu-id="a966a-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a966a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="a966a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a966a-144">NOTES</span></span>

## <span data-ttu-id="a966a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a966a-145">RELATED LINKS</span></span>

[<span data-ttu-id="a966a-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a966a-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a966a-147">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a966a-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a966a-148">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a966a-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


