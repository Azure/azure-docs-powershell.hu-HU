---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 5d3ad3481a57f2578678daa88c1f3e87e9893f7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667965"
---
# <span data-ttu-id="e5c5c-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e5c5c-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e5c5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c5c-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="e5c5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5c5c-104">SYNTAX</span></span>

### <span data-ttu-id="e5c5c-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5c5c-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c5c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5c5c-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c5c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c5c-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="e5c5c-109">A **Remove-AzApiManagementSubscription** parancsmag törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="e5c5c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e5c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="e5c5c-111">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="e5c5c-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="e5c5c-112">Ez a parancs törli a meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="e5c5c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5c5c-113">PARAMETERS</span></span>

### <span data-ttu-id="e5c5c-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e5c5c-114">-Context</span></span>
<span data-ttu-id="e5c5c-115">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e5c5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c5c-116">-DefaultProfile</span></span>
<span data-ttu-id="e5c5c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c5c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c5c-118">-InputObject</span></span>
<span data-ttu-id="e5c5c-119">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="e5c5c-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-120">This parameter is required.</span></span>

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

### <span data-ttu-id="e5c5c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5c5c-121">-PassThru</span></span>
<span data-ttu-id="e5c5c-122">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $false értéke más.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="e5c5c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c5c-123">-ResourceId</span></span>
<span data-ttu-id="e5c5c-124">A kar ResourceId az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="e5c5c-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e5c5c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c5c-126">-SubscriptionId</span></span>
<span data-ttu-id="e5c5c-127">Az előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="e5c5c-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5c5c-128">-Confirm</span></span>
<span data-ttu-id="e5c5c-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c5c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c5c-130">-WhatIf</span></span>
<span data-ttu-id="e5c5c-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c5c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c5c-133">CommonParameters</span></span>
<span data-ttu-id="e5c5c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5c5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c5c-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e5c5c-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c5c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5c5c-136">INPUTS</span></span>

### <span data-ttu-id="e5c5c-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5c5c-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5c5c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c5c-138">System.String</span></span>

### <span data-ttu-id="e5c5c-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5c5c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5c5c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5c5c-140">OUTPUTS</span></span>

### <span data-ttu-id="e5c5c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5c5c-141">System.Boolean</span></span>

## <span data-ttu-id="e5c5c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5c5c-142">NOTES</span></span>

## <span data-ttu-id="e5c5c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5c5c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5c5c-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e5c5c-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="e5c5c-145">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e5c5c-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="e5c5c-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e5c5c-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


