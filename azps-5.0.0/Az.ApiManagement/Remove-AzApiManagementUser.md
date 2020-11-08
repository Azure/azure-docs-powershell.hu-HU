---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186151"
---
# <span data-ttu-id="84c92-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="84c92-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="84c92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84c92-102">SYNOPSIS</span></span>
<span data-ttu-id="84c92-103">Egy meglévő felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="84c92-103">Deletes an existing user.</span></span>

## <span data-ttu-id="84c92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84c92-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84c92-105">DESCRIPTION</span></span>
<span data-ttu-id="84c92-106">A **Remove-AzApiManagementUser** parancsmag egy meglévő felhasználó törlésére.</span><span class="sxs-lookup"><span data-stu-id="84c92-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="84c92-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84c92-107">EXAMPLES</span></span>

### <span data-ttu-id="84c92-108">Példa 1: felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="84c92-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="84c92-109">Ez a parancs egy meglévő felhasználót töröl.</span><span class="sxs-lookup"><span data-stu-id="84c92-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="84c92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84c92-110">PARAMETERS</span></span>

### <span data-ttu-id="84c92-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="84c92-111">-Context</span></span>
<span data-ttu-id="84c92-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="84c92-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="84c92-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="84c92-113">This parameter is required.</span></span>

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

### <span data-ttu-id="84c92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c92-114">-DefaultProfile</span></span>
<span data-ttu-id="84c92-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84c92-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c92-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="84c92-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="84c92-117">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="84c92-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="84c92-118">Ha ez a paraméter nincs megadva, és létezik egy előfizetés, ez a parancsmag kivételt okoz.</span><span class="sxs-lookup"><span data-stu-id="84c92-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="84c92-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="84c92-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="84c92-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84c92-120">-PassThru</span></span>
<span data-ttu-id="84c92-121">Azt jelzi, hogy ez a parancsmag az $Ture értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="84c92-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="84c92-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="84c92-122">-UserId</span></span>
<span data-ttu-id="84c92-123">Megadja az eltávolítandó felhasználó AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="84c92-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="84c92-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84c92-124">-Confirm</span></span>
<span data-ttu-id="84c92-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84c92-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c92-126">-WhatIf</span></span>
<span data-ttu-id="84c92-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84c92-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c92-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84c92-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c92-129">CommonParameters</span></span>
<span data-ttu-id="84c92-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84c92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c92-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84c92-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c92-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c92-132">INPUTS</span></span>

### <span data-ttu-id="84c92-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84c92-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84c92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="84c92-134">System.String</span></span>

### <span data-ttu-id="84c92-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84c92-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84c92-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c92-136">OUTPUTS</span></span>

### <span data-ttu-id="84c92-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84c92-137">System.Boolean</span></span>

## <span data-ttu-id="84c92-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84c92-138">NOTES</span></span>

## <span data-ttu-id="84c92-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84c92-139">RELATED LINKS</span></span>

[<span data-ttu-id="84c92-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="84c92-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="84c92-141">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="84c92-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="84c92-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="84c92-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


