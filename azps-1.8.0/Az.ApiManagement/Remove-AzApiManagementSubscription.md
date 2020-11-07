---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836939"
---
# <span data-ttu-id="4fc81-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc81-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4fc81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fc81-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc81-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4fc81-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="4fc81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fc81-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc81-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fc81-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc81-106">A **Remove-AzApiManagementSubscription** parancsmag törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4fc81-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="4fc81-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4fc81-107">EXAMPLES</span></span>

### <span data-ttu-id="4fc81-108">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="4fc81-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="4fc81-109">Ez a parancs törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4fc81-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="4fc81-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fc81-110">PARAMETERS</span></span>

### <span data-ttu-id="4fc81-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4fc81-111">-Context</span></span>
<span data-ttu-id="4fc81-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4fc81-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4fc81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc81-113">-DefaultProfile</span></span>
<span data-ttu-id="4fc81-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc81-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fc81-115">-PassThru</span></span>
<span data-ttu-id="4fc81-116">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $false értéke más.</span><span class="sxs-lookup"><span data-stu-id="4fc81-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="4fc81-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fc81-117">-SubscriptionId</span></span>
<span data-ttu-id="4fc81-118">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fc81-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="4fc81-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fc81-119">-Confirm</span></span>
<span data-ttu-id="4fc81-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fc81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc81-121">-WhatIf</span></span>
<span data-ttu-id="4fc81-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fc81-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc81-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fc81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc81-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc81-124">CommonParameters</span></span>
<span data-ttu-id="4fc81-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fc81-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc81-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc81-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc81-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc81-127">INPUTS</span></span>

### <span data-ttu-id="4fc81-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4fc81-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4fc81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc81-129">System.String</span></span>

### <span data-ttu-id="4fc81-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4fc81-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4fc81-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc81-131">OUTPUTS</span></span>

### <span data-ttu-id="4fc81-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fc81-132">System.Boolean</span></span>

## <span data-ttu-id="4fc81-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fc81-133">NOTES</span></span>

## <span data-ttu-id="4fc81-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc81-134">RELATED LINKS</span></span>

[<span data-ttu-id="4fc81-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc81-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="4fc81-136">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc81-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="4fc81-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4fc81-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


