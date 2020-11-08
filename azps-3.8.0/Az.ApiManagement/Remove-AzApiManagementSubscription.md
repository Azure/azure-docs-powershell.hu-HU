---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012138"
---
# <span data-ttu-id="8932f-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8932f-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="8932f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8932f-102">SYNOPSIS</span></span>
<span data-ttu-id="8932f-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8932f-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="8932f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8932f-104">SYNTAX</span></span>

### <span data-ttu-id="8932f-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8932f-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8932f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8932f-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8932f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8932f-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8932f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8932f-108">DESCRIPTION</span></span>
<span data-ttu-id="8932f-109">A **Remove-AzApiManagementSubscription** parancsmag törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8932f-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="8932f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8932f-110">EXAMPLES</span></span>

### <span data-ttu-id="8932f-111">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="8932f-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="8932f-112">Ez a parancs törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8932f-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="8932f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8932f-113">PARAMETERS</span></span>

### <span data-ttu-id="8932f-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8932f-114">-Context</span></span>
<span data-ttu-id="8932f-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8932f-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8932f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8932f-116">-DefaultProfile</span></span>
<span data-ttu-id="8932f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8932f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8932f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8932f-118">-InputObject</span></span>
<span data-ttu-id="8932f-119">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="8932f-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="8932f-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8932f-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8932f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8932f-121">-PassThru</span></span>
<span data-ttu-id="8932f-122">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $false értéke más.</span><span class="sxs-lookup"><span data-stu-id="8932f-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="8932f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8932f-123">-ResourceId</span></span>
<span data-ttu-id="8932f-124">A kar ResourceId az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8932f-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="8932f-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="8932f-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8932f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8932f-126">-SubscriptionId</span></span>
<span data-ttu-id="8932f-127">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8932f-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="8932f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8932f-128">-Confirm</span></span>
<span data-ttu-id="8932f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8932f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8932f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8932f-130">-WhatIf</span></span>
<span data-ttu-id="8932f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8932f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8932f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8932f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8932f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8932f-133">CommonParameters</span></span>
<span data-ttu-id="8932f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8932f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8932f-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8932f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8932f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8932f-136">INPUTS</span></span>

### <span data-ttu-id="8932f-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8932f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8932f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8932f-138">System.String</span></span>

### <span data-ttu-id="8932f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8932f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8932f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8932f-140">OUTPUTS</span></span>

### <span data-ttu-id="8932f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8932f-141">System.Boolean</span></span>

## <span data-ttu-id="8932f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8932f-142">NOTES</span></span>

## <span data-ttu-id="8932f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8932f-143">RELATED LINKS</span></span>

[<span data-ttu-id="8932f-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8932f-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="8932f-145">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8932f-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="8932f-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8932f-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


