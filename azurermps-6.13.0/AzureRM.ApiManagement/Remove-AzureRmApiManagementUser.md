---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501239"
---
# <span data-ttu-id="9fffb-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9fffb-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="9fffb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fffb-102">SYNOPSIS</span></span>
<span data-ttu-id="9fffb-103">Egy meglévő felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="9fffb-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fffb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fffb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fffb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fffb-105">DESCRIPTION</span></span>
<span data-ttu-id="9fffb-106">A **Remove-AzureRmApiManagementUser** parancsmag egy meglévő felhasználó törlésére.</span><span class="sxs-lookup"><span data-stu-id="9fffb-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="9fffb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9fffb-107">EXAMPLES</span></span>

### <span data-ttu-id="9fffb-108">Példa 1: felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="9fffb-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="9fffb-109">Ez a parancs egy meglévő felhasználót töröl.</span><span class="sxs-lookup"><span data-stu-id="9fffb-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="9fffb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fffb-110">PARAMETERS</span></span>

### <span data-ttu-id="9fffb-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9fffb-111">-Context</span></span>
<span data-ttu-id="9fffb-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9fffb-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9fffb-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9fffb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9fffb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fffb-114">-DefaultProfile</span></span>
<span data-ttu-id="9fffb-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fffb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fffb-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="9fffb-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="9fffb-117">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="9fffb-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="9fffb-118">Ha ez a paraméter nincs megadva, és létezik egy előfizetés, ez a parancsmag kivételt okoz.</span><span class="sxs-lookup"><span data-stu-id="9fffb-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="9fffb-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fffb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fffb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fffb-120">-PassThru</span></span>
<span data-ttu-id="9fffb-121">Azt jelzi, hogy ez a parancsmag az $Ture értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="9fffb-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9fffb-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="9fffb-122">-UserId</span></span>
<span data-ttu-id="9fffb-123">Megadja az eltávolítandó felhasználó AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="9fffb-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="9fffb-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9fffb-124">-Confirm</span></span>
<span data-ttu-id="9fffb-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fffb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fffb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fffb-126">-WhatIf</span></span>
<span data-ttu-id="9fffb-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9fffb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fffb-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fffb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fffb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fffb-129">CommonParameters</span></span>
<span data-ttu-id="9fffb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fffb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fffb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fffb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fffb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fffb-132">INPUTS</span></span>

### <span data-ttu-id="9fffb-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9fffb-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9fffb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9fffb-134">System.String</span></span>

### <span data-ttu-id="9fffb-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fffb-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fffb-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fffb-136">OUTPUTS</span></span>

### <span data-ttu-id="9fffb-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9fffb-137">System.Boolean</span></span>

## <span data-ttu-id="9fffb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fffb-138">NOTES</span></span>

## <span data-ttu-id="9fffb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fffb-139">RELATED LINKS</span></span>

[<span data-ttu-id="9fffb-140">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9fffb-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="9fffb-141">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9fffb-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="9fffb-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9fffb-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


