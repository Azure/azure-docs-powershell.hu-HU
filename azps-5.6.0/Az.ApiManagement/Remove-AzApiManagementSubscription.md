---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 1a9c44bf88e3e6aba9fdc74e588ca8e8bb7ae792
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939010"
---
# <span data-ttu-id="5d9d3-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5d9d3-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="5d9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9d3-103">Töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="5d9d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d9d3-104">SYNTAX</span></span>

### <span data-ttu-id="5d9d3-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d9d3-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d9d3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d9d3-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d9d3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d9d3-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d9d3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d9d3-108">DESCRIPTION</span></span>
<span data-ttu-id="5d9d3-109">Az **Remove-AzApiManagementSubscription** parancsmag töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="5d9d3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d9d3-110">EXAMPLES</span></span>

### <span data-ttu-id="5d9d3-111">1. példa: Előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="5d9d3-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="5d9d3-112">Ez a parancs töröl egy meglévő előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="5d9d3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d9d3-113">PARAMETERS</span></span>

### <span data-ttu-id="5d9d3-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5d9d3-114">-Context</span></span>
<span data-ttu-id="5d9d3-115">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5d9d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9d3-116">-DefaultProfile</span></span>
<span data-ttu-id="5d9d3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d9d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d9d3-118">-InputObject</span></span>
<span data-ttu-id="5d9d3-119">A PsApiManagementSubscription példánya.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="5d9d3-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-120">This parameter is required.</span></span>

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

### <span data-ttu-id="5d9d3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d9d3-121">-PassThru</span></span>
<span data-ttu-id="5d9d3-122">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $false értéket.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="5d9d3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d9d3-123">-ResourceId</span></span>
<span data-ttu-id="5d9d3-124">Előfizetés Erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="5d9d3-125">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5d9d3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d9d3-126">-SubscriptionId</span></span>
<span data-ttu-id="5d9d3-127">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="5d9d3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d9d3-128">-Confirm</span></span>
<span data-ttu-id="5d9d3-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d9d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d9d3-130">-WhatIf</span></span>
<span data-ttu-id="5d9d3-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d9d3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d9d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9d3-133">CommonParameters</span></span>
<span data-ttu-id="5d9d3-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9d3-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d9d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9d3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d9d3-136">INPUTS</span></span>

### <span data-ttu-id="5d9d3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5d9d3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5d9d3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5d9d3-138">System.String</span></span>

### <span data-ttu-id="5d9d3-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5d9d3-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5d9d3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d9d3-140">OUTPUTS</span></span>

### <span data-ttu-id="5d9d3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d9d3-141">System.Boolean</span></span>

## <span data-ttu-id="5d9d3-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d9d3-142">NOTES</span></span>

## <span data-ttu-id="5d9d3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d9d3-143">RELATED LINKS</span></span>

[<span data-ttu-id="5d9d3-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5d9d3-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="5d9d3-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5d9d3-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="5d9d3-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5d9d3-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


