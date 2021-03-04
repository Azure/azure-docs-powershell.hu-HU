---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 17f7fe4046d5de9dfe288a96a00e8c03486e9c61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922137"
---
# <span data-ttu-id="b1295-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b1295-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="b1295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1295-102">SYNOPSIS</span></span>
<span data-ttu-id="b1295-103">Töröl egy meglévő felhasználót.</span><span class="sxs-lookup"><span data-stu-id="b1295-103">Deletes an existing user.</span></span>

## <span data-ttu-id="b1295-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1295-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1295-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1295-105">DESCRIPTION</span></span>
<span data-ttu-id="b1295-106">Az **Remove-AzApiManagementUser** parancsmag töröl egy meglévő felhasználót.</span><span class="sxs-lookup"><span data-stu-id="b1295-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="b1295-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1295-107">EXAMPLES</span></span>

### <span data-ttu-id="b1295-108">1. példa: Felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="b1295-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="b1295-109">Ez a parancs töröl egy meglévő felhasználót.</span><span class="sxs-lookup"><span data-stu-id="b1295-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="b1295-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1295-110">PARAMETERS</span></span>

### <span data-ttu-id="b1295-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b1295-111">-Context</span></span>
<span data-ttu-id="b1295-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1295-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b1295-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b1295-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b1295-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1295-114">-DefaultProfile</span></span>
<span data-ttu-id="b1295-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1295-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1295-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="b1295-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="b1295-117">Azt jelzi, hogy törölni szeretné-e a termékre vonatkozó előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="b1295-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="b1295-118">Ha nincs megadva ez a paraméter, és létezik előfizetés, ez a parancsmag kivételt tesz.</span><span class="sxs-lookup"><span data-stu-id="b1295-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="b1295-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1295-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1295-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1295-120">-PassThru</span></span>
<span data-ttu-id="b1295-121">Azt jelzi, hogy ez a parancsmag $Ture, ha sikeres, vagy egy $False értéket.</span><span class="sxs-lookup"><span data-stu-id="b1295-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b1295-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="b1295-122">-UserId</span></span>
<span data-ttu-id="b1295-123">Az eltávolítható felhasználó azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1295-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="b1295-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1295-124">-Confirm</span></span>
<span data-ttu-id="b1295-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b1295-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1295-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1295-126">-WhatIf</span></span>
<span data-ttu-id="b1295-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b1295-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1295-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1295-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1295-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1295-129">CommonParameters</span></span>
<span data-ttu-id="b1295-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1295-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1295-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1295-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1295-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1295-132">INPUTS</span></span>

### <span data-ttu-id="b1295-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1295-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1295-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b1295-134">System.String</span></span>

### <span data-ttu-id="b1295-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1295-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1295-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1295-136">OUTPUTS</span></span>

### <span data-ttu-id="b1295-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1295-137">System.Boolean</span></span>

## <span data-ttu-id="b1295-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1295-138">NOTES</span></span>

## <span data-ttu-id="b1295-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1295-139">RELATED LINKS</span></span>

[<span data-ttu-id="b1295-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b1295-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="b1295-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b1295-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="b1295-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b1295-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


