---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503299"
---
# <span data-ttu-id="a8fec-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8fec-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="a8fec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8fec-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fec-103">Előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8fec-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8fec-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8fec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8fec-105">DESCRIPTION</span></span>
<span data-ttu-id="a8fec-106">A **New-AzureRmApiManagementSubscription** parancsmag előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8fec-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="a8fec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8fec-107">EXAMPLES</span></span>

### <span data-ttu-id="a8fec-108">1. példa: felhasználó előfizetése egy termékké</span><span class="sxs-lookup"><span data-stu-id="a8fec-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="a8fec-109">A parancs előfizet egy meglévő felhasználót egy terméket.</span><span class="sxs-lookup"><span data-stu-id="a8fec-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="a8fec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8fec-110">PARAMETERS</span></span>

### <span data-ttu-id="a8fec-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a8fec-111">-Context</span></span>
<span data-ttu-id="a8fec-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a8fec-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8fec-113">-Name</span></span>
<span data-ttu-id="a8fec-114">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="a8fec-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a8fec-115">-PrimaryKey</span></span>
<span data-ttu-id="a8fec-116">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="a8fec-117">Ha ez a paraméter nincs megadva, a kulcs automatikusan jön létre.</span><span class="sxs-lookup"><span data-stu-id="a8fec-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="a8fec-118">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a8fec-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a8fec-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="a8fec-119">-ProductId</span></span>
<span data-ttu-id="a8fec-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyre fel szeretné venni a terméket.</span><span class="sxs-lookup"><span data-stu-id="a8fec-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="a8fec-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a8fec-121">-SecondaryKey</span></span>
<span data-ttu-id="a8fec-122">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="a8fec-123">Ez a paraméter automatikusan jön létre, ha az nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a8fec-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="a8fec-124">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a8fec-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a8fec-125">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="a8fec-125">-State</span></span>
<span data-ttu-id="a8fec-126">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-126">Specifies the subscription state.</span></span>
<span data-ttu-id="a8fec-127">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="a8fec-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="a8fec-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8fec-128">-SubscriptionId</span></span>
<span data-ttu-id="a8fec-129">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="a8fec-130">Ez a paraméter akkor jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a8fec-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="a8fec-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="a8fec-131">-UserId</span></span>
<span data-ttu-id="a8fec-132">Az előfizetői azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8fec-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="a8fec-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fec-133">-DefaultProfile</span></span>
<span data-ttu-id="a8fec-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8fec-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8fec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fec-135">CommonParameters</span></span>
<span data-ttu-id="a8fec-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8fec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fec-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fec-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8fec-138">INPUTS</span></span>

## <span data-ttu-id="a8fec-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8fec-139">OUTPUTS</span></span>

### <span data-ttu-id="a8fec-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8fec-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="a8fec-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8fec-141">NOTES</span></span>

## <span data-ttu-id="a8fec-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8fec-142">RELATED LINKS</span></span>

[<span data-ttu-id="a8fec-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8fec-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a8fec-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8fec-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a8fec-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8fec-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


