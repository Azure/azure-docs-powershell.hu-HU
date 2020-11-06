---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492595"
---
# <span data-ttu-id="266fb-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="266fb-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="266fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="266fb-102">SYNOPSIS</span></span>
<span data-ttu-id="266fb-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="266fb-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="266fb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="266fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="266fb-105">DESCRIPTION</span></span>
<span data-ttu-id="266fb-106">A **Remove-AzureRmApiManagementSubscription** parancsmag törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="266fb-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="266fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="266fb-107">EXAMPLES</span></span>

### <span data-ttu-id="266fb-108">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="266fb-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="266fb-109">Ez a parancs törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="266fb-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="266fb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="266fb-110">PARAMETERS</span></span>

### <span data-ttu-id="266fb-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="266fb-111">-Context</span></span>
<span data-ttu-id="266fb-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="266fb-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="266fb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="266fb-113">-PassThru</span></span>
<span data-ttu-id="266fb-114">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $false értéke más.</span><span class="sxs-lookup"><span data-stu-id="266fb-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="266fb-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="266fb-115">-SubscriptionId</span></span>
<span data-ttu-id="266fb-116">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="266fb-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="266fb-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="266fb-117">-Confirm</span></span>
<span data-ttu-id="266fb-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="266fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="266fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266fb-119">-WhatIf</span></span>
<span data-ttu-id="266fb-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="266fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266fb-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="266fb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="266fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266fb-122">-DefaultProfile</span></span>
<span data-ttu-id="266fb-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="266fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266fb-124">CommonParameters</span></span>
<span data-ttu-id="266fb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="266fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266fb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266fb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="266fb-127">INPUTS</span></span>

## <span data-ttu-id="266fb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="266fb-128">OUTPUTS</span></span>

### <span data-ttu-id="266fb-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="266fb-129">Boolean</span></span>

## <span data-ttu-id="266fb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="266fb-130">NOTES</span></span>

## <span data-ttu-id="266fb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="266fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="266fb-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="266fb-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="266fb-133">Új – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="266fb-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="266fb-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="266fb-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


