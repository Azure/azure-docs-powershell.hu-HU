---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: c8c4a318f3d2e972e742afcbdc13350a0ff77a90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836937"
---
# <span data-ttu-id="008b8-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="008b8-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="008b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="008b8-102">SYNOPSIS</span></span>
<span data-ttu-id="008b8-103">Egy meglévő felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="008b8-103">Deletes an existing user.</span></span>

## <span data-ttu-id="008b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="008b8-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="008b8-105">DESCRIPTION</span></span>
<span data-ttu-id="008b8-106">A **Remove-AzApiManagementUser** parancsmag egy meglévő felhasználó törlésére.</span><span class="sxs-lookup"><span data-stu-id="008b8-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="008b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="008b8-107">EXAMPLES</span></span>

### <span data-ttu-id="008b8-108">Példa 1: felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="008b8-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="008b8-109">Ez a parancs egy meglévő felhasználót töröl.</span><span class="sxs-lookup"><span data-stu-id="008b8-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="008b8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="008b8-110">PARAMETERS</span></span>

### <span data-ttu-id="008b8-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="008b8-111">-Context</span></span>
<span data-ttu-id="008b8-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="008b8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="008b8-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="008b8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="008b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008b8-114">-DefaultProfile</span></span>
<span data-ttu-id="008b8-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="008b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008b8-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="008b8-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="008b8-117">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="008b8-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="008b8-118">Ha ez a paraméter nincs megadva, és létezik egy előfizetés, ez a parancsmag kivételt okoz.</span><span class="sxs-lookup"><span data-stu-id="008b8-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="008b8-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="008b8-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="008b8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="008b8-120">-PassThru</span></span>
<span data-ttu-id="008b8-121">Azt jelzi, hogy ez a parancsmag az $Ture értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="008b8-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="008b8-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="008b8-122">-UserId</span></span>
<span data-ttu-id="008b8-123">Megadja az eltávolítandó felhasználó AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="008b8-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="008b8-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="008b8-124">-Confirm</span></span>
<span data-ttu-id="008b8-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="008b8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008b8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008b8-126">-WhatIf</span></span>
<span data-ttu-id="008b8-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="008b8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008b8-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="008b8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008b8-129">CommonParameters</span></span>
<span data-ttu-id="008b8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="008b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008b8-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008b8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008b8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="008b8-132">INPUTS</span></span>

### <span data-ttu-id="008b8-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="008b8-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="008b8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="008b8-134">System.String</span></span>

### <span data-ttu-id="008b8-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="008b8-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="008b8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="008b8-136">OUTPUTS</span></span>

### <span data-ttu-id="008b8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="008b8-137">System.Boolean</span></span>

## <span data-ttu-id="008b8-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="008b8-138">NOTES</span></span>

## <span data-ttu-id="008b8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="008b8-139">RELATED LINKS</span></span>

[<span data-ttu-id="008b8-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="008b8-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="008b8-141">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="008b8-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="008b8-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="008b8-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


