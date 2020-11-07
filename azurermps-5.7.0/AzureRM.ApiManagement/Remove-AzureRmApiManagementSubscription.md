---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680835"
---
# <span data-ttu-id="3f342-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3f342-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="3f342-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f342-102">SYNOPSIS</span></span>
<span data-ttu-id="3f342-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3f342-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f342-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f342-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f342-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f342-105">DESCRIPTION</span></span>
<span data-ttu-id="3f342-106">A **Remove-AzureRmApiManagementSubscription** parancsmag törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3f342-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="3f342-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f342-107">EXAMPLES</span></span>

### <span data-ttu-id="3f342-108">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="3f342-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="3f342-109">Ez a parancs törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3f342-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="3f342-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f342-110">PARAMETERS</span></span>

### <span data-ttu-id="3f342-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3f342-111">-Context</span></span>
<span data-ttu-id="3f342-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3f342-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3f342-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f342-113">-DefaultProfile</span></span>
<span data-ttu-id="3f342-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f342-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3f342-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f342-115">-PassThru</span></span>
<span data-ttu-id="3f342-116">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $false értéke más.</span><span class="sxs-lookup"><span data-stu-id="3f342-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="3f342-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f342-117">-SubscriptionId</span></span>
<span data-ttu-id="3f342-118">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f342-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="3f342-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f342-119">-Confirm</span></span>
<span data-ttu-id="3f342-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f342-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f342-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f342-121">-WhatIf</span></span>
<span data-ttu-id="3f342-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f342-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f342-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f342-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f342-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f342-124">CommonParameters</span></span>
<span data-ttu-id="3f342-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f342-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f342-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f342-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f342-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f342-127">INPUTS</span></span>

### <span data-ttu-id="3f342-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f342-128">None</span></span>
<span data-ttu-id="3f342-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3f342-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f342-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f342-130">OUTPUTS</span></span>

### <span data-ttu-id="3f342-131">Logikai</span><span class="sxs-lookup"><span data-stu-id="3f342-131">Boolean</span></span>

## <span data-ttu-id="3f342-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f342-132">NOTES</span></span>

## <span data-ttu-id="3f342-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f342-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f342-134">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3f342-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="3f342-135">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3f342-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="3f342-136">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3f342-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


