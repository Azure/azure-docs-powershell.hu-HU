---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503123"
---
# <span data-ttu-id="dac48-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dac48-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="dac48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dac48-102">SYNOPSIS</span></span>
<span data-ttu-id="dac48-103">A meglévő előfizetés részleteinek megadása</span><span class="sxs-lookup"><span data-stu-id="dac48-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dac48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dac48-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dac48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dac48-105">DESCRIPTION</span></span>
<span data-ttu-id="dac48-106">A **set-AzureRmApiManagementSubscription** parancsmag meglévő előfizetés adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="dac48-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="dac48-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dac48-107">EXAMPLES</span></span>

### <span data-ttu-id="dac48-108">1. példa: az állapot és az elsődleges és másodlagos kulcsok beállítása az előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="dac48-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="dac48-109">Ez a parancs az előfizetések elsődleges és másodlagos kulcsait állítja be, és aktiválja.</span><span class="sxs-lookup"><span data-stu-id="dac48-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="dac48-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dac48-110">PARAMETERS</span></span>

### <span data-ttu-id="dac48-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dac48-111">-Context</span></span>
<span data-ttu-id="dac48-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac48-113">-DefaultProfile</span></span>
<span data-ttu-id="dac48-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dac48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="dac48-115">-ExpiresOn</span></span>
<span data-ttu-id="dac48-116">Az előfizetés lejárati dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="dac48-117">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="dac48-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dac48-118">-Name</span></span>
<span data-ttu-id="dac48-119">Az előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dac48-120">-PassThru</span></span>
<span data-ttu-id="dac48-121">passthru</span><span class="sxs-lookup"><span data-stu-id="dac48-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="dac48-122">-PrimaryKey</span></span>
<span data-ttu-id="dac48-123">Az előfizetés elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="dac48-124">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="dac48-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="dac48-125">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dac48-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="dac48-126">-SecondaryKey</span></span>
<span data-ttu-id="dac48-127">Az előfizetés másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="dac48-128">Ez a paraméter automatikusan jön létre, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="dac48-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="dac48-129">A paraméternek 1 – 300 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dac48-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-130">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="dac48-130">-State</span></span>
<span data-ttu-id="dac48-131">Az előfizetési állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-131">Specifies the subscription state.</span></span>
<span data-ttu-id="dac48-132">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="dac48-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="dac48-133">-StateComment</span></span>
<span data-ttu-id="dac48-134">Az előfizetés állapotának megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="dac48-135">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="dac48-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dac48-136">-SubscriptionId</span></span>
<span data-ttu-id="dac48-137">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dac48-137">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac48-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac48-138">CommonParameters</span></span>
<span data-ttu-id="dac48-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dac48-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac48-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dac48-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac48-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dac48-141">INPUTS</span></span>

### <span data-ttu-id="dac48-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="dac48-142">None</span></span>
<span data-ttu-id="dac48-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dac48-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dac48-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dac48-144">OUTPUTS</span></span>

### <span data-ttu-id="dac48-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="dac48-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="dac48-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dac48-146">NOTES</span></span>

## <span data-ttu-id="dac48-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dac48-147">RELATED LINKS</span></span>

[<span data-ttu-id="dac48-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dac48-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="dac48-149">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dac48-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="dac48-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dac48-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


