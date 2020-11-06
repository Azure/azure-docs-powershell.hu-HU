---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493590"
---
# <span data-ttu-id="298e2-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="298e2-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="298e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="298e2-102">SYNOPSIS</span></span>
<span data-ttu-id="298e2-103">A meglévő előfizetés részleteinek megadása</span><span class="sxs-lookup"><span data-stu-id="298e2-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="298e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="298e2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="298e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="298e2-105">DESCRIPTION</span></span>
<span data-ttu-id="298e2-106">A **set-AzureRmApiManagementSubscription** parancsmag meglévő előfizetés adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="298e2-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="298e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="298e2-107">EXAMPLES</span></span>

### <span data-ttu-id="298e2-108">1. példa: az állapot és az elsődleges és másodlagos kulcsok beállítása az előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="298e2-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="298e2-109">Ez a parancs az előfizetések elsődleges és másodlagos kulcsait állítja be, és aktiválja.</span><span class="sxs-lookup"><span data-stu-id="298e2-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="298e2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="298e2-110">PARAMETERS</span></span>

### <span data-ttu-id="298e2-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="298e2-111">-Context</span></span>
<span data-ttu-id="298e2-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="298e2-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="298e2-113">-ExpiresOn</span></span>
<span data-ttu-id="298e2-114">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="298e2-115">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="298e2-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="298e2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="298e2-116">-Name</span></span>
<span data-ttu-id="298e2-117">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="298e2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="298e2-118">-PassThru</span></span>
<span data-ttu-id="298e2-119">passthru</span><span class="sxs-lookup"><span data-stu-id="298e2-119">passthru</span></span>

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

### <span data-ttu-id="298e2-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="298e2-120">-PrimaryKey</span></span>
<span data-ttu-id="298e2-121">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="298e2-122">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="298e2-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="298e2-123">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="298e2-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="298e2-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="298e2-124">-SecondaryKey</span></span>
<span data-ttu-id="298e2-125">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="298e2-126">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="298e2-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="298e2-127">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="298e2-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="298e2-128">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="298e2-128">-State</span></span>
<span data-ttu-id="298e2-129">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-129">Specifies the subscription state.</span></span>
<span data-ttu-id="298e2-130">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="298e2-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="298e2-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="298e2-131">-StateComment</span></span>
<span data-ttu-id="298e2-132">Az előfizetés állapotának megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="298e2-133">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="298e2-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="298e2-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="298e2-134">-SubscriptionId</span></span>
<span data-ttu-id="298e2-135">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="298e2-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="298e2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298e2-136">-DefaultProfile</span></span>
<span data-ttu-id="298e2-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="298e2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="298e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298e2-138">CommonParameters</span></span>
<span data-ttu-id="298e2-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="298e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298e2-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="298e2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298e2-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="298e2-141">INPUTS</span></span>

## <span data-ttu-id="298e2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="298e2-142">OUTPUTS</span></span>

### <span data-ttu-id="298e2-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="298e2-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="298e2-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="298e2-144">NOTES</span></span>

## <span data-ttu-id="298e2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="298e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="298e2-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="298e2-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="298e2-147">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="298e2-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="298e2-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="298e2-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


