---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665667"
---
# <span data-ttu-id="44178-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="44178-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="44178-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44178-102">SYNOPSIS</span></span>
<span data-ttu-id="44178-103">Előfizetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="44178-103">Gets subscriptions.</span></span>

## <span data-ttu-id="44178-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44178-104">SYNTAX</span></span>

### <span data-ttu-id="44178-105">GetAllSubscriptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44178-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44178-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44178-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44178-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="44178-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44178-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="44178-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44178-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="44178-109">DESCRIPTION</span></span>
<span data-ttu-id="44178-110">A **Get-AzApiManagementSubscription** parancsmag megadott előfizetést kap, vagy minden előfizetést, ha nincs megadva előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44178-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="44178-111">Példák</span><span class="sxs-lookup"><span data-stu-id="44178-111">EXAMPLES</span></span>

### <span data-ttu-id="44178-112">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="44178-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="44178-113">Ez a parancs minden előfizetéshez bekerül.</span><span class="sxs-lookup"><span data-stu-id="44178-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="44178-114">2. példa: előfizetés kérése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="44178-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="44178-115">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="44178-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="44178-116">3. példa: a felhasználók összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="44178-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="44178-117">Ez a parancs a felhasználó előfizetéseit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44178-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="44178-118">Példa 4: a termékek összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="44178-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="44178-119">Ez a parancs beolvassa a szorzat összes előfizetését.</span><span class="sxs-lookup"><span data-stu-id="44178-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="44178-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44178-120">PARAMETERS</span></span>

### <span data-ttu-id="44178-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="44178-121">-Context</span></span>
<span data-ttu-id="44178-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="44178-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="44178-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44178-123">-DefaultProfile</span></span>
<span data-ttu-id="44178-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44178-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44178-125">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="44178-125">-ProductId</span></span>
<span data-ttu-id="44178-126">Egy termékazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="44178-126">Specifies a product identifier.</span></span>
<span data-ttu-id="44178-127">Ha meg van adva, ez a parancsmag minden előfizetést megtalál a termékazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="44178-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44178-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44178-128">-SubscriptionId</span></span>
<span data-ttu-id="44178-129">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="44178-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="44178-130">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="44178-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44178-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="44178-131">-UserId</span></span>
<span data-ttu-id="44178-132">A felhasználó azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="44178-132">Specifies a user identifier.</span></span>
<span data-ttu-id="44178-133">Ha meg van adva, ez a parancsmag megkeresi az összes előfizetést a felhasználói azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="44178-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44178-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44178-134">CommonParameters</span></span>
<span data-ttu-id="44178-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44178-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44178-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44178-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44178-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44178-137">INPUTS</span></span>

### <span data-ttu-id="44178-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="44178-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="44178-139">System. String</span><span class="sxs-lookup"><span data-stu-id="44178-139">System.String</span></span>

## <span data-ttu-id="44178-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44178-140">OUTPUTS</span></span>

### <span data-ttu-id="44178-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="44178-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="44178-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44178-142">NOTES</span></span>

## <span data-ttu-id="44178-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44178-143">RELATED LINKS</span></span>

[<span data-ttu-id="44178-144">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="44178-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="44178-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="44178-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="44178-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="44178-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


